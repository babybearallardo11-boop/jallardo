

# Enterprise Cloud Infrastructure: Client Operational Manual


## 1. System Architecture & Topology
* **Presentation Tier (`cloudnova-web`):** WordPress on Apache serving HTTP over port 80.
* **Database Tier (`cloudnova-db`):** MySQL 8.0 on isolated Docker network (`enterprise_backend`). Port 3306 is not published externally.
* **Storage Persistence:** Host volumes `wp_data` (`/var/www/html`) and `db_data` (`/var/lib/mysql`).

## 2. Accessing the Application

To determine the active server IP address assigned via DHCP, run:
\`\`\`bash
hostname -I | awk '{print $1}'
\`\`\`

Access the services via host browser using the discovered IP:
* **Web Portal (Public):** `http://<SERVER-IP>` (e.g., `http://192.168.100.71`)
* **Administrative Dashboard:** `http://<SERVER-IP>/wp-admin`
* **Remote Administration (SSH):** `ssh cloudadmin@<SERVER-IP>`
  
## 3. Service Management
```bash
cd ~/enterprise-stack
docker compose up -d    # Start infrastructure
docker compose ps       # Check health
docker compose logs -f  # Stream logs
docker compose down     # Stop infrastructure (preserves volumes)
```

## 4. Perimeter Security (UFW)
Enforces **Default Deny** ingress.
```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow 22/tcp comment 'Remote Administration SSH'
sudo ufw allow 80/tcp comment 'Cloud Application Web Port'
sudo ufw enable
```

## 5. Disaster Recovery & Backup Restoration
* Backups run daily at 02:00 AM via cron:
  `0 2 * * * /home/cloudadmin/enterprise-stack/automation-script.sh > /dev/null 2>&1`
* To restore a database backup:
```bash
gunzip < /backups/cloudnova_db_backup_[TIMESTAMP].sql.gz | docker exec -i cloudnova-db mysql -u root -pRootSuperSecurePassword2026! wordpress_db
```

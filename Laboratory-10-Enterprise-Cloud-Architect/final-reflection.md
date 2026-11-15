# Final Reflection: Building Resilient Infrastructure in CCM101

Progressing through CCM101 from Mission 1 to Mission 10 fundamentally changed how I approach system administration. Early on, my primary goal was just getting services to start without errors. By the end of the course, my focus shifted toward designing an environment that stays secure, recovers from failures, and runs without constant manual oversight.

At the beginning of the semester, working inside a headless Linux terminal, adjusting permissions, and troubleshooting network interfaces felt like disconnected drills. Deploying the complete stack for CloudNova Technologies in Mission 10 brought all of those skills together. Setting up a minimal Ubuntu Server inside a Type 2 hypervisor with bridged networking gave me a clear, hands-on picture of how underlying hardware and virtualized cloud instances actually operate beneath the surface.

Looking back at the final deployment, three core practices had the biggest impact on my understanding of modern infrastructure:

* **Isolating Application Tiers with Docker Compose:** Splitting the WordPress frontend and the MySQL 8.0 database into separate containers—while keeping port 3306 restricted to an internal Docker network—demonstrated the value of clean architecture. Using named volumes (`wp_data` and `db_data`) also showed me how to safely separate persistent data from disposable containers, making updates and rebuilds much safer.
* **Locking Down the Host with a Strict Firewall:** Applying a *Default Deny* rule in UFW and only opening SSH (22) and HTTP (80) emphasized that security starts at the network edge. Minimizing exposed ports reduces the attack surface and shields the containerized services running on the host.
* **Replacing Manual Tasks with Scheduled Automation:** Building a custom Bash backup script and automating it with a 02:00 AM `cron` job illustrated the difference between a basic test setup and a reliable production server. Dependable systems cannot rely on someone remembering to run routine commands; they need predictable, automated safeguards running in the background.

Finishing this capstone project showed me that strong cloud engineering is built on consistency, security, and recovery. Getting a server online once is only the starting line—hardening the system, isolating services, and automating backups are what truly make an architecture ready for the real world.


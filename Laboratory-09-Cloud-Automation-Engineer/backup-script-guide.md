# BACKUP SCRIPT GUIDE
## Mission 9 – The Cloud Automation Engineer

### 1. Introduction

This document explains the automated backup process created using Bash scripting in an Ubuntu environment. The purpose of the script is to compress the application data directory and save it inside a separate backup directory.

The script uses a timestamp so that every backup receives a unique filename.

### 2. Backup Script

Filename: `backup.sh`

```bash
#!/bin/bash

# Automated Backup Script for CloudNova Technologies
SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Create the backup directory if it does not exist
mkdir -p $BACKUP_DIR

# Compress the source directory into a tarball
tar -czf $BACKUP_DIR/backup_$TIMESTAMP.tar.gz $SOURCE_DIR

echo "Backup completed successfully at $TIMESTAMP!"
```

### 3. Explanation of the Script

**Shebang**

The `#!/bin/bash` line tells Linux to execute the file using the Bash shell.

**SOURCE_DIR**

This variable identifies the directory containing the application data that needs to be backed up.

**BACKUP_DIR**

This variable specifies where the compressed backup files will be stored.

**TIMESTAMP**

The `date` command generates the current date and time in a specific format. It helps give each backup a unique filename.

**mkdir -p**

This command creates the backup directory if it does not already exist. It prevents an error when the directory is already present.

**tar -czf**

This command compresses the application directory into a `.tar.gz` archive.

**echo**

The echo commands display messages indicating when the backup process starts and finishes.

### 4. File Permissions

Initially, Linux does not automatically allow a newly created text file to run as a program.

Command:

```bash
chmod +x backup.sh
```

The `chmod +x` command adds executable permission to the backup script. After applying this permission, the script can be executed using:

```bash
./backup.sh
```

### 5. Verify the Backup

Command:

```bash
ls -l backups/
```

This displays the files inside the backup directory. A successful execution should create a compressed file with a `.tar.gz` extension.

### 6. Cron Job Configuration

To automate the backup process, I configured a Cron schedule.

Cron expression:

```bash
0 2 * * * /root/backup.sh
```

This schedule tells Linux to execute the backup script every day at exactly 2:00 AM.

### 7. Explanation of the Five Cron Fields

| Field | Value | Meaning |
|---|---|---|
| Minute | 0 | At minute zero |
| Hour | 2 | At 2 AM |
| Day of Month | * | Every day of the month |
| Month | * | Every month |
| Day of Week | * | Every day of the week |

### 8. Cron Commands

```bash
crontab -l
```

Displays the currently installed Cron schedule.

```bash
env EDITOR=nano crontab -e
```

Opens the Cron configuration using the Nano text editor.

### 9. Important Considerations

Automated backups should be checked regularly to make sure files are being created correctly. Administrators should also verify that backup archives are readable and stored in a secure location.

A scheduled backup does not guarantee that data can be recovered, so testing the restoration process is also important.

### 10. Conclusion

Through this activity, I learned how to create a Bash script that automates the backup of application data. I also understood how executable permissions allow scripts to run and how Cron schedules repetitive tasks. These techniques are useful in cloud operations because they help reduce manual work and improve the consistency of server maintenance.

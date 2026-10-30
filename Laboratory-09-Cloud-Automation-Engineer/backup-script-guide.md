# <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/file-code-16.svg" width="28" height="28" /> Backup Script & Automation Technical Guide

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/terminal-16.svg" width="20" height="20" /> Full Automation Script (`backup.sh`)

```bash
#!/bin/bash

# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Check if the source directory exists
if [ ! -d "$SOURCE_DIR" ]; then
    echo "Error: Source directory '$SOURCE_DIR' does not exist."
    exit 1
fi

# Create the backup directory if it does not exist
if ! mkdir -p "$BACKUP_DIR"; then
    echo "Error: Failed to create backup directory."
    exit 1
fi

# Compress the source directory into a tarball (.tar.gz)
if tar -czf "$BACKUP_DIR/backup_$TIMESTAMP.tar.gz" -C "$(dirname "$SOURCE_DIR")" "$(basename "$SOURCE_DIR")"; then
    echo "Backup completed successfully at $TIMESTAMP!"
else
    echo "Error: Backup failed."
    exit 1
fi

<img src="https://raw.githubusercontent.com/primer/octicons/main/icons/info-16.svg" width="20" height="20" /> Script Configuration Analysis
1. The Role of chmod +x
By default, Linux prevents plain text files from executing as programs for security reasons. Running chmod +x backup.sh modifies the file's permission bits to grant execute (x) permissions, allowing the system to run the shell script directly.
2. Cron Schedule Expression Breakdown
The cron expression used to schedule the nightly backup is:

0 2 * * * /root/backup.sh

Each of the five time fields represents:
- 0 (Minute): The minute of the hour when the job runs (Minute 0).
- 2 (Hour): The hour of the day in 24-hour format (2:00 AM).
- * (Day of Month): Runs on every day of the month.
- * (Month): Runs in every month of the year.
- * (Day of Week): Runs on every day of the week.

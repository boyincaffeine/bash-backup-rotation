### 📄 `README.md`

````markdown
# Bash Backup Rotation Script

A simple Bash script to create compressed backups with a 5-day rotation policy. Ideal for small projects, local directories, and quick cron job integrations.

## 📦 Features

- Creates `.tar.gz` compressed backups of a target directory or file.
- Retains only the **5 most recent** backups.
- Automatically deletes older backups.
- Timestamped filenames for easy tracking.

## 🛠️ Requirements

- Unix-like OS (Linux, macOS, WSL, Git Bash)
- Bash shell
- `tar` command

## 🚀 Usage

```bash
./backup.sh <source_data_path> <backup_destination_path>
````

### Example:

```bash
./backup.sh data/ backups/
```

This will create a backup named like:

```
backups_25-05-21-23-23-05.tar.gz
```

And rotate to retain only the latest 5 backup files.

## 🧪 Output

```
Backup created
```

If more than 5 backups exist, older ones will be automatically deleted.

## 📅 Automate with Cron (Linux/macOS)

To run daily at midnight:

```bash
0 0 * * * /path/to/backup.sh /path/to/data /path/to/backups
```

## 📂 Sample Output Directory

```
backups_25-05-21-23-21-17.tar.gz
backups_25-05-21-23-21-21.tar.gz
backups_25-05-21-23-21-25.tar.gz
backups_25-05-21-23-22-13.tar.gz
backups_25-05-21-23-23-05.tar.gz
```

## 📃 License

This project is open-source under the [MIT License](LICENSE).

```

---

Would you like me to generate a `LICENSE` file too (MIT, Apache, etc.)? Or help you publish the repo on GitHub?
```


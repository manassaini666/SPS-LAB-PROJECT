# Student Record System (Linux)

A Bash project that demonstrates basic Linux file and directory commands by creating student records, preparing a report, and saving backup files.

## Requirements

- Linux or another environment with Bash and standard Unix commands (`mkdir`, `touch`, `cat`, `sort`, `uniq`, `head`, `tail`, `cp`, `mv`, and `rm`).
- The `student_record_system.sh` script in the current directory.

## Run the project

Open a terminal in the directory containing the script, then run:

```bash
chmod +x student_record_system.sh
./student_record_system.sh
```

Or run it without changing the file's executable permission:

```bash
bash student_record_system.sh
```

## Commands demonstrated

| Command | What it demonstrates |
| --- | --- |
| `pwd` | Shows the current directory. |
| `mkdir -p -v` | Creates the project folder structure and prints created directories. |
| `cd`, `cd ..`, `cd ../..`, `cd /` | Moves between directories. |
| `ls` | Lists directory contents. |
| `touch` | Creates empty files. |
| `echo` with `>` and `>>` | Writes data to a file and appends more data. |
| `cat`, `cat -n`, `cat file1 file2` | Displays file contents, with or without line numbers, and combines displayed contents. |
| `sort`, `uniq`, `head`, `tail` | Sorts and filters lines to prepare report output. |
| `cp`, `mv` | Copies, renames, and moves files. |
| `rm`, `rmdir` | Removes temporary files and empty directories. |

## Output structure

The script creates a `StudentRecords` directory with records, reports, and backup files. Based on the supplied project notes, the expected layout is:

```text
StudentRecords/
├── records/
│   └── sem5/
│       ├── students.txt
│       └── marks.txt
├── reports/
│   └── report_sem5.txt
└── backup/
    ├── students_backup.txt
    ├── marks.txt
    └── sorted.txt
```

## Demo presentation

You can present the project in this order:

1. **Introduce the goal:** “This Bash script demonstrates Linux commands by organizing student names and marks into files, generating a report, and making backups.”
2. **Show where you are and run it:**

   ```bash
   pwd
   ls
   bash student_record_system.sh
   ```

3. **Explain the commands as the script runs:** Point out directory creation and navigation, file creation and writing, displaying and sorting data, and copying or moving backups.
4. **Inspect the generated files:**

   ```bash
   find StudentRecords -maxdepth 4 -type f -print
   cat -n StudentRecords/records/sem5/students.txt
   cat StudentRecords/reports/report_sem5.txt
   ls -l StudentRecords/backup
   ```

5. **Close with the result:** Explain that the records are stored under `records/`, the report under `reports/`, and backup copies under `backup/`.

The attached project notes show this sample final list:

```text
Final list (no duplicates):
     1  101 Anita
     2  102 Vikas
     3  103 Rahul
     4  104 Sana
     5  105 Meena
```

Actual filenames or output can differ if the script has changed. To inspect its exact behavior, review `student_record_system.sh` before presenting.

# Linux File Permission Management

**Course:** Google Cybersecurity Professional Certificate — Course 4  
**Activity Type:** Portfolio Activity  
**Topic:** Managing File Permissions Using Linux Commands

---

## Scenario

As a security professional at a large organization, I was responsible for ensuring
users on the research team were authorized with appropriate file permissions.
My task was to examine existing permissions on the file system, identify any
mismatches, and modify permissions to remove unauthorized access.

---

## Steps Completed

### Step 1 — Check File and Directory Details

Used `ls -la` to list all files including hidden files with their permission strings.

```bash
ls -la
```

This command displays the permission string, owner, group, and file name for
every file and directory, including hidden files starting with `.`

---

### Step 2 — Describe the Permissions String

A permission string has 10 characters. Example: `-rwxrw-r--`

| Position | Meaning |
|---|---|
| 1 | File type (`-` = file, `d` = directory) |
| 2-4 | Owner permissions (read, write, execute) |
| 5-7 | Group permissions |
| 8-10 | Other permissions |

---

### Step 3 — Change File Permissions

Used `chmod` to remove unauthorized write access from "other" users.

```bash
chmod o-w filename.txt
```

---

### Step 4 — Change Permissions on a Hidden File

Hidden files start with `.` — same `chmod` syntax applies.

```bash
chmod u-x,g-w .hidden_file
```

---

### Step 5 — Change Directory Permissions

Used `chmod` to restrict execute permission on a directory for group.

```bash
chmod g-x directory_name
```

---

## Key Takeaways

- `ls -la` reveals full permission details including hidden files
- Permission strings are 10 characters: file type + owner + group + other
- `chmod` syntax: `chmod [who][+/-][permission] filename`
- Principle of least privilege: users should only have the access they need

---

## Skills Demonstrated

`Linux CLI` `chmod` `ls -la` `File Permission Management` `Least Privilege Principle`

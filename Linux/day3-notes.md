# Day 3 - Linux Commands

## 1. cp (Copy)

Copies a file or directory without removing the original.

### Example

```bash
cp test.txt backup.txt
```

---

## 2. mv (Move / Rename)

Moves a file to another location or renames it.

### Example

```bash
mv backup.txt old_backup.txt
```

---

## 3. head

Displays the first lines of a file.

### Example

```bash
head sample.txt
head -3 sample.txt
```

---

## 4. tail

Displays the last lines of a file.

### Example

```bash
tail sample.txt
tail -2 sample.txt
```

---

## 5. history

Shows previously executed commands.

### Example

```bash
history
history | grep touch
```

---

## 6. clear

Clears the terminal screen.

### Shortcut

```text
Ctrl + L
```

---

## 7. whoami

Displays the currently logged-in user.

### Example

```bash
whoami
```

---

## 8. hostname

Displays the system's hostname.

### Example

```bash
hostname
```

---

## 9. uname

Displays Linux kernel and system information.

### Example

```bash
uname
uname -a
```

---

## 10. Disk Usage

### Check available disk space

```bash
df -h
```

### Check directory size

```bash
du -sh .
```

---

# Key Learnings

- `cp` creates a copy.
- `mv` moves or renames files.
- `head` shows the beginning of a file.
- `tail` shows the end of a file.
- `history` displays previous commands.
- `clear` only clears the terminal screen.
- `whoami` shows the current username.
- `hostname` shows the computer name.
- `uname -a` displays detailed system information.
- `df -h` shows available disk space.
- `du -sh` shows the size of a directory.

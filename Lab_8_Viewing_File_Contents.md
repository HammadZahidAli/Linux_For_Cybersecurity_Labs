
# Lab 8: Viewing File Contents

## 🎯 Objectives

- Familiarize with basic commands for viewing file contents in a Linux terminal.
- Learn how to extract and search for specific text within files.
- Understand the differences and use cases of `head`, `tail`, `more`, and `grep` commands.

---

## 🧠 Prerequisites

- Basic knowledge of using a terminal.
- Access to a Linux-based operating system or terminal emulator.

---

## 🛠️ Lab Tasks

### 📝 Task 1: Viewing the Beginning of a File with `head`

**Objective:** Learn how to display the first 10 lines of a file.

```bash
# Navigate to your target directory
cd /path/to/your/directory

# View the first 10 lines of a file
head filename.txt

# View the first 5 lines of a file
head -n 5 filename.txt
```

📌 *Example:*
```bash
head example.txt
```

---

### 📝 Task 2: Viewing the End of a File with `tail`

**Objective:** Learn to display the last 10 lines of a file.

```bash
# View the last 10 lines of a file
tail filename.txt

# View the last 15 lines of a file
tail -n 15 filename.txt
```

---

### 📝 Task 3: Paging Through a File with `more`

**Objective:** Use `more` to browse through files interactively.

```bash
more filename.txt
```

🔍 *Navigation:*
- `Spacebar`: Scroll down one page
- `Enter`: Scroll down one line
- `q`: Quit the viewer

---

### 📝 Task 4: Searching Text Within a File Using `grep`

**Objective:** Learn to search and filter content using `grep`.

```bash
# Search for a specific string in a file
grep "search-term" filename.txt

# Case-insensitive search
grep -i "search-term" filename.txt

# Recursive search in a directory
grep -r "search-term" /path/to/your/directory
```

📌 *Example:*
```bash
grep "Linux" example.txt
```

---

## ✅ Conclusion

By completing this lab, you’ve gained essential skills for viewing and filtering text in files using:

- `head`
- `tail`
- `more`
- `grep`

These tools are critical for log analysis, monitoring, and information retrieval in Linux — key skills in cybersecurity roles.

---

## 💡 Further Exploration

- Try using `less` for advanced viewing.
- Combine `grep` with `pipe (|)` commands.
- Monitor logs live using `tail -f`.

---

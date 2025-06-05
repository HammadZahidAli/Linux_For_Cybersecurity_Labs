
# Lab 9: Working with Links

## Objectives

- Understand the difference between hard links and symbolic links.  
- Learn how to create hard and symbolic links using command-line tools.  
- Explore and compare the file sizes and inodes of hard and symbolic links.

---

## Prerequisites

- Basic knowledge of navigating and using the Linux command line.  
- Access to a Unix-like operating system (Linux or macOS).  
- Basic understanding of file systems and inodes.

---

## Lab Tasks

### Task 1: Create a Hard Link Using `ln`

1. **Open Your Terminal**  
   Open your terminal on your Unix-like operating system. Ensure you have a working directory:
   ```bash
   mkdir ~/link_lab
   cd ~/link_lab
   ```

2. **Create a Sample File**  
   Create a simple text file named `original.txt`:
   ```bash
   echo "This is the original file." > original.txt
   ```

3. **Create a Hard Link**  
   Use the `ln` command to create a hard link named `hardlink.txt`:
   ```bash
   ln original.txt hardlink.txt
   ```
   > A hard link is a directory entry that associates a name with the file's inode directly.

---

### Task 2: Create a Symbolic Link Using `ln -s`

1. **Create a Symbolic Link**  
   Use the `ln -s` command to create a symbolic (soft) link named `symlink.txt`:
   ```bash
   ln -s original.txt symlink.txt
   ```
   > A symbolic link is a reference that points to another file by path.

---

### Task 3: Compare File Sizes and Inodes

1. **Check File Details**  
   Use the `ls -l` command to view file metadata:
   ```bash
   ls -l
   ```
   - **Hard Links**: Share the same inode number and size as the original file.  
   - **Symbolic Links**: Have a different inode and typically a smaller file size (they store only the path).

2. **Display Inode Numbers**  
   Use the `ls -i` command to view inode numbers:
   ```bash
   ls -i
   ```
   - `original.txt` and `hardlink.txt` will have the same inode number.  
   - `symlink.txt` will have a different inode.

---

## Conclusion

In this lab, you learned how to:

- Create both hard and symbolic links using the `ln` command.  
- Compare and understand the differences between them in terms of inodes and file sizes.

### Key Takeaways

- **Hard Links**: Directly link to the file's inode and can only be created within the same file system.  
- **Symbolic Links**: Reference the file path and can span across different file systems.

This foundational knowledge is essential for system administration, file system management, and software development.

---



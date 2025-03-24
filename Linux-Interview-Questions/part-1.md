

---

```markdown
# 🔗 IQ1]  Difference Between Soft Link and Hard Link in Linux

## 📋 Summary Table

| Feature                     | Soft Link (Symbolic Link)                 | Hard Link                                |
|----------------------------|--------------------------------------------|-------------------------------------------|
| **Command**                | `ln -s source target`                      | `ln source target`                        |
| **Points To**              | File name/path                             | File’s inode (actual data)                |
| **Across Filesystems?**    | Yes                                        | No                                        |
| **Can Link Directories?**  | Yes (requires root, not common)            | No                                        |
| **If Original is Deleted** | Link becomes broken                        | File still works                          |
| **Storage Usage**          | Uses small space for path info             | Shares same inode; no extra space used    |
| **Symbol in `ls -l`**      | Starts with `l` (e.g., `lrwxrwxrwx`)       | Appears as a normal file                  |
| **Common Usage**           | Shortcuts to scripts, configs, resources   | Duplicate reference without extra space   |


## 💻 Example Commands

```bash
# Create a sample file
echo "Linux is awesome!" > original.txt

# Create a symbolic (soft) link
ln -s original.txt softlink.txt

# Create a hard link
ln original.txt hardlink.txt
```

---

## 🧪 Behavior on Deletion

- If `original.txt` is deleted:
  - `softlink.txt` → ❌ Broken (dangling link)
  - `hardlink.txt` → ✅ Still accessible (data is preserved)

---

## 🧠 How to Explain in an Interview

> “A **hard link** is like creating another entry to the same physical data on disk—both names point to the same inode. Deleting the original doesn’t affect the other.
>
> A **soft link**, on the other hand, is a pointer to the file path. If the original file is removed or moved, the link breaks.
>
> I typically use **soft links** for configuration sharing and version switching, while **hard links** help when backups are needed without consuming extra space.”

---

## ✅ Use Cases in Real Projects

- **Soft Links:**
  - Centralized logrotate scripts
  - Shared config files for multiple environments
  - Linking current version in deployments (`/var/www/html -> /var/www/releases/v5.2/`)
  
- **Hard Links:**
  - Backup copies without duplication
  - Package managers to reference the same binaries

---
```

---


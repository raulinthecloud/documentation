# 📦 What is the Partition Entry Array (GPT)?

The **Partition Entry Array** is a critical part of the **GUID Partition Table (GPT)** layout. It contains a list of entries that describe each partition on the disk.

---

## 📚 Summary

Each entry in the array represents a single partition and includes the following information:

- **Partition type GUID** (e.g., EFI System, Linux filesystem)
- **Partition unique GUID**
- **First LBA** (starting block of the partition)
- **Last LBA** (ending block of the partition)
- **Attributes** (bootable, read-only, etc.)
- **Partition name** (label, stored in UTF-16)

---

## 📍 Where is it located?

In a standard GPT disk layout:

| Sector        | Content                              |
|---------------|--------------------------------------|
| 0             | Protective MBR                       |
| 1             | GPT Header                           |
| 2–33          | **Partition Entry Array** (default: 128 entries) |
| Last sector   | Backup GPT Header                    |
| Before last   | Backup Partition Entry Array         |

The **number of entries** and **size of each entry** are specified in the GPT Header (sector 1).

---

## 🧠 Mnemonic

> **"Table with partition details: GUID, start-end, label, attributes — located in sectors 2–33."**

---

## 🛠️ Notes

- Each entry is usually 128 bytes.
- Total size = number of entries × entry size.
- A backup copy of the Partition Entry Array is stored at the end of the disk for redundancy.

# 📘 What is the GPT Header?

The **GPT Header** is the main metadata structure in the GUID Partition Table format, located in **sector 1** of a GPT disk.  
It describes how partitions are defined and where critical structures are located.

---

## 📌 Key Features

| Component           | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| **Location**        | Sector 1 (after the Protective MBR at sector 0)                             |
| **CRC32**           | Checksum for verifying integrity of the header                              |
| **Backup Pointer**  | LBA address pointing to the **exact sector** where the **backup GPT header** is stored (typically the last sector) |
| **Disk GUID**       | Unique ID for identifying the disk                                           |
| **Partition Entry Array LBA** | Start of the partition entries (usually sector 2)                  |
| **Usable LBAs**     | Range of sectors available for user partitions                              |
| **Partition Entry Count** | Number of partitions supported (commonly 128)                         |
| **Partition Entry Size**  | Usually 128 bytes per entry                                           |
| **CRC32 of Partition Array** | Ensures integrity of the partition entries                         |

---

## 🔁 Redundancy

GPT provides a **backup header** at the end of the disk.  
The **Backup Pointer** in the main header points to the **exact sector** of this backup header.

The partition entry array is also duplicated near the backup header — this ensures full recoverability if the primary structures are corrupted.

---

## 🧠 Mnemonic

> **GPT Header (sector 1), CRC32, backup pointer**

This summarizes the three essentials:
- Location (sector 1)
- Integrity check (CRC32)
- Recovery (backup pointer → last sector)

---

## 🧭 Why It Matters

Without the GPT header, a GPT disk becomes unreadable.  
It defines where partitions start and end, ensures consistency, and enables recovery.

---

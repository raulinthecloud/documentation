# 📘 What is LBA (Logical Block Addressing)?

**LBA (Logical Block Addressing)** is a method used to identify and access sectors on a storage device such as a hard drive or SSD.

Instead of using the old CHS (Cylinder-Head-Sector) method, LBA treats the disk as a simple linear list of blocks.

---

## 🧱 How It Works

Each block (also called a sector) is assigned a **unique number**, starting from 0.

| LBA Number | Typical Use (on GPT disks)           |
|------------|---------------------------------------|
| LBA 0      | Protective MBR                        |
| LBA 1      | Primary GPT Header                    |
| LBA 2+     | Partition Entry Array                 |
| LBA N-1    | Backup Partition Entry Array          |
| LBA N      | Backup GPT Header (last sector)       |

- Each block usually holds **512 bytes** or **4096 bytes** of data.

---

## 🎯 Why It's Important

- **Simplifies access** to disk sectors
- **Enables large storage support** (up to several TB or even PB)
- **Required for modern partition systems** like GPT and UEFI

---

## 🆚 LBA vs CHS

| Feature           | LBA                         | CHS (Old Method)             |
|-------------------|-----------------------------|------------------------------|
| Addressing        | Linear block numbers         | Cylinders, Heads, Sectors    |
| Max size          | Very large (up to 9.4 ZB)    | Limited (usually ~8.4 GB)    |
| Simplicity        | Much simpler                 | Complex hardware dependency  |
| Modern usage      | Standard in all modern disks | Obsolete                     |

---

## ✅ Summary

> **LBA** makes disk addressing simple and powerful. It’s how your OS knows where everything is — from boot records to partitions and files.

---

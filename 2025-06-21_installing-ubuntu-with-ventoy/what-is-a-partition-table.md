# Partition Table Overview

A **partition table** is a data structure stored at the beginning of a disk that describes how the disk is divided into **partitions**. Each partition can hold a different file system and serve different purposes (e.g., operating system, data storage, swap).

## Main Partition Table Types

### MBR (Master Boot Record)
- Legacy format, compatible with BIOS.
- Supports up to **4 primary partitions** (or 3 primary + 1 extended).
- Maximum partition size: **2 TB**.
- Located at **sector 0** of the disk.
- Does not support disks larger than 2 TB without tricks.

### GPT (GUID Partition Table)
- Modern format, compatible with UEFI.
- Supports **up to 128 partitions** by default.
- Handles disks **larger than 2 TB**.
- Uses **GUIDs** (Globally Unique Identifiers) for each partition.
- Stores a backup copy of the partition table for recovery.

## What Does a Partition Table Contain?
- Partition type (Linux, Windows, EFI, swap, etc.).
- Start and end sectors of each partition.
- Associated file system (ext4, NTFS, FAT32, etc.).
- Partition name or label (optional).
- Boot flag (for bootable partitions).

## How to View or Modify It?

- **Linux**: `fdisk`, `parted`, `lsblk`, `gdisk`, etc.
- **Windows**: Disk Management, `diskpart`.
- **macOS**: `diskutil`

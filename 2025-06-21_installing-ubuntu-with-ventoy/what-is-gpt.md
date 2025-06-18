# What Is GPT?

**GPT** stands for **GUID Partition Table**. It is a modern partitioning scheme used on hard drives and SSDs, designed to replace the older **MBR (Master Boot Record)** format.

## Key Features of GPT

- **Supports Large Drives**: Can handle disks larger than **2 TB**.
- **More Partitions**: Supports up to **128 partitions** per disk (without extended/logical partitions).
- **Reliable**: Stores **multiple copies** of the partition table (main + backup).
- **GUIDs**: Each partition has a **Globally Unique Identifier**.
- **Required by UEFI**: GPT is the standard for UEFI-based systems.

## GPT vs MBR

| Feature              | MBR                          | GPT                          |
|----------------------|-------------------------------|-------------------------------|
| Max Disk Size        | ~2 TB                         | Over 9 zettabytes (theoretical) |
| Max Partitions       | 4 primary (or 3 + 1 extended) | 128 primary partitions         |
| Partition ID         | 32-bit                        | 128-bit GUID                   |
| Redundancy           | No                            | Yes (primary + backup tables)  |
| Boot Mode Support    | BIOS only                     | UEFI (some support BIOS too)   |

## How GPT Works

- Stores the partition table at **the beginning and end** of the disk.
- Uses a **protective MBR** to prevent legacy tools from misidentifying the disk.
- Each partition has metadata like its GUID, type, size, and name.

## How to Check for GPT

- On Linux: use `lsblk -f`, `parted -l`, or `gdisk`.
- On Windows: use Disk Management or `diskpart → list disk` (a *\** under "GPT" means it is GPT-formatted).

GPT is essential for modern systems, especially those using UEFI, and is more robust and future-proof than MBR.

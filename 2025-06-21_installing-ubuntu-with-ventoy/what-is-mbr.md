# What Is MBR?

**MBR** stands for **Master Boot Record**. It is an older partitioning scheme used on hard drives and SSDs, introduced in 1983. It was the standard for PCs using BIOS firmware for many decades.

## Key Features of MBR

- **Located in Sector 0**: The MBR is stored in the first sector of the disk (512 bytes).
- **Boot Code**: Contains a small piece of code that helps boot the operating system.
- **Partition Table**: Can define up to **4 primary partitions**, or **3 primary + 1 extended** (which can hold logical partitions).
- **Max Disk Size**: Supports drives up to **2 TB** in size.

## MBR vs GPT

| Feature              | MBR                          | GPT                            |
|----------------------|-------------------------------|---------------------------------|
| Max Disk Size        | ~2 TB                         | Over 9 ZB (zettabytes)          |
| Max Partitions       | 4 primary (or 3 + 1 extended) | 128 primary                     |
| Partition Table Size | 64 bytes (4 × 16-byte entries)| Flexible (typically 128 entries)|
| Redundancy           | No                            | Yes (primary + backup)          |
| Boot Mode Support    | BIOS                          | UEFI (can also support BIOS)    |

## Limitations of MBR

- **Size Limit**: Can't handle disks larger than ~2 TB.
- **Partition Limit**: Limited to 4 primary partitions.
- **No Redundancy**: If the MBR is corrupted, the system may fail to boot.

## When to Use MBR

- When compatibility with **legacy BIOS systems** is required.
- On **older operating systems** or **older hardware** that don’t support GPT.
- For disks **smaller than 2 TB** and with fewer than 4 partitions.

MBR is largely being replaced by GPT in modern systems, but is still relevant for compatibility with older hardware and software.

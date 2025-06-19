# 🧮 GPT vs MBR Partition Table Comparison

| Feature                          | GPT (GUID Partition Table)                        | MBR (Master Boot Record)                        |
|----------------------------------|---------------------------------------------------|-------------------------------------------------|
| 📅 Age                           | Modern (since 2001, with UEFI)                    | Old (since 1983)                                |
| 🧬 Partition Identification      | Uses globally unique GUIDs                        | Uses simple partition type codes                |
| 🔢 Max Number of Partitions     | 128 (default)                                     | 4 primary or 3 primary + 1 extended             |
| 💾 Max Disk Size                | Up to 9.4 ZB                                      | Up to 2 TB                                      |
| 🔁 Redundancy                   | Yes (backup table at disk end)                    | No                                              |
| 🔐 Error Checking               | Yes (CRC32 checksum)                              | No                                              |
| 🧩 BIOS Compatibility           | No (requires UEFI)                                | Yes                                             |
| 💻 Required for Modern Windows | Yes (mandatory for Windows 11)                    | Not supported by Windows 11                     |
| 🛠️ Conversion Without Data Loss | Yes (using tools like `mbr2gpt` in Windows 10+)   | Risky, often requires reformatting              |

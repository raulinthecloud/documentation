# 🖥️ UEFI vs Legacy BIOS Comparison

| Feature                          | UEFI (Unified Extensible Firmware Interface)      | Legacy BIOS (CSM)                               |
|----------------------------------|---------------------------------------------------|-------------------------------------------------|
| 📅 Origin Year                   | 2005 (popular after 2012)                         | 1975                                            |
| 📦 Firmware Type                | 32/64-bit in flash memory                         | 16-bit in ROM                                   |
| 💻 Graphical Interface          | Often available                                   | No (text-based only)                            |
| 🚀 Boot Speed                   | Faster                                            | Slower                                          |
| 📁 Partition Compatibility      | GPT (and MBR for backward compatibility)          | Only MBR                                        |
| 🔐 Secure Boot Support          | Yes                                               | No                                              |
| 💾 Large Disk Support           | Yes (up to 9.4 ZB with GPT)                       | No (limited to 2 TB)                            |
| 🔄 Redundancy and Recovery      | Yes (GPT backup + CRC check)                      | No                                              |
| 💽 Modern OS Support            | Required for Windows 11, recommended for Linux    | Limited to older OS versions                    |
| 🧩 Modern Device Support        | Full (NVMe, SSDs, etc.)                           | Partial or none                                 |
| 🧠 Execution Mode               | 32/64-bit                                         | 16-bit                                          |
| 🔁 Legacy BIOS Emulation        | Yes (via CSM)                                     | Native BIOS                                     |
| 🧭 Disk & Driver Management     | Advanced driver support and navigation            | Very limited                                    |

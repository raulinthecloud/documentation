# What Is UEFI?

**UEFI** stands for **Unified Extensible Firmware Interface**. It is the modern replacement for the traditional **BIOS** (Basic Input/Output System) used to initialize and boot computers.

## Key Features of UEFI

- **Graphical Interface**: Unlike BIOS, UEFI supports mouse and graphical menus.
- **Faster Boot Times**: Improved boot and resume speeds.
- **Secure Boot**: Protects the system from unauthorized bootloaders and malware.
- **Supports Large Drives**: Works with drives larger than **2 TB** using the **GPT (GUID Partition Table)** format.
- **Modular and Extensible**: Vendors can add drivers and tools to the firmware environment.

## UEFI vs BIOS

| Feature              | BIOS                       | UEFI                         |
|----------------------|----------------------------|------------------------------|
| Interface            | Text-based                 | Graphical and text           |
| Boot Mode            | Legacy                     | UEFI                         |
| Drive Support        | Up to 2 TB (MBR)           | Over 2 TB (GPT)              |
| Boot Speed           | Slower                     | Faster                       |
| Secure Boot          | Not supported              | Supported                    |
| Architecture         | 16-bit                     | 32-bit or 64-bit             |

## How to Know If You're Using UEFI

- On Linux: run `ls /sys/firmware/efi` – if it exists, you're using UEFI.
- On Windows: open **System Information** → check *BIOS Mode* (it says "UEFI" or "Legacy").

## Related Concepts

- **GPT (GUID Partition Table)**: The partition table format used by UEFI.
- **Secure Boot**: A security feature that verifies bootloaders.
- **CSM (Compatibility Support Module)**: Allows UEFI to boot in BIOS/Legacy mode.

UEFI is now the standard on most modern computers, offering enhanced features, flexibility, and security over traditional BIOS systems.

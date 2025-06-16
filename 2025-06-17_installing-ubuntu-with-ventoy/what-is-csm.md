# 🔁 What is CSM (Compatibility Support Module)?

**CSM** stands for **Compatibility Support Module**. It is a feature of UEFI firmware that emulates the behavior of the traditional BIOS.

### 🔧 Purpose:
- Allows legacy (non-UEFI) operating systems and bootloaders to run on modern UEFI hardware.
- Supports MBR partition tables and 16-bit BIOS calls.

### ⚠️ Important:
- **Disabling CSM** enables full UEFI features like Secure Boot.
- Many modern PCs no longer include CSM for security and compatibility reasons.

Use CSM only when backward compatibility is necessary.

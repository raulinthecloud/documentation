# 🔐 What is Secure Boot?

**Secure Boot** is a security standard developed by members of the **UEFI (Unified Extensible Firmware Interface) Forum**.  
Its main goal is to ensure that only **trusted and digitally signed software** is loaded during the boot process of a computer.

---

## ✅ Purpose

Secure Boot protects your system from:
- 🛑 Rootkits and bootkits
- 🧪 Malicious low-level software (before the OS loads)
- 🚫 Unauthorized operating systems or bootloaders

---

## ⚙️ How it works

1. 🔑 The UEFI firmware stores a list of trusted keys (from Microsoft, Linux distros, or custom vendors).
2. 📄 During startup, UEFI checks the **digital signature** of the bootloader or OS kernel.
3. ✅ If the signature is valid and trusted, the system boots.
4. ❌ If not, the firmware **blocks execution** and displays a security warning.

---

## 📌 Key Concepts

| Concept              | Description                                                                            |
|----------------------|----------------------------------------------------------------------------------------|
| **UEFI**             | Modern firmware interface replacing BIOS                                               |
| **Bootloader**       | First program launched by firmware to load the OS (e.g., GRUB, Windows Boot Manager)   |
| **PK, KEK, DB, DBX** | Public Key (PK), Key Exchange Key (KEK), allowed (DB) and disallowed (DBX) signatures   |

---

## 🖥️ Common scenarios

- 🟢 **Pre-installed Windows systems**: Secure Boot is usually enabled by default.
- 🐧 **Linux distros**: Most modern ones like Ubuntu, Fedora, or Debian support Secure Boot.
- 🛠️ **Dual boot setups**: May require Secure Boot to be disabled or manually signed bootloaders.

---

## 🔓 Can I disable it?

Yes. Most BIOS/UEFI setups allow Secure Boot to be disabled.  
However, doing so **reduces security** and is only recommended for advanced users or testing environments.

---

## 🧠 Why it matters

Secure Boot plays a vital role in:
- Protecting against pre-OS malware
- Enforcing trusted OS integrity
- Complying with security standards (like for Windows 11 requirements)

---

## 🧪 Summary mnemonic

**Secure Boot = UEFI + Signature Check + No Unauthorized Code**


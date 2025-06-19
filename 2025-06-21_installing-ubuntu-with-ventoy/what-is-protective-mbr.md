# 🛡️ What is the Protective MBR?

The **Protective MBR (PMBR)** is a special structure located in **sector 0** of a **GPT-formatted disk**. Its main purpose is to protect GPT disks from being mistakenly modified by legacy tools that only understand the older **MBR (Master Boot Record)** partitioning scheme.

---

## 📌 Key Characteristics

- **Location:** Sector 0 of the disk
- **Partition Type:** `0xEE` (GPT Protective)
- **Partitions:** Declares a single fake partition that spans the entire disk
- **Bootable:** No, it is not used to boot
- **Purpose:** Acts as a warning to old MBR-based tools: "Do not modify this disk!"

---

## 🧠 Why is it needed?

Older operating systems and disk utilities that do not recognize GPT might try to repartition or overwrite the disk. The Protective MBR prevents this by:

- Claiming the entire disk is already in use
- Avoiding accidental data loss from old MBR-based tools

---

## 🧪 Example in `gdisk` or `fdisk`:

```
Partition 1: Protective MBR (type EE)
```

---

## 🧠 Mnemonic Summary

```
2001, Protective MBR, sector 0, type EE, 1 fake part, GPT shield, No boot
```

---

## 🆚 MBR vs GPT (with PMBR)

| Feature          | MBR                    | GPT (+ PMBR)                      |
|------------------|------------------------|-----------------------------------|
| Max partitions   | 4 primary              | 128+                              |
| Max disk size    | 2 TB                   | 9.4 ZB                            |
| Sector 0 usage   | Boot + partition table | Protective MBR + pointer to GPT   |
| Legacy support   | Native                 | Requires fallback via PMBR        |

---

## ✅ Conclusion

The Protective MBR is a **compatibility layer** that ensures older tools do not accidentally damage modern GPT disks. While invisible to modern systems, it plays a vital role in safe coexistence with legacy software.

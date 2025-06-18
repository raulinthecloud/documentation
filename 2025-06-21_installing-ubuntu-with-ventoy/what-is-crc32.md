# ✅ What is CRC32 Checksum?

**CRC32 (Cyclic Redundancy Check 32-bit)** is an error-detecting code used to verify the integrity of data.

### 🧠 How it works:
- A **CRC32 value** is calculated from a block of data.
- When the data is read or transferred, the CRC is recalculated and compared.
- If values differ → **data corruption** is detected.

### 📦 In GPT disks:
- CRC32 checks are used to validate the integrity of the partition table.
- Helps protect against silent disk errors.

It's a lightweight, fast way to maintain data reliability.

# 🆔 What is GUID (Globally Unique Identifier)?

A **GUID** (Globally Unique Identifier) is a 128-bit number used to uniquely identify objects, systems, or partitions. In Linux, a partition's GUID, also known as the UUID (Universally Unique Identifier), can be found in the `/etc/fstab` file.

### 📌 In the context of disks:
- Used in **GPT (GUID Partition Table)** to identify partitions.
- Each partition has a unique GUID, avoiding conflicts across systems.
- Ensures better structure, organization, and interoperability across platforms.

### 🔍 Example:
A GUID might look like:  
`3F2504E0-4F89-11D3-9A0C-0305E82C3301`

GUIDs are critical in modern systems for consistency and uniqueness.

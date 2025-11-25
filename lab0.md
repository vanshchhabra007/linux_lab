
# 🧪 LAB 0 – Ubuntu Installation & System Setup

## 🔰 Objective
Set up a working Linux (Ubuntu) environment to be used for future lab work.

---

## 🖥️ Installation Method Chosen
> **Option A – Virtual Machine (VirtualBox)**
<!-- If you used dual boot, replace the above line -->

---

## 📸 Installation Screenshots

1️⃣ VirtualBox / Disk Partition Setup  
2️⃣ Ubuntu Installation Progress  
3️⃣ First Successful Ubuntu Login

```md
![Setup Screenshot](image1.png)
![Installation Screenshot](image2.png)
![Login Screenshot](image3.png)
````

---

## 🧾 Terminal Command Outputs

After installation, the following commands were executed in Ubuntu terminal:

### 🔹 Ubuntu Version

```bash
lsb_release -a

```

### 🔹 Kernel Information

```bash
uname -a

```

### 🔹 Disk Usage

```bash
df -h

```

### 🔹 Memory Usage

```bash
free -m

```

---

## ✨ Reflection

> Write 5–6 lines about the installation experience.

  Example:

```
The installation process was new for me, but interesting. Initially, I faced issues with allocating enough RAM and enabling virtualization from BIOS. Once configured, the Ubuntu installation completed smoothly. Installing guest additions improved display resolution and performance. This lab helped me understand basic Linux installation and system configuration.
```

---

## 💡 Extra Questions

### ✔ What are two advantages of installing Ubuntu in VirtualBox?

| Advantage                  | Description                                                                      |
| -------------------------- | -------------------------------------------------------------------------------- |
| 🔹 Safe & non-destructive  | No risk to existing OS or files — everything is inside a virtual environment.    |
| 🔹 Snapshots & portability | You can take snapshots and revert anytime; the VM can be moved to other systems. |

### ✔ What are two advantages of dual booting instead of using a VM?

| Advantage                    | Description                                                                         |
| ---------------------------- | ----------------------------------------------------------------------------------- |
| 🔹 Full hardware performance | Ubuntu gets full access to RAM, CPU, GPU — great for heavy workloads & development. |
| 🔹 No resource sharing       | The OS runs natively, so no slowdown from virtualization overhead.                  |

---

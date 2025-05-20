# 🐧 Linux Guide: Things To Do After Installation

## 1️⃣ Install Linux Headers
To ensure kernel modules and drivers work correctly (especially for VirtualBox):

```bash
sudo apt update && sudo apt upgrade
sudo apt install linux-headers-generic
sudo apt install linux-headers-$(uname -r)
```

---

## 2️⃣ Install VirtualBox Guest Additions
This boosts performance by enabling features like 3D acceleration and better integration.

### Steps:
1. In VirtualBox menu, choose **Insert Guest Additions CD Image**.
2. Once mounted, open the file manager — you’ll see a CD icon in the sidebar.
3. Open the CD folder, copy all files, and paste them into your **Documents** folder.
4. Open the Terminal (`Ctrl + Alt + T`).
5. Navigate to the Documents folder:
   ```bash
   cd Documents
   ```
6. List the files to make sure it's there:
   ```bash
   ls
   ```
7. Make the installer executable:
   ```bash
   sudo chmod 777 VBoxLinuxAdditions.run
   ```
8. Run the installer:
   ```bash
   sudo ./VBoxLinuxAdditions.run
   ```
9. Finally, reboot the VM:
   ```bash
   reboot
   ```

# **Mavira OS**
A custom Debian-based Linux distribution focused on **simplicity**, **performance**, and **security**.  
Built using the Debian **live-build** system, Mavira OS includes a complete **XFCE desktop**, LightDM login manager, system hardening, custom utilities, and a polished out-of-the-box desktop experience.

---

## **✨ Features**
- Lightweight and fast **XFCE Desktop Environment**
- **LightDM** display manager with autologin support
- Fully set up **Xorg** graphical stack
- Custom **hooks**, **post-install scripts**, and **branding**
- **Fail2Ban**, **AppArmor**, audit rules & security configs
- Ready for **VirtualBox**, **QEMU**, and bare-metal installation
- Pre-configured user environment with custom tools

---

## **📦 Included Components**
- **XFCE4**, xfce4-goodies  
- **xorg** & video drivers  
- **LightDM** + GTK greeter  
- **NetworkManager**  
- Custom `/usr/local/bin` tools  
- GRUB/isolinux bootloader assets  
- System hardening modules  

---

## **🛠️ How to Build the ISO**
Run from project root:

sudo ./build/create_workspace.sh
sudo ./build/build_iso.sh

---

## **▶️ How to Boot in QEMU**
qemu-system-x86_64
-m 2048
-cdrom images/mavira-os-amd64.iso
-boot d
-vga virtio
-accel tcg



---

## **▶️ How to Boot in VirtualBox**
Recommended settings:

- **Chipset:** PIIX3  
- **Graphics Controller:** VMSVGA  
- **Video Memory:** 128 MB  
- **Enable 3D Acceleration**  
- **Storage:** Attach ISO as Optical Drive  
- **Pointing Device:** USB Tablet  

---

## **🐞 Troubleshooting**
### **Stuck on CLI / No GUI**
If desktop does not start, login and run:

sudo systemctl restart lightdm


If GUI packages were not installed during build, add them to:

kali-config/variant-mavira/package-lists/mavira.list.chroot

and rebuild the ISO.

---

## **📜 License**
This project is open-source.  
Feel free to modify, redistribute, or rebuild your own custom distribution on top of Mavira OS.

---

## **💬 Credits**
Developed by **Animesh Sharma**, with guidance and support from the open-source community.

---

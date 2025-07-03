# 🖧 Basic Switch Configuration with Cisco Packet Tracer

This repository contains two Packet Tracer (.pka) files demonstrating **basic switch configuration** in small LAN environments.

---

## 📂 Files Included

- `2-PC-1-Switch.pka`  
  > A simple topology with **2 PCs** connected to **1 switch**.  
  > Ideal for learning initial switch setup, port configuration, and basic connectivity testing.

- `4-PC-1-Switch.pka`  
  > A slightly larger setup with **4 PCs** connected to **1 switch**.  
  > Good for practicing port labeling, VLAN basics, and switch security practices.

---

## 🎯 Objectives

These activities cover the following foundational switch configuration tasks:

- Assigning a **hostname** to the switch
- Setting up a **management IP address** on the VLAN 1 interface
- **Securing access** with console and password protection
- **Saving configurations** to prevent loss on reboot
- Testing **end-to-end connectivity** using the `ping` command

---

## ⚙️ Configuration Steps (Common to Both Files)

> Open `.pka` files in **Cisco Packet Tracer**, and access the CLI of the switch.

### 1. Set a Hostname
```bash
Switch> enable
Switch# configure terminal
Switch(config)# hostname Switch_A
```

### 2. Configure VLAN 1 Interface
```bash
Switch_A(config)# interface vlan 1
Switch_A(config-if)# ip address 192.168.1.1 255.255.255.0
Switch_A(config-if)# no shutdown
Switch_A(config-if)# exit
```

### 3. Set Console Access Password
```bash
Switch_A(config)# line console 0
Switch_A(config-line)# password cisco
Switch_A(config-line)# login
Switch_A(config-line)# exit
```

### 4. Set Enable Password
```bash
Switch_A(config)# enable password class
```

### 5. Save the Configuration
```bash
Switch_A# write memory
```

---

## ✅ Verification

- Use `ping` from one PC to another to test connectivity
- Use the `show running-config` command to verify switch settings
- Check LED lights and cable types in **Physical Mode** if desired

---

## 📝 Notes

- These activities are great practice for beginners in CCNA or anyone new to configuring Cisco switches.
- Default VLAN 1 is used for simplicity. For production setups, creating and assigning custom VLANs is recommended.

---

## 📎 Requirements

- Cisco Packet Tracer (version 7.x or higher recommended)
- Basic understanding of CLI and network addressing

---

## 📚 Learning Resources

- [Cisco Networking Academy](https://www.netacad.com)
- [Packet Tracer CLI Cheatsheet (Cisco Docs)](https://learningnetwork.cisco.com/s/article/packet-tracer-cli-commands)

---

🛠️ *Feel free to clone this repo and modify the .pka files for your own practice!*

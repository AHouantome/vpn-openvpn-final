# 🛡️ VPN Setup Using OpenVPN

This project demonstrates how to set up a secure VPN using OpenVPN on Ubuntu. It includes certificate-based authentication, IP forwarding, and packaging client configuration — all documented with screenshots.

## 🔧 Tools & Technologies
- Ubuntu Linux
- OpenVPN
- easy-rsa
- systemd

---

## 📋 Key Steps (with Screenshots)

### 1. OpenVPN Installation
```bash
sudo apt install openvpn easy-rsa
```
![Install OpenVPN](01_collection_of_files.png)

### 2. Generate Certificates and Keys
```bash
./easyrsa init-pki
./easyrsa build-ca
```
![Generate CA](07_generate_keys_1.png)

### 3. Configure the VPN Server
```bash
sudo nano /etc/openvpn/server.conf
```
![Edit Config](05_edit_server_conf.png)

### 4. Enable IP Forwarding
```bash
sudo nano /etc/sysctl.conf
```
![Enable Forwarding](06_enable_ip_forwarding.png)

### 5. Start the VPN Server
```bash
sudo systemctl start openvpn@server
sudo systemctl enable openvpn@server
```
![Start VPN](11_start_vpn_server.png)

### 6. Package and Zip Client Files
![Zip Files](16_zip_client_files.png)

---

## 💡 What I Learned

- VPN setup using Linux CLI
- Certificate-based authentication with easy-rsa
- How to troubleshoot server configuration issues

## 📂 Files Included

- README.md
- 16 screenshots (.png)

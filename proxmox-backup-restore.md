# Proxmox Backup restore

1. Download Proxmox VE 6.4-1:
```
wget https://www.proxmox.com/images/download/pve/iso/proxmox-ve_6.4-1.iso
```

2. Install Proxmox in the VirtualBox.
   
3. Chande `sshd_config` file in the Proxmox CLI:
```
nano /etc/ssh/sshd_config
```
- escape the # symbol before the `Port 22` line
- escape the # symbol before the `ListenAddress 0.0.0.0`
- set the `PermitRootLogin` option to `yes`

This is necessary so that you can upload the dump file via FileZilla (or other file manager) to Proxmox storage.

4. Unzip dump file:
- Install zstd (optional)
```
sudo apt-get install zstd
```
- Unzip file
```
unzstd vzdump-qemu-101-2023_10_29-07_44_58.vma.zst
```

5.

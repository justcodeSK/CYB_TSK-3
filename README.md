# Task 3 - Vulnerability Scan on My PC

## Tool Used
- Nessus Essentials (or OpenVAS)
- VM (Kali Linux 2025.1c)

## Scan Target
- Localhost : inet 192.168.56.103

## Scan Type
- Full vulnerability scan

## Configuration & Installation
- Used Kali Linux OS is much better than using a windows OS Enviornment.
- Used command line interface to update Packages and tools in Linux (In root/administrator command)  and setup openvas.
  - `apt-get install openvas` \\No need to use sudo if alredy in root/administrator command.
  - `gvm-setup` \\Saved the UDID and Password.
- Now checked all setup wen't well.
  - `gvm-check-setup`
-Before starting the gvm we need to look all `gvmd data`, `SCAP data`, `Certificates data`
 - `sudo greenbone-feed-sync --type NVT
sudo greenbone-feed-sync --type SCAP
sudo greenbone-feed-sync --type GVMD_DATA
`
- Now Start GVM(Greenbone Vulnerablity Mananger-Frame work of tools used for VUlnerablity Manangement).
  - `gvm-start`
  - `gvm-stop`

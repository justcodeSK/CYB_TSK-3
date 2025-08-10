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
 - `greenbone-feed-sync --type GVMD_DATA
greenbone-feed-sync --type SCAP
greenbone-feed-sync --type NVT
greenbone-feed-sync --type CERT
`
- Now Start GVM(Greenbone Vulnerablity Mananger-Frame work of tools used for VUlnerablity Manangement).
  - `gvm-start`
  - `gvm-stop`
  
## Issues Faced
- The configuration and Installation was simple to learn, the issue faced in OpenVAS was with the Feed data, it keeps on not updating in the WebUI (NVT, SCAP etc).
- Key Solutions learned Checked the postgress database of gvm.
- Tried multiple attempts like restarting gvm, reinstalling the gvm in new virtual box Guest-OS(Kali), Altering the database to work with GUI, Creating new DB and new gvm user.
- Re-installed the sync data multiple times to update the feed.
- Hence the data base does has the data and its not yet able to update to web ui.
- Still searching on for furrther solutions.
- Screen short of issue faced `task_delayed.png`

## Reference and Learned
- References used : https://www.youtube.com/watch?v=ZJcEWx9mlng , https://www.youtube.com/watch?v=LGh2SetiKaY , https://www.youtube.com/watch?v=0CZBN9DnDCg
- Couldint perform a vulnerablity scan even after multiple tries and But i make it the most of it by learning much from youtube and how an actual vulnerablity scan should have worked.

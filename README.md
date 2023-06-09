## Architecture ##

Network:
The network cis made up of two machines: a MacOs (host) and a Kali Linux virtual machine running on VMWare.
Both machines are connected through a local area network (LAN).

Hosts:
Host Machine (MacOs):
IP Address: [*]
Operating System: macOS

Virtual Machine (Kali Linux):
IP Address: [*]
Operating System: Kali Linux

## Implementation ##

Automated Backup:
The automated backup script is executed on the host machine (MacOs).
Backups are stored locally on the host machine in the directory defined by the "backup_location" variable.
Backups are then transferred to a remote server (Kali Linux) using the rsync protocol.

## Best Practices ##

Secure Connections: Ensure that SSH connections between the host machine and the virtual machine are secure by using SSH keys and not passwords.

## Required Configurations ##

System (Host Machine - MacOs):

Ensure that the macOS operating system is up to date.
Install the required dependencies for the backup script, such as rsync and tar.

Network:

Configure network settings of the the host machine and remote server to allow SSH connections.

Services:

Ensure that the SSH service is enabled and configured on both the host machine and remote servert to allow remote connections.

## How to ##

Backup a new folder:
Add the absolute path of the folder to the backup script in the "repository" variable.
Execute the backup script by selecting the "Perform Backup" option (1) in the menu.
The backup will be created locally in the directory specified by the "backup_location" variable and transferred to the remote server.

Restore Backup:
Select the "List Backups" option in the menu to display the available backups on the virtual machine (Kali Linux).
Identify the backup file corresponding to the previous date you want to restore.
Execute the "Restore Backup" option in the menu.
Enter the name of the backup file to restore when prompted.
The backup will be transferred from the virtual machine to the host machine and restored in the directory specified by the "backup_location" variable.
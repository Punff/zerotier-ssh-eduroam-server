# Setting Up Debian on an IBM Thinkpad T43 for Remote Access and Backups

## Introduction
In this project, I transformed an old 'IBM Thinkpad T43' into a minimal Debian server affectionately named "junkyard" to serve as a remote access point and backup solution. The setup involved configuring SSH, firewall settings, ZeroTier network, and automated backups using rsync.

## Process

### 1. Installation and Stripping Down
I started by installing Debian on the IBM Thinkpad T43, aiming for a minimal setup to optimize performance. Stripping down unnecessary components helped keep the system lightweight.
Additionally I setup TLP which significantly reduced the CPU load when idle.

### 2. Setting Up SSH and Firewall
To enable remote access, I configured SSH on junkyard. Additionally, firewall settings were adjusted to ensure the necessary ports were open for SSH connections.

### 3. ZeroTier Network Setup
Since direct access to junkyard was limited by the Eduroam network, I turned to ZeroTier. By setting up a ZeroTier network and connecting junkyard and my personal laptop, I enabled remote access. Initially, access was restricted to devices on the same network.

### 4. Routing Between Networks
To overcome the limitation of accessing junkyard from different networks, I followed guidance from the [ZeroTier documentation](https://zerotier.atlassian.net/wiki/spaces/SD/pages/224395274/Route+between+ZeroTier+and+Physical+Networks). This involved setting up routing between the ZeroTier and physical networks. With this configuration, I could access junkyard from my laptop on various networks, such as my network back home (unfortunatley excluding the Eduroam network at my University as it restricts SSH connections).

### 5. Multiple Users
I integrated my roommate's external SSD into the setup by connecting it to junkyard. After partitioning the SSD, I created a user account for my roommate and added his laptop to the ZeroTier network. This enabled my roommate to access his user account remotely, stored on his SSD.

### 6. Use Cases
Currently serving as a backup for personal files with an automated 'rsync' script I wrote.
An additional use case in the works is a family photo web gallery hosted locally where access is restriced to devices on the network

# Setting Up Debian on an IBM Thinkpad T43 for Remote Access and Backups

## Introduction
In this project, I transformed an old IBM Thinkpad T43 into a minimal Debian server named "junkyard" to serve as a remote access point and backup solution. The setup involved configuring SSH, firewall settings, ZeroTier network, and automated backups using rsync.

## Steps

### 1. Installation and Stripping Down
- Installed Debian on IBM Thinkpad T43.
- Stripped down the installation to make it minimal.

### 2. Setting Up SSH and Firewall
- Configured SSH on "junkyard" for remote access.
- Implemented firewall settings to forward necessary ports for SSH.

### 3. ZeroTier Network Setup
- Eduroam network limitations necessitated a ZeroTier network setup.
- Connected "junkyard" and personal laptop via ZeroTier network for remote access.
- Initial access was restricted to the current network.

### 4. Routing Between Networks
- Followed instructions from [ZeroTier documentation](https://zerotier.atlassian.net/wiki/spaces/SD/pages/224395274/Route+between+ZeroTier+and+Physical+Networks) to route between ZeroTier and physical networks.
- Enabled access to "junkyard" from personal laptop on different networks (e.g., home network).

### 5. External SSD Integration
- Plugged in roommate's external SSD to "junkyard".
- Partitioned the SSD and set up a user account for roommate.
- Added roommate's laptop to the ZeroTier network for remote access to their user account on "junkyard".

### 6. Automated Backups
- Set up an automated backup script using rsync on "junkyard".
- Currently, "junkyard" serves as a backup solution.

## Future Projects
- Planning to collaborate on additional projects with roommate utilizing "junkyard" as a base.

## Conclusion
The project successfully transformed an old IBM Thinkpad T43 into a useful Debian server, providing remote access and backup solutions via SSH, ZeroTier network, and automated backups.

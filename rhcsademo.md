```markdown
# RHEL System Administration Tasks

## [Manage Networking]
Configure network and set the static parameters.

**Parameters:**
- IP-ADDRESS = 172.25.250.10
- NETMASK = 255.255.255.0
- GATEWAY = 172.25.250.254
- Nameserver = 172.24.254.254
- Hostname = servera.lab.example.com

## [Installing and Updating Software Packages]
Configure your system to use these locations as default repositories:

**Repositories:**
- `http://content.example.com/rhel9.0/x86_64/rhcsa-practice/rht`
- `http://content.example.com/rhel9.0/x86_64/rhcsa-practice/errata`

## [Managing Local Users and Groups]
Create the following users, groups and group memberships:

**Requirements:**
- A group named `sharegrp`
- User `harry` who belongs to `sharegrp` as a secondary group
- User `natasha` who also belongs to `sharegrp` as a secondary group
- User `copper` who:
  - Does not have access to an interactive shell on the system
  - Is not a member of `sharegrp`
- All users (`harry`, `natasha`, `copper`) should have password `redhat`

## [Controlling Access to Files]
Create collaborative directory `/var/shares` with the following characteristics:

**Requirements:**
- Group ownership of `/var/shares` should be `sharegrp`
- The directory should be readable, writable and accessible to members of `sharegrp` but not to any other user
- Files created in `/var/shares` automatically have group ownership set to the `sharegrp` group

## [Accessing Linux File Systems] - Task 1
Find all lines in the file `/usr/share/mime/packages/freedesktop.org.xml` that contain the string `ich`.

**Requirements:**
- Put a copy of these lines in the original order in the file `/root/lines`
- `/root/lines` should contain no empty lines
- All lines must be exact copies of the original lines

## [Accessing Linux File Systems] - Task 2
1. Find all the files owned by user `natasha` and redirect the output to `/tmp/output`
2. Find all files that are larger than 5MiB in the `/etc` directory and:
   - Copy them to `/find/largedir`
   - Redirect the output to `/find/largefiles`

## [Managing Local Users and Groups] - Additional Task
Create a user `fred` with:
- User ID: 3945
- Password: `iamredhatman`

## [Managing Files from the Command Line]
Search the string `nologin` in the `/etc/passwd` file and save the output in `/root/strings`

## [Configuring NTP/Time Synchronization]
Configure your system so that it is an NTP client of `classroom.example.com`

## [Scheduling Future Tasks]
User `natasha` must configure a cron job that:
- Runs daily at 14:23 local time
- Executes: `/bin/echo hello`

## [Archiving and Transferring Files & SELinux]
Create a backup file named `/root/backup.tar.bz2` or `/root/backup.tar.gz2`

**Requirements:**
- The backup file should contain the content of `/usr/local`
- Should be zipped with bzip2 or gzip2 compression format
- Ensure SELinux is in enforcing mode (change if not)

## [Create a Bash Script]
Create a script file named `find.sh` that when executed will:
- Find all files from 30K to 60K file size from the directory `/etc`
- Copy those files to `/root/data` directory

## [Managing SELinux Security]
Your webcontent has been configured in port 82 at the `/var/www/html` directory.

**Requirements:**
- Make the content accessible
- Do not alter or remove any files in this directory

## [Set the Password expire date]
The password for all new users in `servera.lab.example.com` should expire after 30 days.

## [Autofs Configuration]
Configure autofs to automount the home directories of user `remoteuser15`.

**Specifications:**
- NFS Server: `utility.lab.example.com` (172.24.10.10)
- NFS Export: `/netdir` to your system
- User: `remoteuser15`
- Home directory: `utility.lab.example.com:/netdir/remoteuser15`
- Local mount point: `/netdir/remoteuser15` (beneath `/netdir`)
- Home directories must be writable by their users
- Only `remoteuser15` home directory is accessible from your system

---

## [Question for second node serverb]

### Add a Swap partition
Add an additional swap partition of 512 MiB to your system.

**Requirements:**
- The swap partition should automatically mount when your system boots
- Do not remove or otherwise alter any existing swap partition on your system

### [Create a logical volume]
Create a new logical volume according to the following requirements:

**Specifications:**
- Logical volume name: `database`
- Volume group: `datastore`
- Size: 50 extents
- Extent size: 16 MiB
- Filesystem: vfat
- Mount point: `/mnt/database` (automatically mounted at system boot time)

### [LVM partition resize]
Resize LVM partition to approximately 850MB.

**Requirements:**
- LV name: `database`
- Partition size must be within approximately 830MB to 865MB
- Partition must be usable

### [TUNING SYSTEM PERFORMANCE]
Change the current tuning profile for serverb to default profile

### [UMASK Configure]
Set permission for user `daffy` to get the following permissions when creating new files or directories:
- Files: `-rw-------`
- Directories: `drwx-------`

### [SUDO Configuration]
Configure sudo permissions for users who are members of the `admin` group, allowing them to use sudo without a password.

---

## [Container Questions]

### Questions 01:
Create a container image named `monitor` from a Containerfile from below link:
- URL: `http://fromwebserver/Containerfile`
- **Note:** All tasks must be done using `student` user

### Questions 02:
Create rootless container and:
- Do volume mapping as specified in the question
- Run container as a service from normal user account
- The service must be enabled to start automatically after reboot
```

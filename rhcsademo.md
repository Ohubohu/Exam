

                                          [Manage Networking]
Configure network and set the static parameters. Consider machine configured as DHCP, need to config it with static
parameters.

IP-ADDRESS= 172.25.250.10
NETMASK= 255.255.255.0
GATEWAY= 172.25.250.254
Nameserver= 172.24.254.254
Hostname= servera.lab.example.com



                            [Installing and Updating Software Packages]
    •   Configure your system to use this location as a default repository (public/local repo):
    •   http://content.example.com/rhel9.0/x86_64/rhcsa-practice/rht
    •   http://content.example.com/rhel9.0/x86_64/rhcsa-practice/errata


                                  [Managing Local Users and Groups]
Create the following users, groups and group memberships:
    •   A group named sharegrp
    •   A user harry who belongs to sharegrp as a secondary group
    •   A user natasha who also belongs to sharegrp as a secondary group
    •   A user copper who does not have access to an interactive shell on the system and who is not a member
        of sharegrp.
    •   harry, natasha and copper should have the password redhat



                                        [Controlling Access to Files]
Create collaborative directory /var/shares with the following characteristics:
    •   Group ownership of /var/shares should be sharegrp.
    •   The directory should be readable, writable and accessible to member of sharegrp but not to any other user. (It is
        understood that root has access to all files and directories on the system)
    •   Files created in /var/shares automatically have group ownership set to the sharegrp group.

                                       [Accessing Linux File Systems]
Find all lines in the file /usr/share/mime/packages/freedesktop.org.xml that contain the string ich.
Put a copy of these lines in the original order in the file /root/lines.
/root/lines should contain no empty lines and all lines must be exact copies of the original lines in
/usr/share/mime/packages/freedesktop.org.xml




                                       [Accessing Linux File Systems]
Find all the files owned by user natasha and redirect the output to /tmp/output.
Find all files that are larger than 5MiB in the /etc directory and copy them to /find/largedir and redirect the output
to /find/largefiles



                                  [Managing Local Users and Groups]
Create a user fred with a user ID 3945. Give the password as iamredhatman



                              [Managing Files from the Command Line]
Search the string nologin in the /etc/passwd file and save the output in /root/strings


                               [Configuring NTP/Time Synchronization]
Configure your system so that it is an NTP client of classroom.example.com



                                          [Scheduling Future Tasks]
The user natasha must configure a cron job that runs daily at 14:23 local and execute: /bin/echo hello


                            [Archiving and Transferring Files & SELinux]
Create a backup file named /root/backup.tar.bz2 or /root/backup.tar.gz2. The backup file should contain the content
of /usr/local and should be zipped with bzip2 or gzip2 compression format.
Furthermore, ensure SELinux is in enforcing mode. If it is not, change SELinux to enforcing mode.


                                          [Create a Bash Script]


Questions: Create a script file name find.sh. when you run this script, it will find all files from 30K to 60k file
size from the directory /etc directory & copies those files to /root/data directory.



                                       [Managing SELinux Security]

Your webcontent has been configured in port 82 at the /var/www/html directory (Don't alter or remove any files in
this directory). Make the content accessible.


                                      [Set the Password expire date]
The password for all new users in servera.lab.example.com should expires after 30 days.


                                          [Autofs Configuration]
          Configure autofs to automount the home directories of user remoteuser15. Note the following:
     •    utility.lab.example.com (172.24.10.10), NFS-exports /netdir to your system, where
          user is remoteuser15
     •    remoteuser15’s home directory is utility.lab.example.com:/netdir/remoteuser15
     •    remoteuser15’s home directory should be auto mounted locally beneath /netdir as
          /netdir/remoteuser15
     •    Home directories must be writable by their users while you are able to login as any of
          the remoteuser15 only home directory that is accessible from your system


                                    [Question for second node serverb]

Add a Swap partition
---------------------------------

Add an additional swap partition of 512 MiB to your system. The swap partition should automatically mount when
your system boots. Do not remove or otherwise alter any existing swap partition on your system.


                                         [Create a logical volume]
Create a new logical volume according to the following requirements:
 - The logical volume is named database and belongs to the datastore volume group and has a size of 50 extents.
 - Logical volume in the datastore volume group should have an extent size of 16 MiB.
 - Format the new logical volume with vfat filesystem. The logical volume should be mounted automatically
   mounted under /mnt/database at system boot time.


                                            [LVM partition resize]
LVM partition resize re-size LVM partition 850MB. Where LV name is database. Partition size
must be within approximately 830MB to 865MB and usable.



                                   [TUNING SYSTEM PERFORMANCE]

Change the current tuning profile for serverb to default profile



                                            UMASK Configure
Questions: Set permission for user daffy. User will get the permission below for file & directory when he creates new
files or directory.
-rw-------
drwx-------


                                          SUDO Configuration
Question: Configure sudo permissions for users who are members of the admin group, allowing them to use sudo
without a password.


                                         Container Questions
Questions 01: Create a container image named monitor from a Containerfile from below link
http://fromwebserver/Containerfile . All this task done using student user.


Questions 02: Create rootless container and do volume mapping which they asked you in the question and run container
as a service from normal user account, the service must be enable so it could start automatically after reboot.

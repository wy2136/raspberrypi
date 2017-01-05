# Mount External Disk

### Guide

Install necessary packages

    sudo apt-get install hfsplus hfsutils hfsprogs

Create a folder for mounting

    sudo mkdir /media/mydrive

Add a line to the <code>/etc/fstab</code> file

    sudo vi /etc/fstab
    # /dev/sda2    /media/mydrive    hfsplus defaults,force,gid=pi,uid=pi,noatime    0    0
    
Change the owner and permission 
    
    sudo chown -R root:users /media/mydrive/
    sudo chmod -R ug=rwx,o=rx /media/mydrive/

### Trouble shooting

In case the mounted file system becomes read-only, try the following command before mounting 
(from: https://adityalaghate.in/mount-hfsplus.html)

    sudo umount /media/mydrive
    fsck.hfsplus -f /dev/sdaX
    sudo mount -a

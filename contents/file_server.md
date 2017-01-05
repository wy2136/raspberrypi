# File Server: Samba

### Guide

    sudo apt-get install samba samba-common-bin
    sudo vi /etc/samba/smb.conf
    # read only = no
    # security = user
    #
    # [mydrive]
    #   comment = external hard drive on raspberry pi
    #   path = /media/mydrive
    #   valid users = @users
    #   force group = users
    #   create mask = 0775
    #   directory mask = 0775
    #   read only = no
    #   browseable = yes

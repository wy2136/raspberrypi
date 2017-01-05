# MiniDlna

### Guide

    sudo apt-get install minidlna
    sudo vi /etc/minidlna.conf
    # media_dir=/media/mydrive
    sudo service minidlna force-reload
    
To rebuild Media_DB forcibly:

    sudo minidlnad -R

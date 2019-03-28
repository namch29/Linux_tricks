1. No sound in ubuntu server: 
      sudo apt-get remove --purge alsa-base
      sudo apt-get remove --purge pulseaudio 
      sudo apt-get install alsa-base
      sudo apt-get install pulseaudio 
      sudo alsa force-reload
      sudo apt-get install pavucontrol
      reboot
      
 2. Change username:
        sudo passwd root
    Login as root account
    Change the username and the home folder to the new name that you want.
        usermod -l <newname> -d /home/<newname> -m <oldname>
    Change the group name to the new name that you want.
        groupmod -n <newgroup> <oldgroup>
    Lock the "root" account.
        passwd -l root
    If you were using ecryptfs (encrypted home directory). Mount your encrypted directory using 
        ecryptfs-recover-private 
    and edit <mountpoint>/.ecryptfs/Private.mnt to reflect your new home directory.
      
 3. https://linuxize.com/post/how-to-change-hostname-on-ubuntu-18-04/
 
 4. Using universe repository:
        sudo add-apt-repository universe
        
 5. Apps after install Ubuntu server:
      xinit openbox obconf obmenu obkey terminator thunar thunar-archive-plugin nitrogen lxappearance 
      
      Cursor:
            sudo add-apt-repository ppa:dyatlov-igor/la-capitaine
            sudo apt update
            sudo apt install la-capitaine-cursor-theme
      Autostart:
            compton&
            plank&
            nitrogen --restore&
      Time:
            dpkg-reconfigure tzdata

6. DPKG is locked:
      ps aux | grep -i apt
      sudo kill -9 <PID>
      sudo killall apt apt-get

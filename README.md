# Linux_tricks
1. No sound in ubuntu server: 
sudo apt-get remove --purge alsa-base   
sudo apt-get remove --purge pulseaudio
sudo apt-get install alsa-base  
sudo apt-get install pulseaudio
sudo alsa force-reload

=====================================================
2. Change name of user:

    
Log in using your username and password.

    
Set a password for the "root" account:    
              sudo passwd root
    
Log out. exit
    
Log in using the "root" account and the password you have previously set. Change the username and the home folder to the new name that you want.
           usermod -l <newname> -d /home/<newname> -m <oldname>

    
Change the group name to the new name that you want.              
	        groupmod -n <newgroup> <oldgroup>
    
Lock the "root" account.
              passwd -l root

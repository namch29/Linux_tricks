# Linux_tricks
1. No sound in ubuntu server
sudo apt-get remove --purge alsa-base   
sudo apt-get remove --purge pulseaudio
sudo apt-get install alsa-base  
sudo apt-get install pulseaudio
sudo alsa force-reload

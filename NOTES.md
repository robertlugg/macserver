# hostname
mmserver
10.0.0.135

# ufw firewall
sudo apt update
sudo apt install ufw
sudo ufw enable

# ssh
sudo apt update -y
sudo apt install -y openssh-server
sudo ufw allow ssh

# Aptitude package manager.
Needed to resolve issue with conflict of libjpeg62-dev
sudo apt-get install aptitude
sudo aptitude install libjpeg62-dev
# Guacomole
sudo apt install -y libcairo2-dev libjpeg-turbo8-dev libjpeg62-dev libpng12-dev libtool-bin uuid-dev 
sudo apt install -y libavcodec-dev, libavformat-dev, libavutil-dev, libswsccale-dev
sudo apt install -y freerdp2-dev libpango1.0-dev libssh2-1-dev libtelnet-dev libvncserver-dev libwebsockets-dev libpulse-dev
# Home Assistant

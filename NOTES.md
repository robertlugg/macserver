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
- Needed to resolve issue with conflict of libjpeg62-dev
sudo apt-get install aptitude

# Guacomole
## Perhaps best install guide
https://computingforgeeks.com/install-and-use-guacamole-on-ubuntu/

## Get dependencies
sudo aptitude install -y libcairo2-dev libjpeg-turbo8-dev libjpeg62-dev libpng-dev libtool-bin uuid-dev
sudo aptitude install -y libavcodec-dev libavformat-dev libavutil-dev libswscale-dev
sudo aptitude install -y freerdp2-dev libpango1.0-dev libssh2-1-dev libtelnet-dev libvncserver-dev libwebsockets-dev libpulse-dev
sudo aptitude install -y libssl-dev libvorbis-dev libwebp-dev
## Now, build
git clone git://github.com/apache/guacamole-server.git
wget https://apache.org/dyn/closer.lua/guacamole/1.4.0/source/guacamole-server-1.4.0.tar.gz?action=download -o guacamole-server-1.4.0.tar.gz
tar xzf guacamole-server-1.4.0.tar.gz
cd guac*
CFLAGS=-Wno-error ./configure --with-init-dir=/etc/init.d
make
sudo make install
sudo ldconfig
sudo systemctl daemon-reload
sudo systemctl start guacd
sudo systemctl enable guacd

# Home Assistant

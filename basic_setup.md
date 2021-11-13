
### very first steps ###

`adduser daniel` - create user

`usermod -aG sudo daniel` - add user to sudo group (for sudo priveledges) 

`deluser pi` - remove the default user

`systemctl enable ssh` enable ssh for startup

`nano /etc/sysctl.conf` add `vm.swappiness = 10` add bottom



### some more apps to install ###

`apt install aptitude`

`apt install lm-sensors`

#### docker ####

`curl -fsSL https://get.docker.com -o get-docker.sh`

`sh get-docker.sh`

`adduser lunar` - create non sudo user

`usermod -aG docker lunar`

`apt install python3 python3-pip`

`pip install docker-compose`





#### docker compose: unifi ####

watch for ports to open, they are slow, can watch with nmap for them to open

attach with `<ip>:8080`

when adopting, make sure to put <ip> into controller/controller host IP (no port), check box for override inform host with controller IP

restart docker  
  

1) add ssh config
2) ufw
3) 


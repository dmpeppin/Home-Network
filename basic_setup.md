
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

/home/lunar/configs/*

/home/lunar/docker-compose/*/dockercompose.yaml






#### docker compose: pihole ###

- run attached the first time to obtain the password
- set upstream dns to ** 1.1.1.1 **
- dont worry about local dns for now
- not sure what dns setting in docker compose are for...


1) factory reset devices
2) load unifi controller onto machine
3) adopt devices
4) set ssh password
5) ssh into all devices
6) create new VLAN for controller machine
7) activate new VLAN on port for controller machine
8) log into controller after new VLAN and IP are applied
9) check "override inform" ???
10) use `set-inform http://10.0.10.10:8080/inform` on all devices to set new controller location


# Reduce card writes #

add to `./etc-pihole/pihole-FTL.conf`

```
# Items older than x days will be deleted from log
MAXDBDAYS=30
# Write to DB every x minutes
DBINTERVAL=720`
```



#### docker compose: unifi ####

watch for ports to open, they are slow, can watch with nmap for them to open

attach with `<ip>:8080`

when adopting, make sure to put <ip> into controller/controller host IP (no port), check box for override inform host with controller IP

restart docker  
  

1) add ssh config
2) ufw
3) 



### very first steps ###

`adduser daniel`

`usermod -aG sudo daniel`

`deluser pi`

`systemctl enable ssh`

`nano /etc/sysctl.conf` add `vm.swappiness = 10` to bottom, reduces swap usage

`apt install lm-sensors` - temperature monitor

1) add ssh config
2) ufw
3) 




#### docker ####

`curl -fsSL https://get.docker.com -o get-docker.sh`

`sh get-docker.sh`

`adduser lunar` - create non sudo user  to run docker

`usermod -aG docker lunar`

`apt install python3 python3-pip` - python repository for docker compose

`pip install docker-compose`

/home/lunar/configs/*

/home/lunar/docker-compose/*/dockercompose.yaml

`docker-compose up -d` `docker-compose down`




#### pihole setup ####

- run attached the first time to obtain the password
- set upstream dns to ** 1.1.1.1 **
- dont worry about local dns for now
- not sure what dns setting in docker compose are for...

#### unifi setup ####

1) factory reset devices
2) load unifi controller onto machine
3) adopt devices 
4) set ssh password
5) ssh into all devices...
6) create new VLAN network to be used by controller machine
7) activate new VLAN on physical port for controller machine
8) log into controller after new VLAN and IP are applied
9) check "override inform" ???
10) ssh `set-inform http://10.0.10.10:8080/inform` on all devices to set new controller location


### Reduce card writes ###

add to `./etc-pihole/pihole-FTL.conf`

```
# Items older than x days will be deleted from log
MAXDBDAYS=30
# Write to DB every x minutes
DBINTERVAL=720`
```



1) add ssh config
2) ufw
3) 


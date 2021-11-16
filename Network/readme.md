## Networks ##

- #### Name	Subnet	VLAN DNS ####
- Infrastructure	10.0.10.0/24	10
- Servers	10.0.20.0/24	20
- Endpoints Daniel  10.0.30.0/24	30		
- Endpoints Maggie	10.0.31.0/24	31		
- IoT	10.0.50.0/24	50

Set Infrastructure, Servers, Endpoints Daniel, IoT with "DHCP Name Server" Manual "10.0.10.10" for pihole

Set Maggie to "DHCP Name Server" Manual "1.1.1.1" to allow ads



## Static IP ##

- Main PC	10.0.30.10
- Main Server	10.0.20.10
- Main Laptop 10.0.30.30
- PiHole, Unifi	10.0.10.10
- Home Assistant	10.0.50.10


## Access Points ##

- "Lunar"	IoT (50)	2.4GHz
- "Otter" Endpoints Daniel (5GHz)



## Firewalls ##



## USG Configs ##

- Set inform host to controller IP. 
- After changing controller IP, on each device, ssh in and run `set-inform http://<new ip>:8080/inform` to find new controller location
- Set Wifi channels

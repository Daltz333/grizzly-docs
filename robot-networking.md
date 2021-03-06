# Robot Networking
FRC Robots can be networked various ways. The most common way is through the usage of what's called [DHCP (Dynamic Host Configuration Protocol)](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol). In simple terms, DCHP auto assigns IP addresses to devices connected to the DHCP server. Another means of handling networking is via Static IP Addresses. 

- Dynamic Host Configuration Protocl (IP Addresses *can* change)
- Static IP Configuration (IP Addresses are fixed, conflicts can occur)

A handy picture diagram of DHCP can be found [here](https://i.imgur.com/AJRAdoP.jpg).

#### What We Use
Grizzly Robotics static IPs our robots. We do this for a variety of reasons.
- Static IPed robots don't need to wait for a DHCP server to assign it an IP, therefore connecting faster.
- Static IPed robot components can connect to each other faster, as it does not need to resolve [domain names](https://www.cloudflare.com/learning/dns/what-is-dns/).

#### Our Setup
The Grizzly Robotics standard setup includes:
- [Raspberry Pi3](https://www.raspberrypi.org/products/raspberry-pi-3-model-b/) (for vision and camera streaming)
- [Ethernet Switch](https://www.amazon.com/NETGEAR-Ethernet-Unmanaged-Protection-GS105NA/dp/B0000BVYT3) (for more ethernet ports)
- [FRC legal radio](https://www.andymark.com/products/open-mesh-om5p-ac-dual-band-1-17-gbps-access-point-radio)
- [FRC RoboRIO](https://www.andymark.com/products/ni-roborio)
- Driverstation Laptop

![](https://i.imgur.com/4hL0m4W.png)

### Static IP Configuration
#### For Driverstations:
- Static IP of: 10.0.66.5
- Subnet of: 255.0.0.0
- Every other field should be blank

#### For everything else (including RoboRIO):
- Static IP of: 10.0.66.X (X being a non-conflicting number between 2 and 20)
- Subnet of: 255.255.255.0
- Gateway of (if needed otherwise keep blank): 0.0.0.0
- DNS Server of (if needed otherwise keep blank): 0.0.0.0

### Pro Tips!
- To static IP the RoboRIO you must plug in via USB and navigate to 172.22.11.2 in your web browser

### Example Images
![](https://i.imgur.com/vZMF5EM.png)
![](https://i.imgur.com/tAcHjFY.png)
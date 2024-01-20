---
layout: post
title: "Home Network (Project)"
date: 2024-01-04 23:11 +0000
categories: learning networking
---

## Table of Contents

- [Overview](#overview)
- [Initial Research](#initial-research)
    - [Access point research](#access-point-research)
    - [Camera research](#camera-research)
    - [Chat GPT storage amount](#chat-gpt-storage-amount)
    - [Do I need a Unifi gateway?](#do-i-need-a-unifi-gateway)
- [Further Research](#further-research)
    - [Placing an order](#placing-an-order)
    - [Power Requiremnents](#power-requirements)
    - [PoE Switch vs PoE Injector](#poe-switch-vs-poe-injector)
- [Further Research pt2](#further-research-pt2)
    - [2.4Ghz vs 5Ghz](#24ghz-vs-5ghz)
    - [What is MIMO](#what-is-mimo)
    - [PoE switch options](#poe-switch-options)
- [Conclusion from Research](#conclusion-from-research)
    - [Setting up the Unifi-Controller](#setting-up-the-unifi-controller)
    - [Is a security gateway needed?](#is-a-security-gateway-needed)
    - [Purchases](#purchases)
    - [Fixing WiFiman](#fixing-wifiman)
    - [Test results from Dan's room](#test-results-from-dans-room)
- [Configuration from Unifi-Controller](#configuration-from-unifi-controller)



<br>

## Overview
The Wi-Fi in our house is currently bad when not close to the router. We have multiple networks setup within the house as we have a router which has direct connections to 3 rooms in the house and then to a seperate mesh network. The mesh network is then scattered around the house and creates it's own seperate network. This means we have 2x SSID's and there is conflict in the house between the networks. In the furthest parts of the house the internet signal is poor. I've tried to setup an AP on one side but the AP signals kept dropping (I think the AP is at fault).

The idea of this research is to allow for a new network to be setup using only Ubiquti kit where possible or at least Ubiquti AP's as they're supposed to be good and easy to manager / nice to manage with the Unifi-controller giving a good idea on what's going on on the network and displaying things in a user friendly way (showing the topology of the network, nice UI etc).

<br><br>

### Initial Research
04/01/24 | 21:45 | 23:37
<br><br>

### Access point research

[YouTube: 2022 Complete Unifi Setup Guide](https://www.youtube.com/watch?v=kGBFkIzf6x0)

This would have been more useful as a guide after all kit arrives. Not worth watching the research stage
<br><br>

[YouTube: Is Ubiquiti UniFi Worth It? \| New Network Setup](https://www.youtube.com/watch?v=cwc9GgFs_gE)

I like Peter but he has no idea what he is doing with network stuff. He was sent loads of kit so not a good reference point
<br><br>

[YouTube: Which is the Best AP for You? - UniFi Access Points Explained 2022](https://www.youtube.com/watch?v=y5I_WhnviYY)

Essentially the U6 Lite should be fine for home. Anything else is kinda overkill by the sounds of it. Mileage may vary depending on your house size
<br><br>

[Stackoverflow: How to use escaped pipe in markdown](https://stackoverflow.com/questions/17319940/how-to-escape-a-pipe-char-in-a-code-statement-in-a-markdown-table)

You can escape a pipe in markdown using a backslash 
<br><br>

### Camera research

[YouTube: Unifi Protect G5 bullet review](https://www.youtube.com/watch?v=BbmrdY2lA5k)

The g4 bullet is better than G5 as it's higher res / looks better at night. There is a comparison on the video
<br><br>

### Chat GPT storage amount

**Chat with GPT** <br>
I then wondered how much storage will be needed to store 1 months worth of footage for 2x G4 cameras which are recording in 2k for a month straight. I asked GPT this and the following is a link to the chat. [link to ChatGPT](https://chat.openai.com/share/b955b46b-bae4-4b3d-984e-a2b84a373c51)

**Summary of chat** <br>
1GB of storage per day so ~30GB per month. This is not very much if you're planning on deleting the footage when not needed. Using a dream machine would be overkill for this if you're not requiring other features it offers.
<br><br>

[Reddit: Do I need a Unifi gateway?](https://www.reddit.com/r/UNIFI/comments/15rgxt3/do_i_need_a_unifi_gateway/)

### Do I need a Unifi gateway?

Essentially the gateway is for pretty dashboard / for inbuilt storage. Not sure there is much other reason to use it. Someone suggested usign a RaspberryPi as a cloud key using something called [UnifiPi](https://unifipi.com/)

Further research needed here
<br><br>


### Further Research
05/01/24 | 19:46 | 23:35 | 10 min break
<br><br>

[YouTube: Unifi Home Network Upgrade - Why I finally switched](https://www.youtube.com/watch?v=wi_geRfabAs)

He spoke about the fact that you could use [linuxserver/unifi-controller](https://hub.docker.com/r/linuxserver/unifi-controller) and run a docker image which you use to run the Unifi-controller.

Checked reddit about this and found [Docker Vs. Raspberry Pi for Controller?](https://www.reddit.com/r/Ubiquiti/comments/xwhtka/docker_vs_raspberry_pi_for_controller/). In the initial statement the user said about hosting the docker image on a synology NAS. Someone in the comments posted a link to [Self-host the Unifi Controller on a Synology NAS](https://www.wundertech.net/self-host-the-unifi-controller-on-a-synology-nas/).

I'm thinking that I may not need a CloudKey and could save 200 if I do decide to get cameras. Either way I think I'll order the access points then go from there. Something important to note is that the **firmware should be updated** if kit is bought as this can prevent issues right away.
<br>

[Reddit: I understand why people don’t like Ubiquiti now](https://www.reddit.com/r/Ubiquiti/comments/udvz31/i_understand_why_people_dont_like_ubiquiti_now/)

I checked Reddit for reasons not to buy the kit before making the purchase and found the following post. This was a small business complaining about multiple cameras. Someone educated replied and essentially said that Ubiquti is fine but maybe not for his use case / they need to spend more than what that are. This makes me think that it should be ok to order the access points.
<br><br>

### Placing an order

Order placed for 3x U6+ Access Points. From here we can then see if anything is else is required and can also tune the equipment on arrival. I was going to order 2 however 3 should be fine as if 2 is enough for the house, one can go in the garage.

[U6+ Product Page](https://uk.store.ui.com/uk/en/products/u6-plus)

I've placed an order but cancelled it as I was supposed to add a switch to the order using guidance from this reddit post [Cancelling order](https://www.reddit.com/r/Ubiquiti/comments/m5s0bx/cancelling_order/). Now I'm reading deeper into it, it sounds like the U6+ actually has some issues anyway. I thought it was the same AP as the U6 Lite which it's not.

[U6+ vs U6-Lite oddities](https://www.reddit.com/r/Ubiquiti/comments/16d0yi4/u6_vs_u6lite_oddities/)

Read this article which says about RAM differences between the U6+ U6 Lite and there is mention of the Pro too. Sounds like it goes U6+ then U6 Lite and then the U6 Pro in terms of how much RAM each has.

Someone also said in another article about there being issues with 2.4Ghz and saying that the AP's perform way better on 5Ghz. I'm struggling to find any more info about this and cannot find the post I read it on.

Trying to understand how PoE works at the moment so that whatever AP's I get I don't have to run cables to. This would neaten things up a little. Just read through [Recommended hardware to meet Unifi POE requirements?](https://www.reddit.com/r/Ubiquiti/comments/13srj0d/recommended_hardware_to_meet_unifi_poe/) and am going to read through
<br><br>

### Power Requirements

The [Flex Mini](https://uk.store.ui.com/uk/en/pro/category/all-switching/products/usw-flex-mini) requires **2.5W** per unit and I'm planning on getting **2** units which would be a total of **5W**

The [U6+](https://uk.store.ui.com/uk/en/products/u6-plus) requires **9W** per unit and I'm planning on getting **3** units which would be a total of **27W**

Overall Total: **32W**

<br>

### PoE Switch vs PoE Injector

[POE switch vs injectors for 2-3 APs?](https://www.reddit.com/r/Ubiquiti/comments/ir1r1u/poe_switch_vs_injectors_for_23_aps/) 

I read through this but didn't understand the logic or what was being said.

[I bought a house with 3 Unifi access points installed throughout the house but I have no idea what I need to use them.](https://www.reddit.com/r/HomeNetworking/comments/kqkhup/i_bought_a_house_with_3_unifi_access_points/)

People just talk about whether it's worth getting switches or PoE. Nothing of use here

[How To Setup a UniFi Access Point WITHOUT A CONTROLLER! (QuickTip)](https://www.youtube.com/watch?v=SOY5Dcu9dwg)

Video on how to setup an AP with the app 

[Cheap POE Gigabit Switch 8 Ports?]()

I finally found what I was looking for. Someone on this post added the following photo:

[Reddit](https://www.reddit.com/r/HomeNetworking/comments/s3oyea/cheap_poe_gigabit_switch_8_ports/)

When searching for cheap PoE switches someone suggested what I was looking for, an 8 port PoE switch. 4 of the ports are PoE and the other 4 are not. It has an overall max power of 64W which would be fine for my usage as I only need 32W as calculated earlier. This would allow for an additional 32W with the remaining 1 port so maybe this could be used to beam Wi-Fi to the garage.

<br>

![8-port-amazon-switch](/img/Screenshot 2024-01-05 at 23.09.47.png)

[Switch suggested](https://www.amazon.com/TP-Link-TL-SG108PE-Shielded-Lifetime-Protection/dp/B01BW0AD1W/?th=1)

On the same [Reddit](https://www.reddit.com/r/HomeNetworking/comments/s3oyea/cheap_poe_gigabit_switch_8_ports/) post there was some information regarding security cameras / NVR's

![VLAN-DVR-advice](/img/Screenshot 2024-01-05 at 23.29.15.png)

[Chat GPT link](https://chat.openai.com/share/c2721371-04a1-4077-9682-901431bbcbe9)

### Further research pt2
09/01/24 | 20:44 | 22:55

Watched a tutorial on how to setup Unifi Protect so that the footage is streamed to the Synology camera system [Adding Cameras to Synology from Unifi](https://www.youtube.com/watch?v=AJYEy093Cdo)


I then looked up whether it's worth getting a UDM Pro or the UDM SE and found [Dream Machine Pro vs SE?](https://www.reddit.com/r/Ubiquiti/comments/uj20p7/dream_machine_pro_vs_se/). As the UDMP SE also has the PoE ports people say that this is a better option.

Checked some comparisons [U6+ v U6 lite](https://www.reddit.com/r/Ubiquiti/comments/16sh8zc/u6_v_u6_lite/) and [U6+ vs U6 lite](https://www.reddit.com/r/Ubiquiti/comments/14ipulk/u6_vs_u6_lite/). There is some mention of the U6 Pro which sounds to be the most reliable. It sounds like the benefit of the U6+ is that it has stronger connection but uses more RAM. I think I saw mention of the U6+ having less RAM than the U6 Lite in another post. There was also mention that the U6+ had WiFi 6 on the 2.4Ghz band which the U6 Lite doesn't.

I then saw this post where a Network technician says to get the U6 Pro. I'm feeling like the U6 Pro is the most solid option and will be the most reliable [Upgrading my setup: Looking for input on the U6 Plus vs. U6 Lite (currently sold out)](https://www.reddit.com/r/Ubiquiti/comments/14mnvu3/upgrading_my_setup_looking_for_input_on_the_u6/)

Watched this video twice after reading a reddit post about the U7 Pro [U7-Pro is HERE! Testing UniFi's First Wi-Fi 7 Access Point](https://www.youtube.com/watch?v=7JNXghzzaZc)

### 2.4Ghz vs 5Ghz

Read the following post [Wifi 6 and 2.4Ghz question](https://www.reddit.com/r/HomeNetworking/comments/106iduw/wifi_6_and_24ghz_question/)

I started to read about signals to work out whether I'd benefit from the U6 Pro's 4x4 Mimo > the U7 Pro's 6Ghz. I found out that 2.4Ghz has more range but is generally a slower connection. This can be used for IoT devices as they're on older hardware and don't need quick speeds. Newer devices like phones are better connected on a 5Ghz network but the range may suffer slightly.

This means that I would need to setup 2x VLAN's, 1 which is a 2.4Ghz network for IoT devies, another which is 5Ghz for mobiles / laptops etc. This further clarifies that the U6 Pro is likely the best option but I will research this further.

### What is MIMO

[✅ How Much Faster Is 4x4 vs 2x2 MIMO External Antenna On T-Mobile 5G Home Internet? - FAQ #2](https://www.youtube.com/watch?v=ix3iKr7ZAbA)

It feels like the best option is the U6 Pro due to reliability and that it's got 4x4 MIMO. The U7 Pro has Ghz but it seems like that is more if you have gigabit internet speeds which we don't therefore it doesn't seem worth the extra £20. The price difference is £152.40 or £171.60

### PoE switch options

The vast majority for people say that it's not worth using injectors. The reason for this is that they cause inconsistencies in the network and can create failures which are hard to troubleshooting and can break kit if they fail - overall not worth.

I then went back to research PoE switches and saw the return of the TP-Link switch. I looked up the difference between a TP-Link switch vs a Ubiquti one to see what I'd be missing if I swapped between kit.

You may lose the ability to turn off AP's remotely and also you may lose the ability to create VLAN's with non-Ubiuti kit. These are 2 things which I plan on doing therfore I think it makes sense to get a Ubiuti switch.

It doesn't currently make sense to get a Dream Machine due to having no cameras but does make sense to get an 8 port switch like this [Lite 8 PoE](https://uk.store.ui.com/uk/en/pro/category/all-switching/products/.usw-lite-8-poe) as an in the middle step.

I found this guide which spoke about whether it's worth getting a  [Unifi switch or not?](https://www.reddit.com/r/Ubiquiti/comments/171btbv/unifi_switch_or_not/)

>Amiga07800 . 3 mo. ago <br>
>The 16 ports has a VERY low PoE budget than won’t be enough for you. You have some other options:
>1. Swap UDM Pro for the SE - 95W PoE on 8 ports - and eventually add a non PoE UniFi switch
>2. Use TWO USW-Lite-8-PoE, 104W PoE budget,” 
>
>Beside, I REALLY suggest to swap the U6+ for the U6-Pro, they are vastly superior (and have a Qualcomm chipset)

This guy suggested the U6 Pro's which I think are the better option now and also suggested either the 8 port switch or a UDM SE.

### Conclusion from research
I don't much more research is required here. I Will do some final checks tomorrow but I think this should all now be ok to order. I will setup search alerts on eBay over the coming weeks to try to get some money off of the AP's as they sell for £135 instead of £154. Also I might be able to pickup the 8 port switch from a 3rd party site without paying the £10 delivery fee which Ubiquti charge.

In regards to setting up a Unifi Controller I will run this on my laptop and will think about a solution for this long term. I have a couple of cheap Raspberry Pi's so maybe able to use one of these to turn the docker image as self-hosted controller to keep it up 24/7.

The plan is to setup 3x networks. 5Ghz networks for phones, this will be our primary network for laptops/tablets/mobiles. Another 2.4Ghz network which will be used for IoT devices. An additional guest network. I think Ubiquti has an easy setup option for this but I'll likely refer back to the video at the top of this article and then also fine some other information on ideal network setups.

I will add more sections to this as I configure the network and also after buying kit to put the price I paid for everything

### 

13/01/24 

15:54 start?

### Are Unifi switches needed?

[Home Network Tour with UniFi Dream Router](https://www.youtube.com/watch?v=PyDpLJIKg0M)

The reason you would want to use Ubiquiti switches is so that you can put them on seperate VLAN's and manage the ports inidivually from the Unifi Controller page

### Setting up the Unifi-Controller

[UI Site Manager](https://unifi.ui.com/)

[Self Hosted UniFi Network Application Controller Install Tutorial](https://www.youtube.com/watch?v=lkUhWnDPutg)

He shows how to self host the Unifi app on a uBuntu image and provides the code

### Is a security gateway needed?

[UniFi Controller: How to Set Up a Simple Ubiquiti UniFi Network](https://www.youtube.com/watch?v=PAuteE-Jr9E)

This was good at it summarised what is needed for a basic Ubiquti network

[2021 Complete Unifi Setup Guide](https://www.youtube.com/watch?v=xhmJxYllnWg)

This video shows that 


[I'm getting rid of my Unifi Dream Router…](https://www.youtube.com/watch?v=YSFo-DfmucM)

He speaks about the differences between the UDM (Ubiquti Dream Machine) and the UDM SE (Ubiquiti Dream Machine Special Eddition)

He says the only differnces are:
1. The UDM has 6 less PoE ports
2. The UDM doesn't support the really high speeds (multiple Gbs)
3. The UDM only has 128 + SD storage for cameras

18:24 end

22:14 start

[Best Ubiquiti router for a setup like mine](https://www.reddit.com/r/Ubiquiti/comments/13e84s1/best_ubiquiti_router_for_a_setup_like_mine/)

everyone says to get the UDM SE, not sure what other options there are?

It's hard to work out what routers exist within the Unifi line and if one is even needed to use the full functionality of the Unifi offering.


Spoke to my Dad this evening to let him know that it's hard to proceed any further given that depending on the camera requirements this will dictate what networking equipment to go. If we're definitley going to get cameras then it makes most sense to get a UDM SE to avoid buying switches seperate to the NVR which will be needed to store the footage from the cameras. Also it will work out cheaper than getting all individual parts and will also make for a cleaner setup overall as it's basically an all in one setup


start unknown
14/01/24

alex ISP setup



11:52 end


start 17:34

network port

patched it into a wall socket with Dad

we use option X out of either the A or B options

18:15


start 21:00

### Purchases

10/01/24

U6-pro
£117
ebay

13/01/24

U6-pro
£129.99
ebay

16/01/24

USW-flex-mini
£29.29
ebay

19/01/24
start 18:56

Tried to download the Unifi-controller from [Self-Hosting a UniFi Network Server](https://help.ui.com/hc/en-us/articles/360012282453-Self-Hosting-a-UniFi-Network-Server#:~:text=Start%20the%20newly%20installed%20UniFi,Adopt%20your%20first%20UniFi%20device.)

19:36 - managed to finally adopt the device after mutliple resets of the device. Had to plug it directly into the router rather than into the wall port in the kitchen.

end 19:37 gym session

start 20:53

Managed to connect to the AP

You have to create a new network from within the Unifi Controller

Wifiman is not working when viewing the signal strength of floor plan pages on my phone within the app

downloaded wifiman on my macbook, it still is not doing signal strength and floor plan

unboxed the 8 port poe switch

If I'm unable to use the PoE from the switch I can always use the PoE injector which came with one of the AP's that I bought

Found this video [Unifi Gigabit Managed Switch Lite 8 PoE](https://www.youtube.com/watch?v=lWM0KnAQ8gA) where he says that if you plug your laptop/desktop into the switch you can adopt it that way

The switch then updated itself after I tried to Adopt it

Adoption failed

Found a guide which says about using SSH to connect to the switch

[Why does my UniFi hardware tell me "Adoption failed"? (3 Solutions!!)](https://www.youtube.com/watch?v=WHdyKfuouDI)

Guice on how to setup SSH keys

[UniFi - Adding SSH Keys to UniFi Devices](https://help.ui.com/hc/en-us/articles/235247068-UniFi-Adding-SSH-Keys-to-UniFi-Devices)

Found this guide regarding connecting to the switch via SSH

[Unifi Switch CLI Commands](https://www.youtube.com/watch?v=H68f4HZMGH8)

The above was a little technical and also vague in regards to resolving failed adoption issues

[Different ways to adopt unifi devices](https://www.youtube.com/watch?v=4p96fPY-8RY)

This guys is really good and broke things down. Installed LAN Scan from the appstore to view devices on my network

When scanning I could not find the device even though it was plugged into my laptop via a port replicator

Tried to plug it into the router again, it then said getting ready and adopted

### Fixing WiFiman

I need to read this when researching "Ubiquiti WiFiman"

[I’ve turned on WiFiMan support and I’m connected to a UniFi Network, any ideas why Signal Mapper is grayed out/how to fix this?](https://www.reddit.com/r/Ubiquiti/comments/v3p33c/ive_turned_on_wifiman_support_and_im_connected_to/)

### Test results from Dan's room

Tested the WiFi in Dan's room with the AP under the router

SSID: Test
Download: 56.02 Mbps
Upload: 17.38 Mbps

SSID: Beaufoys
Download: 7.26 Mbps
Upload: 6.03 Mbps

SSID: TALKTALK
latency error


### UDM vs UDR

[UniFi Dream Machine vs UniFi Dream Router \| which is the right router for you?](https://www.youtube.com/watch?v=nML_kqFpRSQ)

You can only use Unifi networking stuff and cannot run protect as well when using the UDM therefore it is not fit for purpose

[UDR Fail or Success?](https://www.youtube.com/watch?v=E6K2nITRdeA)

He had issues which were resolved with a software update



## Configuration from Unifi-Controller

[Unifi Network Optimization](https://www.youtube.com/watch?v=NCnRhYGMzvA)


end 00:17
start 11:15

Last night setup

Router -> 8 port PoE switch -> AP (Router)
                            -> AP (Kitchen)

Connected some devices up too, all work. The speeds are no better in the lounge for some reason (they were pretty much maxed anyway)

When looking at the client list there are some random devices which were only showing their MAC addresses with no additioanl information

I tried to kick these off then network but they rejoined. I've checked my apple watch and it was connected therefore it must have been shared by my phone / macbook

changed the SSID then the switch was stuck offline

end 12:30

start 15:33

noted down mac addresses for connected devices and gave them friendly name

going to later set it up so that they auto connect to the network

end 15:45

start 19:16

I just went and bought a G3 Flex camera for £35 which I found on facebook marketplace. I've just plugged into the PoE switch but just remered you cannot self host Unifi Protect therfore need to wait until the UDR arrives before I'm able to adpot it.

The next thing to buy will be either a UDM SE to replace the UDR or to get a CloudKey Gen 2 if we choose to have more cameras / the UDR does not have enough storage or RAM.

### Unblocking a device

I found out how to unblock a device. The device will appear in the offline section when going to the "Client Devices" option from the left hand sidebar then choosing offline from the top navigation bar.

The blocked devices will appear with a red dot next to them.

![unblocking-device-new-GUI-1](/img/network-research/unblocking%20a%20device%201.png)

![unblock-device-new-GUI-2](/img/network-research/unblock%20a%20device%202.png)
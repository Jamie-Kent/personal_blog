---
layout: post
title: "Home Network (Project)"
date: 2024-01-04 23:11 +0000
categories: learning networking
---

<a name="readme-top"></a>

<ul>
    <li><a href="#overview">Overview</a></li>
    <li>
    <a href="#unifi-network-research">Unifi Network Research</a></li>
        <ul>
        <li><a href="#typical-setups">Typical Setups</a></li>
        <li>Is it worth it / why switch</li>
        <li>Best AP</li>
    <li><a href="#u6">U6+</a></li>
            <ul>
                <li><a href="#order">Order</a></li>
                <li><a href="#u6-product-page">U6+ Product Page</a></li>
                <li><a href="#vlan-for-cameras">U6+ vs vs U6 Lite</a></li>
                <li><a href="#vlan-for-cameras">Power reqirements</a></li>
            <ul>
            <ul>
            <li><a href="#order">Order</a></li>
            <li><a href="#u6-product-page">Powering devices via PoE</a></li>
            <li><a href="#vlan-for-cameras">How to work out power requirements</a></li>
            <li><a href="#vlan-for-cameras">Alternative power sources</a></li>
            
        </ul>
        
    </ul>
    <li>Unifi gateways - is it required</li>
   
</ul>
<li><a href="#unifi-protect-research">Unifi Protect Research</a></li>
        <ul>
            <li><a href="#vlan-for-cameras">VLAN for cameras</a></li>
            <li><a href="#vlan-for-cameras">G5 Bullet review</a></li>
            <li><a href="#vlan-for-cameras">Storage requirements</a></li>
            <li><a href="#vlan-for-cameras">Streaming to Synology NAS</a></li>
        </ul>
    </ul>
</ul>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  
</details>


<br>



## Overview
The Wi-Fi in our house is currently bad when not close to the router. We have multiple networks setup within the house as we have a router which has direct connections to 3 rooms in the house and then to a seperate mesh network. The mesh network is then scattered around the house and creates it's own seperate network. This means we have 2x SSID's and there is conflict in the house between the networks. In the furthest parts of the house the internet signal is poor. I've tried to setup an AP on one side but the AP signals kept dropping (I think the AP is at fault).

The idea of this research is to allow for a new network to be setup using only Ubiquti kit where possible or at least Ubiquti AP's as they're supposed to be good and easy to manager / nice to manage with the Unifi-controller giving a good idea on what's going on on the network and displaying things in a user friendly way (showing the topology of the network, nice UI etc).

<p align="right">(<a href="#readme-top">back to top</a>)</p>


## Unifi Network Research

<h3 id="typical-setups">Typical Setups</h3>

[YouTube: 2022 Complete Unifi Setup Guide](https://www.youtube.com/watch?v=kGBFkIzf6x0)

The first part of this video is useful to familiarize yourself with what kit would be needed for a typical network. The second half can be used to configure your network once you have all hardware setup.

**Hardware used:** <br>
- Unifi Cloud Gateway:
    - UDM SE (UDM-SE)
- Switch:
    - Unifi Flex Mini 5-Port (USW-Flex-Mini)
- Access Points:
    - U6 Lite (U6-Lite)
    - U6 Pro (U6-Pro)
- Cameras:
    - G3 Flex (UVC-G3-FLEX)
    - G3 Instant (UVC-G3-INS)

**UDM SE** <br>
Roles:
- Unifi Console
- Unifi Controller
- Router
- Inbuilt switch

UDM SE vs UDM Pro:
- Integrated 8-port PoE/PoE+ switch vs no PoE
    - (6) PoE
    - (2) PoE+
- 128 GB SSD for Unifi Protect recordings vs no SSD
- 2.5 GbE RJ45 WAN ports vs 1Gbps on Pro


<br><br>

access points

[YouTube: Which is the Best AP for You? - UniFi Access Points Explained 2022](https://www.youtube.com/watch?v=y5I_WhnviYY)

The U6 Lite should be fine for general house usage, there are other options available but these are likely to be overkill.

### Do I need a Unifi gateway?

[Reddit: Do I need a Unifi gateway?](https://www.reddit.com/r/UNIFI/comments/15rgxt3/do_i_need_a_unifi_gateway/)

**What is a gateway** <br>
The USG Ubiquiti UniFi Security Gateway, is an enterprise Gateway router with Gigabit Ethernet that combines advanced security features with high performance routing technology.

**Function:** <br>
- Routing
- Security

Typical usage: <br>
ISP Modem -> USG -> Switch

Any of the [UniFi Cloud Gateways](https://uk.store.ui.com/uk/en) will do the same thing as the USG I believe.

**What is a Unifi Console?** <br>
From what I've read, the console is the device which sits between the modem and the switch. This is a physical piece of hardware which hosts the Unifi-Controller as well as providing other function.

Example of Unifi consoles: <br>
- [UniFi Cloud Gateways](https://uk.store.ui.com/uk/en)

<br>

**What is a Unifi-Controller** <br>
This is a network management software which can be either self-hosted or runs by default on Unifi Consoles. These are usually referred to as [UniFi Cloud Gateways](https://uk.store.ui.com/uk/en).

Running the device 24/7 will allow for:
- Setting up configuraitons
- Ability to check the status of devices

Self-hosting:
- [UnifiPi](https://unifipi.com/)

Further research needed here
<br><br>


### Are Unifi switches needed?

[Home Network Tour with UniFi Dream Router](https://www.youtube.com/watch?v=PyDpLJIKg0M)

The reason you would want to use Ubiquiti switches is so that you can put them on seperate VLAN's and manage the ports inidivually from the Unifi Controller page

### Setting up the Unifi-Controller

[UI Site Manager](https://unifi.ui.com/)

[Self Hosted UniFi Network Application Controller Install Tutorial](https://www.youtube.com/watch?v=lkUhWnDPutg)

He shows how to self host the Unifi app on a Ubuntu image and provides the code

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

<br>

**Research pt5** <br>
| start 22:14 | end

- Researched the best Unifi router
- Found that the UDR could be an option
- Encountered roadblock which affects ordering kit

<br>

[Best Ubiquiti router for a setup like mine](https://www.reddit.com/r/Ubiquiti/comments/13e84s1/best_ubiquiti_router_for_a_setup_like_mine/)

**Other Unifi cloud console options** <br>
It's hard to work out what routers exist within the Unifi line and if one is even needed to use the full functionality of the Unifi offering. Everyone says that the UDM SE is the best option which makes sense but with minimal info on what cameras are needed it doesn't make sense for me. Someone suggested the UDR which I had not yet heard of really.

<br>

**Redditor suggesting UDR** <br>
>Duke-Kaboom · 9 mo. ago
>Is price the driving factor ?
>
>If not .....best setup UdmProSE. Has built in Poe and extra ports for expansion as well as the ability to add cameras for protect. 3 Ap's Done
>
>If yes. Then Edge router, with separate programming of the ap's. The edge router Interface is basic looking and technical.
>
>But
>
>If you "want the full.ubiquity setup" Sounds like you are looking for the more user friendly "single pane" experience others have described. Then you want the Unifi OS. I'd avoid cloudkey and usg all together as they are the old Platform..
>
>Another mid range option would be go with the UDR. It has 2 Poe ports to power two AP's and it has built in Wifi to act as the 3rd AP. This will still give you the single pane experience but slightly more cost effective.

<br>

**Roadblocked** <br>
Spoke to my Dad this evening to let him know that it's hard to proceed any further given that depending on the camera requirements this will dictate what networking equipment to go. If we're definitley going to get cameras then it makes most sense to get a UDM SE to avoid buying switches seperate to the NVR which will be needed to store the footage from the cameras. Also it will work out cheaper than getting all individual parts and will also make for a cleaner setup overall as it's basically an all in one setup.


<br>



I then looked up whether it's worth getting a UDM Pro or the UDM SE and found [Dream Machine Pro vs SE?](https://www.reddit.com/r/Ubiquiti/comments/uj20p7/dream_machine_pro_vs_se/)


Checked some comparisons [U6+ v U6 lite](https://www.reddit.com/r/Ubiquiti/comments/16sh8zc/u6_v_u6_lite/) and [U6+ vs U6 lite](https://www.reddit.com/r/Ubiquiti/comments/14ipulk/u6_vs_u6_lite/). There is some mention of the U6 Pro which sounds to be the most reliable. 


U6+ vs U6 Lite:
- U6+ has better connection
- U6 Lite uses less RAM
- U6 Lite has more RAM
- U6+ has WiFi 6 on the 2.4Ghz band


[Upgrading my setup: Looking for input on the U6 Plus vs. U6 Lite (currently sold out)](https://www.reddit.com/r/Ubiquiti/comments/14mnvu3/upgrading_my_setup_looking_for_input_on_the_u6/)

I then saw this post where a Network technician says to get the U6 Pro. I'm feeling like the U6 Pro is the most solid option and will be the most reliable

>JacksonCampbell Cake day · 7 mo. ago <br>
Network Technician
Get the U6 Pro. The U6 Lite has the inferior chipset that can have horrible performance issues. The U6+ was made as an upgrade to it in some ways and is better but no Bluetooth. U6 Pro is better than both with WiFi 6 on both bands and MU-MIMO and OFDMA.


### 2.4Ghz vs 5Ghz

Read the following post [Wifi 6 and 2.4Ghz question](https://www.reddit.com/r/HomeNetworking/comments/106iduw/wifi_6_and_24ghz_question/)

I started to read about signals to work out whether I'd benefit from the U6 Pro's 4x4 Mimo > the U7 Pro's 6Ghz. I found out that 2.4Ghz has more range but is generally a slower connection. This can be used for IoT devices as they're on older hardware and don't need quick speeds. Newer devices like phones are better connected on a 5Ghz network but the range may suffer slightly.

This means that I would need to setup 2x VLAN's, 1 which is a 2.4Ghz network for IoT devies, another which is 5Ghz for mobiles / laptops etc. This further clarifies that the U6 Pro is likely the best option but I will research this further.

### What is MIMO

[✅ How Much Faster Is 4x4 vs 2x2 MIMO External Antenna On T-Mobile 5G Home Internet? - FAQ #2](https://www.youtube.com/watch?v=ix3iKr7ZAbA)

It feels like the best option is the U6 Pro due to reliability and that it's got 4x4 MIMO in the 5Ghz range. The U7 Pro has 6Ghz but it seems like that is more if you have gigabit internet speeds which we don't therefore it doesn't seem worth the extra £20. The price difference is £152.40 or £171.60

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

I will add more sections to this as I configure the network and also after buying kit to put the price I paid for everything.

<br>



[YouTube: Unifi Home Network Upgrade - Why I finally switched](https://www.youtube.com/watch?v=wi_geRfabAs)

He spoke about the fact that you could use [linuxserver/unifi-controller](https://hub.docker.com/r/linuxserver/unifi-controller) and run a docker image which you use to run the Unifi-controller.

Checked reddit about this and found [Docker Vs. Raspberry Pi for Controller?](https://www.reddit.com/r/Ubiquiti/comments/xwhtka/docker_vs_raspberry_pi_for_controller/). In the initial statement the user said about hosting the docker image on a synology NAS. Someone in the comments posted a link to [Self-host the Unifi Controller on a Synology NAS](https://www.wundertech.net/self-host-the-unifi-controller-on-a-synology-nas/).

I'm thinking that I may not need a CloudKey and could save 200 if I do decide to get cameras. Either way I think I'll order the access points then go from there. Something important to note is that the **firmware should be updated** if kit is bought as this can prevent issues right away.

<br><br>

### Placing an order

**Thoughts when ordering** <br>
Order placed for 3x [U6+ Access Points](https://uk.store.ui.com/uk/en/products/u6-plus). From here we can then see if anything else is required and can also tune the equipment on arrival. I was going to order 2 however 3 should be fine as if 2 is enough for the house, one can go in the garage.

**Order cancellation** <br>
I found out how to [cancel my order](https://www.reddit.com/r/Ubiquiti/comments/m5s0bx/cancelling_order/) as I forgot to add a switch. I done some more digging and found that people were reporting issues with the U6+ so decided against re-ordering.

<br>

[U6+ vs U6-Lite oddities](https://www.reddit.com/r/Ubiquiti/comments/16d0yi4/u6_vs_u6lite_oddities/)

**RAM differences** <br>
Read this article which says about RAM differences between the U6+ U6 Lite and there is mention of the Pro too. Sounds like it goes U6+ then U6 Lite and then the U6 Pro in terms of how much RAM each has.

**Band usage** <br>
Someone also said in another article about there being issues with 2.4Ghz and saying that the AP's perform way better on 5Ghz. I'm struggling to find any more info about this and cannot find the post I read it on.

<br>

[Recommended hardware to meet Unifi POE requirements?](https://www.reddit.com/r/Ubiquiti/comments/13srj0d/recommended_hardware_to_meet_unifi_poe/)

**Struggling to understand PoE** <br>
Trying to understand how PoE works at the moment so that whatever AP's I get I don't have to run cables to. This would neaten things up a little.
<br><br>

### Power Requirements

The [Flex Mini](https://uk.store.ui.com/uk/en/pro/category/all-switching/products/usw-flex-mini) requires **2.5W** per unit and I'm planning on getting **2** units which would be a total of **5W**

The [U6+](https://uk.store.ui.com/uk/en/products/u6-plus) requires **9W** per unit and I'm planning on getting **3** units which would be a total of **27W**

Overall Total: **32W**

<br>

### PoE Switch vs PoE Injector

[Cheap POE Gigabit Switch 8 Ports?](https://www.reddit.com/r/HomeNetworking/comments/s3oyea/cheap_poe_gigabit_switch_8_ports/)

I found what I thought I was looking for. When searching for cheap PoE switches someone suggested what I was looking for, an 8 port PoE switch. 4 of the ports are PoE and the other 4 are not. It has an overall max power of 64W which would be fine for my usage as I only need 32W as calculated earlier. This would allow for an additional 32W with the remaining 1 port so maybe this could be used to beam Wi-Fi to the garage.

I later realised that this was not fit for purpose as all kit needs to be Ubiquti. 

Having a Ubiquti switch allows:
- Manual power cylcing of PoE devices
- VLAN assignment to port number
- 

<br>

>flywithabuzz · 2 yr. ago <br>
Technically you don't need a PoE switch if you're only planning to use 2 PoE devices. You can get PoE injectors for $10-$15 each....but now you also need to provide power to each of those injector bricks. It's in your best interest to get an 8 port switch with 4 PoE if you're serious about potentially needing 2 more PoE ports.
>
>Also, if you're running cameras, I would highly recommend getting a managed 8-port switch so you can setup VLAN tagging to have better control of who those cameras are sending data.
>
>[Managed 8 Port Switch: $69.99](https://www.amazon.com/TP-Link-TL-SG108PE-Shielded-Lifetime-Protection/dp/B01BW0AD1W/)
>
>Unless you're buying used, the breakdown for getting PoE is:
>
>8 Port Switch : $16.99
>
>8 Port Switch w/4 PoE :$64
>
>1 PoE Injector: $15
>
>8 Port Switch + 4 PoE Injectors: $ 16.99+$45 = $61.99


<br>

[Cheap POE Gigabit Switch 8 Ports?](https://www.reddit.com/r/HomeNetworking/comments/s3oyea/cheap_poe_gigabit_switch_8_ports/) 

In the above post there was some information regarding security cameras / NVR's

>vrtigo1 · 2 yr. ago <br>
Good advice about putting cameras in their own VLAN. If you're using a PC-based DVR like BlueIris, another simpler option for someone that doesn't know anything about VLANs, managed switches, trunk ports and/or firewall ACLs would be to just segregate the entire physical camera network to its own switch, then put two NICs in the DVR PC. Connect 1 NIC to the main network and the other to the camera network. This isn't as secure as putting all the cameras in their own VLAN but it should still prevent them from connecting to the Internet or other devices on the LAN.



Summary of [chat with GPT](https://chat.openai.com/share/c2721371-04a1-4077-9682-901431bbcbe9):
- The Flex Mini is powered via PoE but doesn't provide PoE power
- Flex mini can powered via USB-C or PoE
- PoE sources include, PoE Switch, Router with PoE or an Injector
- EdgeRouter is not part of the Unifi line, this is for ISP's
- Went through power requirements, Ubiquiti has all power requirments on their product pages
- Negatives of using a TP-Link for the PoE switch





<p align="right">(<a href="#readme-top">back to top</a>)</p>














<br><br><br><br><br><br><br>

## Unifi Protect research

[YouTube: Unifi Protect G5 bullet review](https://www.youtube.com/watch?v=BbmrdY2lA5k)

The g4 bullet is better than G5 as it's higher res / looks better at night. There is a comparison on the video
<br><br>


**Chat with GPT (storage requirements)** <br>
I then wondered how much storage will be needed to store 1 months worth of footage for 2x G4 cameras which are recording in 2k for a month straight. I asked GPT this and the following is a link to the chat. [link to ChatGPT](https://chat.openai.com/share/b955b46b-bae4-4b3d-984e-a2b84a373c51)


**Summary of chat** <br>
1GB of storage per day so ~30GB per month. This is not very much if you're planning on deleting the footage when not needed. Using a dream machine would be overkill for this if you're not requiring other features it offers.



Watched a tutorial on how to setup Unifi Protect so that the footage is streamed to the Synology camera system [Adding Cameras to Synology from Unifi](https://www.youtube.com/watch?v=AJYEy093Cdo)

<br>

**Buying G3 camera** <br>
I just went and bought a G3 Flex camera for £35 which I found on facebook marketplace. I've just plugged into the PoE switch but just remered you cannot self host Unifi Protect therfore need to wait until the UDR arrives before I'm able to adopt it.

The next thing to buy will be either a UDM SE to replace the UDR or to get a CloudKey Gen 2 if we choose to have more cameras / the UDR does not have enough storage or RAM.




<br><br>





[DONT buy/upgrade to the Unifi G4 doorbell pro just yet..!](https://www.youtube.com/watch?v=nQSbUTwbCdE&)

Pro differences:
1. Cost over 100+ more
2. Has 8MP package sensor
3. Can be powered with PoE
4. Better microphone quality

[Ubiquiti vs Ring?](https://www.reddit.com/r/Ubiquiti/comments/15ynub5/ubiquiti_vs_ring/)

People say not to look at Ring as it's owned by Amazon. Also you have to pay a monthly subscription cost of £3.49 to store footage.


**Price from Retailer & Ebay** <br>

**Model** | **Retail** | **New** | **Used**
Ubiquiti G4 | £189.18 | £150 | £120
Ring Gen 2 | £99.99 | £45 | -







<br><br>







[Help me decide between Unifi G3 cameras or something like Blink / Arlo etc](https://www.reddit.com/r/homeautomation/comments/7gp6vk/help_me_decide_between_unifi_g3_cameras_or/)

Ubiquiti vs Blink or Arlo

- Wireless (Blink & Arlo) require battery replacements
- Wireless (Blink & Arlo) will degrade Wi-Fi quality when you have multiple
- Cameras should be at least 9ft away from the ground (installed via ladder)
- Storing footage of the interior of your home is a privacy concern
- Ubiquiti has an inferior NVR to someone like Blue Iris
- Locally stored footage can be stolen by a thief



<p align="right">(<a href="#readme-top">back to top</a>)</p>



<br>














**Purchases** <br>

**Date** | **Model** | **Price** | **Platform**
10/01/24 | Ubiquiti UniFi 6 Pro Access Point (U6-Pro) | £117 | ebay
13/01/24 | Ubiquiti UniFi 6 Pro Access Point (U6-Pro) | £129.99 | ebay
16/01/24 | Ubiquiti Unifi Flex Mini Switch (USW-Flex-Mini) | £29.29 | ebay
20/01/24 | Ubiquiti UniFi Dream Router (UDR) | £228.60 | 4gon

**Total Price** <br>
£



<br>










Download the Unifi-controller from [Self-Hosting a UniFi Network Server](https://help.ui.com/hc/en-us/articles/360012282453-Self-Hosting-a-UniFi-Network-Server#:~:text=Start%20the%20newly%20installed%20UniFi,Adopt%20your%20first%20UniFi%20device.)

19:36 - managed to finally adopt the device after mutliple resets of the device. Had to plug it directly into the router rather than into the wall port in the kitchen.












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

SSID: private
Download: 7.26 Mbps
Upload: 6.03 Mbps

SSID: TALKTALK
latency error






### UDM vs UDR

[UniFi Dream Machine vs UniFi Dream Router \| which is the right router for you?](https://www.youtube.com/watch?v=nML_kqFpRSQ)

You can only use Unifi networking stuff and cannot run protect as well when using the UDM therefore it is not fit for purpose

[UDR Fail or Success?](https://www.youtube.com/watch?v=E6K2nITRdeA)

He had issues which were resolved with a software update














Last night setup

Router -> 8 port PoE switch -> AP (Router)
                            -> AP (Kitchen)

Connected some devices up too, all work. The speeds are no better in the lounge for some reason (they were pretty much maxed anyway)

When looking at the client list there are some random devices which were only showing their MAC addresses with no additioanl information

I tried to kick these off then network but they rejoined. I've checked my apple watch and it was connected therefore it must have been shared by my phone / macbook

changed the SSID then the switch was stuck offline








**Auto-connecting MAC addresses** <br>
noted down mac addresses for connected devices and gave them friendly name

going to later set it up so that they auto connect to the network











<br>

**Unblocking a device** <br>
I found out how to unblock a device. The device will appear in the offline section when going to the "Client Devices" option from the left hand sidebar then choosing offline from the top navigation bar.

The blocked devices will appear with a red dot next to them.

![unblocking-device-new-GUI-1](/img/network-research/unblocking%20a%20device%201.png)

![unblock-device-new-GUI-2](/img/network-research/unblock%20a%20device%202.png)


**Setup pt19** <br>
23/01/24 | start 18:14 | end 

On review - check guest settings (it said about hotspot settings)

<br>

Modem -> router -> camera + 8-port-poe-lite

<br>

**Setting up the UDR** <br>
- Setup the UDR via the Unifi Network app
- Created a new SSID when setting up the UDR
- Reset all devices for re-adoption
- Re-adopted all devices
- Updated UDR via Unifi Protect mobile app
- Wiped adoption for G3-Flex
- Managed to adopt 8-port-poe-lite via Unifi Network app
- Adpopted devices: UDR, 8 port switch, 4 port switch, G3 Flex
- Stopped running the local server, from site selector it went grey
- Adopted U6 pro in Dan's room

<br>

**Wiring** <br>
- Wired everything into an extension lead

<br><br>

## Network Configuration
Explanation on all advanced settings within the Unifi-Controller <br>
[UniFi's Advanced Wi-Fi Settings Explained](https://www.reddit.com/r/Ubiquiti/comments/r0dh9p/unifis_advanced_wifi_settings_explained/)

**Reasons for creating a VLAN** <br>
1. **Security:** <br>
If a less secure device like a **Chrome casts**, **Printers** etc is hacked, it will not have access to the rest of the network which has devices like computers, phones, tablets etc are on.
2. **Congestion:** <br>
The more devices added to the network, the more congestion. 

<br><br>

### Creating IoT Network
1. Disable "Auto Scale Network"
2. Gateway/Subnet mask = 192.169.2.1 -> 192.168.107.1

**Advanced Configuration:** <br>
1. Auto -> Manual
2. VLAN ID = 2 -> 107
3. Multicast DNS = Enable
    - This will allow devices on the main network to discover devices on the IoT network. This allows the communication between the devices and facilates things like streaming to chrome cast from mobile phone.
4. "Add Network"

<br><br>

### Creating Guest Network
1. Disable "Auto Scale Network"
2. 192.168.2.1 -> 192.168.10.1

**Advanced Configuration:** <br>
1. VLAN ID = 2 -> 10
2. Network Type = Guest Network
    - This tells the devices that they're alone and that they cannot see any devices on the network. The only thing they can see is the internet. Two devices which are both on the guest network cannot communicate.
3. Disable Multicast DNS
    - Don't want these devices to be able to communciate with chrome cast etc
4. Add Network

<br><br>

### Creating Cameras Network
1. Disable "Auto Scale Network"
2. 192.168.2.1 -> 192.168.20.1

**Advanced Configuration:** <br>
1. VLAN ID = 2 -> 10
2. Disable Multicast DNS
3. Add Network

<br><br>


## WiFi Networks

### Main network
1. Settings>WiFi>Create New
2. Network = Default
3. Create WiFi Network

<br>

### IoT Network
1. Settings>WiFi>Create New
2. Add "_IoT" onto the end of the network name
3. Network = IoT
4. Turn 5Ghz WiFi band off
    - IoT devices generally connect better to 2.4Ghz networks. They struggle with combined SSID's (2.4Ghz + 5Ghz under the same network name)
5. Create WiFi Network

<br>

### Guest Network
1. Settings>WiFi>Create New
2. Add "_Guest" onto the end of the network name
3. Network = GuestNet
4. Create WiFi Network

<br>

## Firewall Rules

<br><br>

**WiFi Connectivity** <br>
- Mapped out the house on my phone 2x times
    - Kitchen AP not picked up
    - Dan's room AP not picked up



<br>

**MAC address privacy** <br>
[[Solved] UniFi Binding: Dealing with MAC Randomization](https://community.openhab.org/t/solved-unifi-binding-dealing-with-mac-randomization/128816)

I found out that Apple hide the MAC addresses for their devices by giving the router a fake MAC address.





<br><br><br><br><br><br><br>


**Initial Research pt1** <br>
04/01/24 | start 21:45 | finish 23:37 | 1 hour 53 minutes

- Overview
- Not sure what else, I moved the content around



**Research pt2** <br>
05/01/24 | 19:46 | 23:35 | 1 hour 29 min

- Found out about self hosting unifi-controller from Docker
- Self-hosting from Synology NAS
- Update firmware to avoid adoption issues
- Might be able to avoid buying a seperate NVR by self-hosting
- Placed order for U6+ then cancelled the order
- Researched U6+ vs U6 Lite
- Further PoE research
- Researched power requirements
- PoE switch vs Injector



**Research pt3** <br>
09/01/24 | 20:44 | 22:55 | 2 hours 11 minutes

- Researched how to setup Unifi Protect
- Further research on UDMP vs UDM SE
- Researched U6+ vs U6 Lite and found out that U6 Pro is the most reliable
- Researched different bands (2.4Ghz and 5Ghz)
- Reasearched MIMO
- U6 Pro vs U7 Pro
- PoE vs Injectors
- Conclusion from research



**Research pt4** <br>
13/01/24 | start 15:54 | end 18:24 | 2 hours 30 minutes

- Researched benefits of buying Ubiquiti switches
    - Seperate VLAN management per port
    - Restart devices via PoE
- How to self-host the controller on Ubuntu
- Watched another summary video of a home setup
- Watched another vs video the UDMP vs the UDMSE



**Research pt6** <br>
14/01/24 | start 9:28 | end 11:52 | 2 hours 24 minutes

- Researched cameras
- Researched how WISP's work
- Researched QNAP vs Synology
- Researching Unifi Protect on Synology NAS
- Researching self-hosting services



**Research pt7** <br>
14/01/24 | start 17:34 | end 18:15 | 41 minutes

- Patched network port into the wall



**Research pt8** <br>
15/01/24 | start 7:55 | end 8:02 | 7 minutes

- Researched camera install in a doctors office



**Research pt9** <br>
19/01/24 | start 18:56 | end 19:37 | 41 minutes

- Downloaded the unifi-controller then self-hosted it from my macbook
- Fixed issues when setting up the Access Point by wiring it directly into the router



**Research pt10** <br>
19/01/24 | start 20:53 | end 00:17 | 3 hours 24 minutes

- Created new network within unifi-controller
- Encountered adoption issues
- Researched how to SSH to switch
- Installed LAN Scan to find the IP
- Tried to reset and power cylce the switch again which resolved the issue
- Tried to fix WiFiman
- Tested the Wi-Fi from brothers room
- Researched the difference between UDM and UDR
- Researched how to configure the network



**Research pt11** <br>
20/01/24 | start 11:15 | end 12:30 | 1 hour 15 minutes

- Setup PoE switch
- Tested speeds from the living room
- Assessed currently connected clients to setup Alias'
- Realised that the MAC addresses were changing



**Research pt12** <br>
20/01/24 | start 15:33 | end 15:45 | 12 minutes

- Noted down MAC addresses so that I may be able to setup auto-connecting or something similar like my work has



**Research pt13** <br>
20/01/24 | start 19:16 | end 21:20 | 2 hours 4 minutes

- Researching how to unblock devices
- Other research?


**Research pt14** <br>
20/01/24 | start 21:20 | end 21:41 | 21 minutes

- Styling network-research page


**Ring gen 2 vs Unifi G4 (non-pro) pt15** <br>
20/01/24 | start 22:35 | end 23:07 | 32 mins

- Researched G4 doorbell vs G4 Pro doorbell
- Researched Ubiquiti vs Ring doorbells & prices


**Updating the Table of contents pt16** <br>
21/01/24 | start 8:36 | end 10:26 | 1 hour 50 minutes

- Researched how to make a table of contents


**Fixing formatting pt17** <br>
21/01/24 | start 11:29 | end 15:09 | 3 hours 40 minutes

- Styling network-research page
- Researched Ubiquiti vs Blink / Arlo


**Fixing formatting pt18** <br>
21/01/24 | start 21:53 | end 23:17 | 1 hour 24 minutes

- Styling network-research page
- moved all time tracking to the bottom of the page
- continued to sort out the contents section
- commited page at pt18
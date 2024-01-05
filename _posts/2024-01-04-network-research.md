---
layout: post
title: Ubiquti Research
date: 2024-01-04 23:11 +0000
categories: learning networking
---

## Table of Contents

- [Overview](#overview)
- [Initial Research](#initial-research)
    - [Access point research](#access-point-research)
    - [Camera research](#camera-research)
    - [Chat GPT storage amount](#chat-gpt-storage-amount)
- [Further Research](#further-research)
    - [Placing an order](#placing-an-order)
    - [Power Requiremnents](#power-requirements)
    - [PoE Switch vs PoE Injector](#poe-switch-vs-poe-injector)

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

This would have been more useful as a guide after all kit arrives. Not worth watching the reasearch stage
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

### Power Requirements:

The [Flex Mini](https://uk.store.ui.com/uk/en/pro/category/all-switching/products/usw-flex-mini) requires **2.5W** per unit and I'm planning on getting **2** units which would be a total of **5W**

The [U6+](https://uk.store.ui.com/uk/en/products/u6-plus) requires **9W** per unit and I'm planning on getting **3** units which would be a total of **27W**

Overall Total: **32W**

<br>

### PoE Switch vs PoE Injector

I read through this [POE switch vs injectors for 2-3 APs?](https://www.reddit.com/r/Ubiquiti/comments/ir1r1u/poe_switch_vs_injectors_for_23_aps/) but didn't understand the logic or what was being said.

and this [I bought a house with 3 Unifi access points installed throughout the house but I have no idea what I need to use them.](https://www.reddit.com/r/HomeNetworking/comments/kqkhup/i_bought_a_house_with_3_unifi_access_points/)

People just talk about whether it's worth getting switches or PoE. Nothing of use here

Video on how to setup an AP with the app [How To Setup a UniFi Access Point WITHOUT A CONTROLLER! (QuickTip)](https://www.youtube.com/watch?v=SOY5Dcu9dwg)

I finally found what I was looking for [Cheap POE Gigabit Switch 8 Ports?](). Someone on this post added the following photo:

When searching [Reddit](https://www.reddit.com/r/HomeNetworking/comments/s3oyea/cheap_poe_gigabit_switch_8_ports/) for cheap PoE switches someone suggested what I was looking for, an 8 port PoE switch. 4 of the ports are PoE and the other 4 are not. It has an overall max power of 64W which would be fine for my usage as I only need 32W as calculated earlier. This would allow for an additional 32W with the remaining 1 port so maybe this could be used to beam Wi-Fi to the garage.

<br>

![8-port-amazon-switch](/img/Screenshot 2024-01-05 at 23.09.47.png)

[Switch suggested](https://www.amazon.com/TP-Link-TL-SG108PE-Shielded-Lifetime-Protection/dp/B01BW0AD1W/?th=1)

On the same [Reddit](https://www.reddit.com/r/HomeNetworking/comments/s3oyea/cheap_poe_gigabit_switch_8_ports/) post there was some information regarding security cameras / NVR's

![VLAN-DVR-advice](/img/Screenshot 2024-01-05 at 23.29.15.png)

[Chat GPT link](https://chat.openai.com/share/c2721371-04a1-4077-9682-901431bbcbe9)
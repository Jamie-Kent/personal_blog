---
layout: post
title: Ubiquti Research
date: 2024-01-04 23:11 +0000
categories: learning github
---

<br>
**04/01/24**
<br><br>
**Research start - 21:45** <br>
**Research finish - 23:37**
<br>
<br>


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

[YouTube: Unifi Protect G5 bullet review](https://www.youtube.com/watch?v=BbmrdY2lA5k)

The g4 bullet is better than G5 as it's higher res / looks better at night. There is a comparison on the video
<br><br>

**Chat with GPT** <br>
I then wondered how much storage will be needed to store 1 months worth of footage for 2x G4 cameras which are recording in 2k for a month straight. I asked GPT this and the following is a link to the chat. [link to ChatGPT](https://chat.openai.com/share/b955b46b-bae4-4b3d-984e-a2b84a373c51)

**Summary of chat** <br>
1GB of storage per day so ~30GB per month. This is not very much if you're planning on deleting the footage when not needed. Using a dream machine would be overkill for this if you're not requiring other features it offers.
<br><br>

[Reddit: Do I need a Unifi gateway?](https://www.reddit.com/r/UNIFI/comments/15rgxt3/do_i_need_a_unifi_gateway/)

Essentially the gateway is for pretty dashboard / for inbuilt storage. Not sure there is much other reason to use it. Someone suggested usign a RaspberryPi as a cloud key using something called [UnifiPi](https://unifipi.com/)

Further research needed here
<br><br>

<br>
**05/01/24**
<br><br>
**Research start - 19:46** <br>
**Research finish - 20:21**
<br>
**break - 10 min**
<br>
<br>

### Further Research

[YouTube: Unifi Home Network Upgrade - Why I finally switched](https://www.youtube.com/watch?v=wi_geRfabAs)

He spoke about the fact that you could use [linuxserver/unifi-controller](https://hub.docker.com/r/linuxserver/unifi-controller) and run a docker image which you use to run the Unifi-controller.

Checked reddit about this and found [Docker Vs. Raspberry Pi for Controller?](https://www.reddit.com/r/Ubiquiti/comments/xwhtka/docker_vs_raspberry_pi_for_controller/). In the initial statement the user said about hosting the docker image on a synology NAS. Someone in the comments posted a link to [Self-host the Unifi Controller on a Synology NAS](https://www.wundertech.net/self-host-the-unifi-controller-on-a-synology-nas/).

I'm thinking that I may not need a CloudKey and could save 200 if I do decide to get cameras. Either way I think I'll order the access points then go from there. Something important to note is that the **firmware should be updated** if kit is bought.
<br>

[Reddit: I understand why people don’t like Ubiquiti now](https://www.reddit.com/r/Ubiquiti/comments/udvz31/i_understand_why_people_dont_like_ubiquiti_now/)

I checked Reddit for reasons not to buy the kit before making the purchase and found the following post. This was a small business complaining about multiple cameras. Someone educated replied and essentially said that Ubiquti is fine but maybe not for his use case / they need to spend more than what that are. This makes me think that it should be ok to order the access points.
<br><br>

### Placing an order

Order placed for 3x U6+ Access Points. From here we can then see if anything is else is required and can also tune the equipment on arrival. I was going to order 2 however 3 should be fine as if 2 is enough for the house, one can go in the garage.

[U6+ Product Page](https://uk.store.ui.com/uk/en/products/u6-plus)

I've placed an order but cancelled it as I was supposed to add a switch to the order using guidance from this reddit post [Cancelling order..](https://www.reddit.com/r/Ubiquiti/comments/m5s0bx/cancelling_order/). Now I'm reading deeper into it, it sounds like the U6+ actually has some issues anyway. I thought it was the same AP as the U6 Lite which it's not.

[U6+ vs U6-Lite oddities](https://www.reddit.com/r/Ubiquiti/comments/16d0yi4/u6_vs_u6lite_oddities/)

Read this article which says about RAM differences between the U6+ U6 Lite and there is mention of the Pro too. Sounds like it goes U6+ then U6 Lite and then the U6 Pro in terms of how much RAM each has.

Someone also said in another article about there being issues with 2.4Ghz and saying that the AP's perform way better on 5Ghz. I'm struggling to find any more info about this and cannot find the post I read it on.

Trying to understand how PoE works at the moment so that whatever AP's I get I don't have to run cables to. This would neaten things up a little. Just read through [Recommended hardware to meet Unifi POE requirements?](https://www.reddit.com/r/Ubiquiti/comments/13srj0d/recommended_hardware_to_meet_unifi_poe/) and am going to read through
<br><br>

Checked power consumption for required devices:

[Flex Mini](https://uk.store.ui.com/uk/en/pro/category/all-switching/products/usw-flex-mini) 

2.5W x 2 = 5W
<br><br>

[U6+](https://uk.store.ui.com/uk/en/products/u6-plus) 

9W x 3 = 27W

**Total:** 27+5 = 32W

I read through this [POE switch vs injectors for 2-3 APs?](https://www.reddit.com/r/Ubiquiti/comments/ir1r1u/poe_switch_vs_injectors_for_23_aps/) but didn't understand the logic or what was being said.


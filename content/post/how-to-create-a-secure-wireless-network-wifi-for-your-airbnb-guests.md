+++
author = "Göran S"
date = "2017-10-03T16:07:37Z"
description = "If you are renting out your home on AirBnB, Booking.com etc or have a small business you may want to offer free WiFi access for clients. To do that in a secure way you don’t want to connect them to your own local network (LAN) where you have your computers, NAS backup and IoT devices connected."
draft = false
keywords = ["AirBnB","Secure WiFi", "Guest Network", "OpenDNS"]
tags = ["AirBnB","Secure WiFi","Guest Network"]
title = "How to create a secure wireless network (WiFi) for your AirBnB guests"
topics = ["topic 1"]
type = "post"

+++
![enter image description here][1]
If you are renting out your home on [AirBnB][2], [Booking.com][3] etc or have a small business you may want to offer free WiFi access for clients. To do that in a secure way you don’t want to connect them to your own local network (LAN) where you have your computers, NAS backup and IoT devices connected.

You want to have an isolated network that is only for your guests. In technical terms you have to create something that is called a VPN or VLAN - virtual private network or virtual local area network. 

The easiest way to do that is using a WiFi router that offers guest access/guest zone as a built in feature. Many routers today have that feature such as Asus, TP-Link, Netgear, Linksys and Ubiquity and the vendors usually have instructions how to do this and there are How-To's that are easy to find.

 - [TP-Link][4]
 - [How to configure guest network on a dual band wireless network router][5]
 - [How to create a private wireless network for your AirBnB guests][6]
 - [How to Create a Guest Network in UniFi Controller][7]
 - [WeMustBeGeeks - How-To][8]

## Configuring the guest network
Log in to the router and select Guest Network (or something similar) from the admin view. Give the the network a meaningful name (SSID).  

Choose an authentication system, such as WPA2-Personal and an access key. It’s not secure to run a guest network that isn’t encrypted, and especially not one with a default password. Create a [strong password (PIN)][9].  

Using a strong password on your guest network will not be a problem for your guests because they will only have to touch the [GoWi.Fi sign][10] with their Android devices and it will instantly get configured with the right SSID and PIN (password).    

Now when you have it setup, log onto the guest network and check that you can not access any of your devices on your own network. 

## Preventing your visitors from doing bad stuff
It is also a good practice to use a web content filter so that your ISP does not report you for downloading illegal content that your visitors is responsible for. You also keep them safe from viruses and ransomware. [OpenDNS][11] is a great solution for this. 

To prevent your guest from circumventing your OpenDNS settings be sure to configure your WiFi routers firewall rules to [force all DNS traffic over port 53][12]. 

If you can don’t give your guests physical access to the router or lock down access to the admin interface and ethernet ports as much as possible.


  [1]: https://res.cloudinary.com/dtnahfj7l/v1507048071/x10x0n9xlwufiudnb3wy
  [2]: https://www.airbnb.com/
  [3]: https://www.booking.com
  [4]: http://www.tp-link.com/us/faq-1082.html
  [5]: http://www.tp-link.se/article/?faqid=649
  [6]: http://www.robbmontgomery.com/2014/03/how-to-create-private-guest-network-for.html
  [7]: https://help.ubnt.com/hc/en-us/articles/115000166827-UniFi-Wireless-Guest-Network-Setup
  [8]: https://www.wemustbegeeks.com/how-to-configure-guest-wifi-with-ubiquiti-edgerouter-and-unifi-access-points/
  [9]: https://passwordsgenerator.net/
  [10]: https://www.gowi.fi/
  [11]: https://www.opendns.com/home-internet-security/
  [12]: https://support.opendns.com/hc/en-us/articles/227988027

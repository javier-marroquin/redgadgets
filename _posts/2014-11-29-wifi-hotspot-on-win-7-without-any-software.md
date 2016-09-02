---
title: WiFi Hotspot on Win 7 Without any Software!
date: 2014-11-29T21:29:52+00:00
author: Redgadget
layout: post
permalink: /wifi-hotspot-on-win-7-without-any-software/
categories:
  - Hack
  - Software
  - Technology
tags:
  - wifi hotspot windows 7 without software
---
Many a times we have to share the internet connection that is available on our laptop to other devices say a phone, another laptop. One way to do that is by using a third party software like Connectify, Virtual Router Manager, Mhotspot etc. ,

The other way, the simpler way is to use your laptop itself as a **WiFi Hotspot**

Here it goes


## <span id="Step_1">Step 1:</span>

Open the Command prompt as Administrator (Right click and select Run as administrator).

## <span id="Step_2">Step 2:</span>

Type the following command in the command prompt and hit &#8216;Enter&#8217;

<pre>netsh wlan set hostednetwork mode=allow ssid=Redgadgets key=ReDGadGeT@321</pre>

**SSID:** Name of your WiFi Hotspot.

**Password:** Password to connect to the newly created WiFi

## <span id="Step_3">Step 3:</span>

Enable the HotSpot

Type the following command and hit enter.

<pre>netsh wlan start hostednetwork</pre>

Now go to Network And Sharing center and You can see your newly created wifi hotspot connection.But, as you can see, it has no network access.We need to fix this by enabling sharing of internet connection for your working Internet connection.In my case, it is wifi connection, but it can be Ethernet or any other working internet connection.

## <span id="Step_4">Step 4:</span>

To enable sharing, Click on your default Internet connection and select Properties. Under the Sharing tab, tick the box saying – Allow other network users to connect through this computer’s Internet connection. Under the Home networking Connection, select the connection which is showing as your hotspot connection.

## <span id="Step_5">Step 5:</span>

In order to stop the Wifi hotspot, Just type the following command in the command prompt.

<pre>netsh wlan stop hostednetwork</pre>

Read: <a href="http://redgadgets.com/protect-eyes-from-computer/" target="_blank">Protect eyes from computer</a>

### <span id="Note">Note:</span>

If you like to use it daily then create a **.bat** where these commands are loaded in it.

Lazy to do that?

Download the file below

[WiFi.zip](/images/WiFi.zip)

Did it work for you? Do you have an alternative? Let us know in the comment section.

Thanks!
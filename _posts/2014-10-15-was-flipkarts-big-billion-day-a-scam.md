---
title: 'Was Flipkart&#8217;s Big Billion Day a scam?'
date: 2014-10-15T20:33:54+00:00
author: Redgadget
layout: post
permalink: /was-flipkarts-big-billion-day-a-scam/
categories:
  - Hack
  - Internet
  - News
tags:
  - big billion day scam
  - flipkart scam
img: flipkart-big-billion-day.jpg
---
In my opinion, Flipkart’s **The big billion day** was a huge scam.
  
First let me explain what I did. Instead of manually refreshing the page every 5 seconds to check if new &#8220;STEAL DEALS&#8221; had arrived, I wrote a simple python script to do the same. You can check out my python script here. [shadowfax92/flipkart_parser.py](https://github.com/shadowfax92/Flipkart-Big-Billion-Day-parser/blob/master/flipkart_parser.py)

Basically, the script parsed Flipkart’s page every 5 seconds to see if any new product had arrived in “STEAL DEAL” section. If a new product had arrived, my scripted shouted “Ring Ring Ring” (Thanks to OS X “say” command :P) on my mac and then send out a mail along with few product details like Name of product, discount offered/price, status of product (whether sold out or not) and the link to the &#8220;shop now&#8221;/&#8221;view product&#8221; page. What I noticed (once the script started working) is very bizarre.

Read: <a href="http://redgadgets.com/flipkart-big-billion-day-story/" target="_blank">Flipkart Big Billion Day Story!</a>

Whenever a new product arrived (the one&#8217;s with crazy discounts like 90% and above) in the “STEAL DEAL” section, it was already in “Sold out” state. This basically means two things, either someone bought all of these products within 5 seconds (which is very unlikely) or Flipkart was simply fooling the customers into believing that they were too late in selecting the product. I think the latter case is more plausible.
  
Indirectly, Flipkart was attracting a huge number of customers to their page who finally ended up buying the next best thing.

Few of the sample mails sent by my script:

Mail-1:

from: X@somemail.com
  
to: Y@somemail.com
  
date: Mon, Oct 6, 2014 at 6:11 PM
  
subject: Simmtronics Xpad X802 Tablet

Simmtronics Xpad X802 Tablet
  
Offer: Sold Out
  
Flat at Rs 99
  
[http://www.flipkart.com/simmtron&#8230;.](http://www.flipkart.com/simmtronics-xpad-x802-tablet/p/itmdjz8q2tey9cfy?pid=TABDJZ8Q2TEY9CFY&offer=D_Day_SimmtronicsXpad_StealDeal)

Mail-2:

from: X@somemail.com
  
to: Y@somemail.com
  
date: Mon, Oct 6, 2014 at 6:11 PM
  
subject: HGST Touro Mobile 2.5 inch 1 TB External Hard Disk

HGST Touro Mobile 2.5 inch 1 TB External Hard Disk
  
Offer: Sold Out
  
Flat 90% Off
  
[http://www.flipkart.com/hgst-tou&#8230;.](http://www.flipkart.com/hgst-touro-mobile-2-5-inch-1-tb-external-hard-disk/p/itmdv9f8ugypcxkb?pid=ACCDHUJHVBD9ZXZU&offer=D_Day_HGST1TBHarddrive_StealDeal)

> &#8211;Nikhil Venkat Sonti

If you had any similar experience or a contrasting opinion then please leave it as a comment.
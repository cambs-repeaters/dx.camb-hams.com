---
id: 2776
title: 'Beaconing the journey to Mull'
date: '2013-05-11T10:19:56+00:00'
author: M0BLF
layout: post
guid: 'http://dx.camb-hams.com/?p=2776'
permalink: /2013/05/11/beaconing-the-journey-to-mull/
video_type:
    - '#NONE#'
categories:
    - General
tags:
    - mull2013
---

The eagle-eyed among you might have noticed that many of us were beaconing on APRS on our journey to Mull, and you might have wondered how we had such good APRS coverage, even in the middle of rural Scotland.

The trick was that M0BLF-9 ahead of the convoy, and M0VFC at the back of the convoy were both acting as APRS igates, able to relay reports from the other cars straight onto the internet. This meant that we could be entirely independent of any local APRS infrastructure.

M0BLF-9 was probably the more complex setup, so that’s what I’m going to explain here:

On the RF side, it was a Kenwood TH-D92 handheld, but with the handheld’s own beaconing and GPS disabled, so it was just acting as a TNC+rig. The handheld was connected via USB to a laptop running APRSIS32 (running off an inverter). The APRS software was set up to gate received packets to APRS-IS. In order to beacon itself, however, the laptop needed to ‘know’ where it was, and this was achieved by a Bluetooth dongle in the laptop, communicating with a Bluetooth GPS receiver (this had the added effect of improving the D72’s battery life, as the rig’s GPS could be disabled). The internet connection to the laptop was provided by a mobile phone set up to allow Wifi tethering. The theory was that, with several miles between M0VFC and I, and with our phones on different networks, the effect of any holes in mobile phone coverage should be minimal.

The result was that we had pretty good coverage across the whole journey, and we’ll be repeating this setup on the way back if you want to follow our progress.

[![Our arrival on APRS](http://dx.camb-hams.com/wp-content/uploads/2013/05/aprs-mull.png)](http://dx.camb-hams.com/wp-content/uploads/2013/05/aprs-mull.png)
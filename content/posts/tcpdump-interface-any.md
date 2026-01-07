+++
title = "tcpdump -i any"
date = "2026-01-06T21:47:36-07:00"
description = "TIL about `-i any` in `tcpdump`"
showFullContent = false
readingTime = false
hideComments = false
+++

Today I Learned that you can use `-i any` in `tcpdump` to capture packets on all interfaces. This is a huge time saver when I don't remember the specific interface name on a server and just want to quickly look at a packet capture. [[link](https://www.tcpdump.org/manpages/tcpdump.1.html)]
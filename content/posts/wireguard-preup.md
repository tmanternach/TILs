+++
title = "Wireguard PreUp/PostDown"
date = "2025-12-20T08:25:31-07:00"
description = "TIL you can run scripts when Wireguard connects or disconnects"
showFullContent = false
readingTime = false
hideComments = false
+++

I have been a Wireguard user for many years now. But Today I Learned you can configure "PreUp, PostUp, PreDown, PostDown" scripts just like a normal Linux network interface. I am using this on a Proxmox server to make sure IP Forwarding is enabled whenever the Wireguard interface is up.

```
[Interface]
PrivateKey = [hidden]
Address = 172.16.0.13/24
PreUp = sysctl net.ipv4.ip_forward=1
PostDown = sysctl net.ipv4.ip_forward=0
```

The only place I can find this documented is in the `wg-quick` man page, found [here](https://manpages.debian.org/unstable/wireguard-tools/wg-quick.8.en.html).
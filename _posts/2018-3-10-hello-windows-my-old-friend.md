---
layout: post
title: Hello Windows, my old friend
tags: windows hardware drivers gpu solidworks
lang: en_US
---
I've been using a MacBook for the past 3 years and I loved it absolutely; loved it so much that I almost forgot what Windows felt like. That was until yesterday. I bought a used Acer V5-573G ([benchmark](http://www.userbenchmark.com/PCBuilder/Custom/S3484-M2485.7928.3227.89289vsS3484-M2485.7928.3227.89289)).

My sole purpose to use it for product development, or specifically, to make basic Solidworks assemblies. The GPU felt like a good enough compromise for SWX, owing to my budget. Other hardware specs also should give a promising SWX experience, at least in theory. That was until I realized how painful Windows can become.

So I did a clean install of Windows 10, installed a ton of hardware drivers and installed Solidworks 2016.

When I first opened SWX it took it's time, and that little icon notification bar indicated the software is running on my NVIDIA GPU. But when I sketched a simple part and added some very basic features, it was laggy as hell. I couldn't even rotate my part smoothly. Then I ran the benchmark test offered by the software itself to see what's up. The laptop could not even zoom in/out of an assembly without lagging. It was horrible and frustrating.

So I did what any sane man would do; Googled to check if someone else to had this problem. It was a quick yes, none of them seemed to find a technical solution for the problem. It appeared Nvidia drivers were having compatibility issues with Solidworks 2016, and manufacturer hasn't resolved it.

Now we all know why. Nvidia is releasing a seperate line of GPUs (Quadro) for product development softwares for a higher price range. It is not likely for them to make their gaming cards also compatible with those software.

So I spent a complete Saturday for rolling back and forth GPU drivers to find one that works with my software, upgrading and downgrading the OS untill Solidworks responds to it. And finally it did, on GPU driver version 311.15 and Windows 7.

I am taking this moment to thank Nvidia for being this arrogant, and to thank Windows for reminding me what a nightmare an OS can become.

Peace! ✌️
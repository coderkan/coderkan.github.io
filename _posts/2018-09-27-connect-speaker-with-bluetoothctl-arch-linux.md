---
layout: post
title: "Connect to Speaker with Bluetoothctl in BBQLinux"
description: 
headline: 
modified: 2018-09-27
category: linux
tags: [linux,bluetooth,bluetoothctl]
imagefeature: 
mathjax: 
chart: 
comments: true
featured: true
---

Hi everyone,

In this post I will show you how to connect bluetooth speaker device in BBQLinux with terminal using bluetoothctl. Nowadays there are a lot of devices including bluetooth like speakers, headsets. So if you are Linux user you need to use comman-line interface to done your jobs. Sometimes UI solutions not working properly. 

# What is Bluetooth?

Bluetooth is a standard for the short-range wireless interconnection of cellular phones, computers, and other electronic devices. SHortly is a protocol for wireless communication. It was developed in 1990s, to reduce the number of cables. Nowadays all electronic devices has also bluetooth to communicate eachother.

# Using Bluetoothctl

If you have electronic devices and connect to them, bluetoothctl is very good option to use in command-line. **Bluetoothctl** is command-line interface in [Bluez]() bluetooth stack. 

If you dont have this program you simply install like that from terminal.

Type:

    yaourt bluez

and select bluez package.

<p align="center">
    <img src="{{ site.url }}/images/Linux/bluetoothctl/install_bluez.png">
</p>

After installed you will see it in terminal if type **bluetoothctl**.

Firstly We need to start **bluetooth.service** in terminal.

    systemctl start  bluetooth.service

After that you can also control bluetooth.service status.

    systemctl status  bluetooth.service.

Your bluetooth.service if running successfully you will see these in your terminal.

    [coderkan@coderkanpc ~]$ systemctl status bluetooth.service 
    * bluetooth.service - Bluetooth service
    Loaded: loaded (/usr/lib/systemd/system/bluetooth.service; enabled; vendor pres
    Active: active (running) since Thu 2018-09-27 20:12:55 +03; 19s ago
        Docs: man:bluetoothd(8)
    Main PID: 5783 (bluetoothd)
    Status: "Running"
        Tasks: 1 (limit: 4915)
    CGroup: /system.slice/bluetooth.service
            `-5783 /usr/lib/bluetooth/bluetoothd


After running your bluetooth.service, we can type **bluetoothctl** in terminal.

    [coderkan@coderkanpc ~]$ bluetoothctl  
    Agent registered
    [bluetooth]# 

Successfuly entered bluetoothctl your terminal has looks like above. 

To scanning device;

    [bluetooth]# power on
    Changing power on succeeded
    [bluetooth]# default-agent 
    Default agent request successful
    [bluetooth]# scan on
    Discovery started
    [NEW] Device 70:99:1C:0C:0F:8D JBL GO 2
    [NEW] Device 47:43:0C:D1:2C:A2 47-43-0C-D1-2C-A2    

type **power on, default-agent** and after that **scan on** command to scanning bluetooth devices.

To pair devices;

    [bluetooth]# pair 70:99:1C:0C:0F:8D 
    Attempting to pair with 70:99:1C:0C:0F:8D
    [CHG] Device 70:99:1C:0C:0F:8D Connected: yes
    [CHG] Device 70:99:1C:0C:0F:8D UUIDs: 00001108-0000-1000-8000-00805f9b34fb
    [CHG] Device 70:99:1C:0C:0F:8D UUIDs: 0000110b-0000-1000-8000-00805f9b34fb
    [CHG] Device 70:99:1C:0C:0F:8D UUIDs: 0000110c-0000-1000-8000-00805f9b34fb
    [CHG] Device 70:99:1C:0C:0F:8D UUIDs: 0000110e-0000-1000-8000-00805f9b34fb
    [CHG] Device 70:99:1C:0C:0F:8D UUIDs: 0000111e-0000-1000-8000-00805f9b34fb
    [CHG] Device 70:99:1C:0C:0F:8D ServicesResolved: yes
    [CHG] Device 70:99:1C:0C:0F:8D Paired: yes
    Pairing successful
    [CHG] Device 70:99:1C:0C:0F:8D ServicesResolved: no
    [CHG] Device 70:99:1C:0C:0F:8D Connected: no
    [bluetooth]#

type **pair device-adress**. 


After pairing with bluetooth device we can connect to device now.
This is very simple to do it. Just type **connect device-adress**.

    bluetooth]# connect 70:99:1C:0C:0F:8D 
    Attempting to connect to 70:99:1C:0C:0F:8D
    [CHG] Device 70:99:1C:0C:0F:8D Connected: yes
    Connection successful
    [CHG] Device 70:99:1C:0C:0F:8D ServicesResolved: yes
    [JBL GO 2]#

If you see your terminal like above your connection is successfully. Now you can enjoy with music.

If you would like to close your connection and scan you just write this command your terminal. 

    scan off
    power off
    disconnect

To exit **[bluetooth]** section just type **exit**.


<p align="center">
    <img src="{{ site.url }}/images/Linux/bluetoothctl/result_terminal_image.png">
</p>

I hope you enjoy reading.

Have a nice coding.


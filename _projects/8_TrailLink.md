---
layout: post
title: Trail Link
github: https://github.com/KengLL/Hiking-Board-ESPNOW
image: /img/in-post/post-eleme-pwa/ChatGPT%20Image%20Jun%203,%202025,%2010_18_28%20AM.png
description: lightweight, battery-efficient peer-to-peer (P2P) communication system
tags:
  - "Software Development"
  - "Embedded System"
---
# TrailLink - Communication Device

A lightweight, battery-efficient peer-to-peer (P2P) communication system designed to keep hiking groups connected—even in remote areas with no Wi-Fi or cellular service.

## Overview

**TrailLink** is a simple and reliable messaging device that uses the **ESP-NOW protocol** to enable short, predefined message exchanges between hikers. Whether you're hiking, camping, or in areas with limited connectivity, TrailLink ensures your group stays in touch.

> 🛠 Built with ESP32 S3  
> 📶 Communicates using ESP-NOW (no internet required)  
> 📬 Supports predefined messages for efficient interaction  
> 🔋 Battery-efficient and portable  
> 📦 3D-printed enclosure for durability in the field

![TrailLinkPoster](/img/in-project/TrailLink%20-%20Communication%20Device.png)
----------

## Problem

When hiking in groups across remote terrains, physical distance can lead to disconnection and safety concerns. Cellular and Wi-Fi networks often fail in such environments, making a dedicated offline communication system essential.

----------

## Key Features

-   **Battery Efficient**: Runs on a 9V battery with power regulation
    
-   **P2P Mesh Networking**: Uses ESP-NOW for direct or relayed communication
    
-   **Simple UI**: OLED screen for reading messages and button-based input
    
-   **Inbox System**: View received messages
    
-   **Message Relay**: Messages can hop across intermediate devices
    
-   **Transmission Range**: ~150m verified range
    
-   **Scalable**: Supports 4+ users per group and up to 35 messages per package
    

----------

## System Architecture

### 📦 Hardware

-   **ESP32 S3 Dev Module**
    
-   **OLED Display** (I2C interface)
    
-   **Push Buttons** for input
    
-   **9V Battery + Voltage Regulator**
    
-   **Custom PCB** (Designed in KiCad)
    
-   **3D Printed Enclosure** with access for USB-C charging, buttons, and battery
    

### 🧠 Software

-   **ESP-NOW Protocol** for low-power, low-latency communication
    
-   **Message State Machine** for managing send/receive/relay
    
-   **Predefined Message System** for quick, structured communication
    
-   **Inbox and Bulletin Board System**: Savepoint-based messaging
    

----------

## Device Block Diagram


----------

## Message Relay Mechanism

-   **Messenger Mode**: Users carry and forward messages physically across nodes.
    
-   **Bulletin Board Mode**: Devices left at fixed locations act as message savepoints.
    

----------

## State Diagram

The device follows a structured flow:

1.  Start State
    
2.  Action Decision (Send, Receive, or Pair)
    
3.  Based on input:
    
    -   **Send** → Carry/Broadcast Message
        
    -   **Receive** → Display or Store Message
        

----------

## Results

-   ✅ **Tested Transmission Range**: 150 meters
    
-   ✅ **Support for Groups**: 4+ users
    
-   ✅ **Scalability**: Up to 35 messages per transmission
    
-   ✅ **Reliable P2P Communication** without needing Wi-Fi or mobile data
    

----------

## Authors

-   Keng-Lien Lin
    
-   Roberto Reyes
    
-   Hou Dren Yuen
    

Developed as part of **ECE 196 (Spring 2025)** at **UC San Diego - Department of Electrical and Computer Engineering**

----------

## Resources

-  [🔗 Website](https://sites.google.com/ucsd.edu/ece-196-fp-s25/home?authuser=0)
    
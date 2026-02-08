---
title: Setting Up WayStation
description: 
published: 1
date: 2026-02-08T11:23:34.320Z
tags: 
editor: markdown
dateCreated: 2026-02-08T11:00:37.578Z
---

# This is how to setup the WayStation in start.np6
>Make sure your IP are set in the _WAYSTATION_pos-db.xml inside of posdata in order for the devices to find each other read the prior docs in order to proceed
{.is-warning}

## Setting the IP
First thing your going to want to do is set the IP inside of _WAYSTATION_pos-db.xml, This is critical as it lets the KVS and all the other devices see the WayStation, The picture below will show where the file is located![screenshot_2026-02-08_051845.png](/screenshot_2026-02-08_051845.png)
>I would recomend using NP++ as these files are xml and its easier to read with it
{.is-info}

Upon Opening the file search for this block
```
<Section name="Messaging">
         <Parameter name="networkAdaptorBaseIp" value="192.168.1"/>
         <Parameter name="Np6WayCoreServerPort" value="2136"/>
         <Parameter name="ProductionSharpServerPort" value="4423"/>
         <Parameter name="serverPort" value="2225"/>
         <Parameter name="NpSharpServerPort" value="24423"/>
         <Parameter name="multicastIp" value="233.0.0.177"/>
         <Parameter name="multicastPort" value="4176"/>
      </Section>
```

Change the "networkAdaptorBaseIp" value="192.168.1"/>, to the first 3 octets of your computers IP

## Sample WayStation Config
The code below is my sample config for my WayStation,
```
..\bin | npapp.exe "..\POSDATA\_WAYSTATION_pos-db.xml" "..\OUT" "..\TEMP" pos-log61.properties
..\bin | npapp.exe "..\POSDATA\_PROD_PRI_pos-db.xml" "..\OUT" "..\TEMP" pos-log61.properties

```
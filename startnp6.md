---
title: Setting Up WayStation
description: 
published: 1
date: 2026-02-08T11:27:04.536Z
tags: 
editor: markdown
dateCreated: 2026-02-08T11:00:37.578Z
---

# This is how to setup the WayStation in start.np6

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

Change the "networkAdaptorBaseIp" to the first 3 octets of your computers IP, and do the exact same for the _PROD_PRI_pos-db.xml

## Sample WayStation Config
The code below is my sample config for my WayStation,
```
..\bin | npapp.exe "..\POSDATA\_WAYSTATION_pos-db.xml" "..\OUT" "..\TEMP" pos-log61.properties
..\bin | npapp.exe "..\POSDATA\_PROD_PRI_pos-db.xml" "..\OUT" "..\TEMP" pos-log61.properties

```
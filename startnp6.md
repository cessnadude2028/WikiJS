---
title: Setting Up WayStation
description: 
published: 1
date: 2026-02-08T11:14:23.722Z
tags: 
editor: markdown
dateCreated: 2026-02-08T11:00:37.578Z
---

# This is how to setup the WayStation in start.np6
>Make sure your IP are set in the _WAYSTATION_pos-db.xml inside of posdata in order for the devices to find each other read the prior docs in order to proceed
{.is-warning}

## Setting the IP
First thing your going to want to do is set the IP inside of _WAYSTATION_pos-db.xml, This is critical as it lets the KVS and all the other devices see the WayStation,

## Sample WayStation Config
The code below is my sample config for my WayStation,
```
..\bin | npapp.exe "..\POSDATA\_WAYSTATION_pos-db.xml" "..\OUT" "..\TEMP" pos-log61.properties
..\bin | npapp.exe "..\POSDATA\_PROD_PRI_pos-db.xml" "..\OUT" "..\TEMP" pos-log61.properties

```
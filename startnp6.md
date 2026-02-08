---
title: Adding Devices To Start.np6
description: 
published: 1
date: 2026-02-08T11:00:37.578Z
tags: 
editor: markdown
dateCreated: 2026-02-08T11:00:37.578Z
---

# This is how to add terminals or KVS to start.np6

The code below is my sample config for my WayStation,
```
..\bin | npapp.exe "..\POSDATA\_WAYSTATION_pos-db.xml" "..\OUT" "..\TEMP" pos-log61.properties
..\bin | npapp.exe "..\POSDATA\_PROD_PRI_pos-db.xml" "..\OUT" "..\TEMP" pos-log61.properties

..\bin | npapp.exe "..\POSDATA\_POS12_pos-db.xml" "..\OUT" "..\TEMP" pos-log61.properties
..\bin | npapp.exe "..\POSDATA\_POS13_pos-db.xml" "..\OUT" "..\TEMP" pos-log61.properties

..\bin | npapp.exe "..\POSDATA\_KVS33_pos-db.xml" "..\OUT" "..\TEMP" pos-log61.properties
..\bin | npapp.exe "..\POSDATA\_KVS34_pos-db.xml" "..\OUT" "..\TEMP" pos-log61.properties
..\bin | npapp.exe "..\POSDATA\_KVS35_pos-db.xml" "..\OUT" "..\TEMP" pos-log61.properties
..\bin | npapp.exe "..\POSDATA\_KVS31_pos-db.xml" "..\OUT" "..\TEMP" pos-log61.propertie
```
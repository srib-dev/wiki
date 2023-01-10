---
title: "Broadcast Server"
linkTitle: "BCS"
date: 2023-01-10
weight: 2
description: >
  En beskrivelse av BCS.
---

BCS er et program som må kjøre på en kompatibel versjon av Windows Server. Den har som oppgave å fasilitere for kommunikasjonen mellom alle instanser av DigaSystem. BCS må kjøre i Administrator modus for at den skal kunne gjøre endringer i XML-databasen.

Det viktigste den gjør er å fasilitere for kommunikasjonen mellom Turboplayer, DigAIRange og DBM. Uten denne fasiliteringen, kan ikke Turboplayer hente ut sendeplaner og laste inn lydfiler fra NAS-et. 

BCS administrerer også sendeplanen lokalt på den maskinen som kjører BCS. Den sendeplanen er lagret som en XML database. 

BCS kan, og burde, kjøre i samsvar med en "Buddy", altså en sekundær instans av BCS som kjører i "Buddy"-modus. Når BCS-instansen som kjører i "Master"-modus kreperer, tar Buddy-BCS over jobben til Master-BCS og fortsetter å fasilitere kommunikasjonen. 

Buddy-BCS administrerer også sendeplanen lokalt på maskinen den kjører på, hvilket også er en XML-database. Men den er aktivt synkronisert med Master-BCS sin XML-database.


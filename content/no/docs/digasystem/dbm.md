---
title: "Database Manager"
linkTitle: "DBM"
date: 2023-01-10
weight: 2
description: >
  En beskrivelse av DBM.
---

DBM er databasesystemet som ligger i kjernen av DigaSystem. Dette er programmet en bruker for å administrere lagrede lydklipp og sanger. Det er også mulig å bruke DBM for videoklipp, reklamer og bilder, men det er ikke spesielt relevant for radiodrift. 

Det er en rekke ting en kan gjøre for å forvalte innholdet av DBM på en bedre måte.

1. Tildele merkelapper til lydfiler.
2. Fordele lydfiler inn i ulike tabeller.
3. Legge til beskrivelser.
4. Fylle ut lydfilenes metadata korrekt.
5. Begrense rettighetene til ulike brukere.

Siden dette er kjernen av DigaSystem, er alle de andre programmene i utgangspunktet bare en modul av databasen som bare kan åpnes ved å åpne DBM først. Nyere versjoner av MultiTrack kan installeres som et separat program på datamaskinen. Så en kan derfor teknisk sett ha en datamaskin bare dedikert til lydredigering. 
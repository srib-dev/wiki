---
title: "Sound Empire Caster 1.2.8"
linkTitle: "SE Caster"
date: 2023-06-21
weight: 1
description: >
  En forklaring av lydkringkastingsprogrammet Sound Empire Caster.
---

### Kort forklaring

Sound Empire Caster er en "standalone" programvare for Windows. "Standalone" betyr at den ikke kommer med et installasjonsprogram og kan bare kjøres ved å starte `.exe`-filen i mappen.

Siste versjon er `1.2.8` (21.06.23) og ble lansert i 2021. Utviklerne er Ukrainsk, så ut av åpenbare grunner, er det godt mulig at det ikke kommer flere oppdateringer på en stund.

Dette programmet kan brukes til å opprette en lydstrøm fra en lokallydkilde, omgjøre det til en viss lyd-kodek og sende det til lydstrøm-server. I vårt tilfelle bruker vi en kanal på det lokale lydkortet til [opptaks-PC'en](/docs/computers/serverrom/opptak) for å opprette lydstrømmer med diverse lyd-kodeker. Vi sender de lydstrømmene til en IceCast2-server på [radio.srib.no](/docs/webservices/radio) for internett-kringkasting.

En viktig ting å kunne er hva en "enkoder" er. Med "enkoder" menes egentlig bare en lydstrøm. Når du oppretter en "enkoder" i SE Caster oppretter du en kanal som konverterer lydkilden til den gitte lydkodeken. En lydkodek er et program som implementerer en algoritme som komprimerer og dekomprimerer digital lyd data  i følge et visst lydfilformat. 

Du kan se på det som at SE Caster er en fabrikk, mens enkoderne er samlebånd hvor ting pakkes automatisk inn i pakker. For hvert samlebånd i fabrikken, er det en ulik innpakkingsmetode av varene som kommer på samlebåndet. Fabrikken pakker altså inn de samme tingene inn i pakker som ser ulike ut, og åpnes på ulike måte.

### Konfigurering

Når en først kjører programmet, er det et par ting en trenger å fikse. Trykk deg inn på generelle innstillinger for SE Caster og...

1. Sørg for at riktig kanal på lydkortet er valgt som inngangskilde.
2. Endre "Station info" til å være aktuelt for radioen. 
3. Sørg for at "Start with windows" er krysset av.

### Hvordan lage ny enkoder

For å lage en ny enkoder gjør du følgende:

1. Trykk på det røde pluss-tegnet.
2. Fyll inn riktig informasjon:

| Parameter | Forklaring |
| --------- | ---------- |
| Stream type | Hvilken lydstrømmingsservertjeneste serveren bruker | 
| Server | IP-adressen eller domenenavnet til IceCast2 |
| Port | Hvilken port som serveren skal motta lydstrømmen på |
| Username | Brukernavnet som skal assosieres med lydstrømmen. Dette trengs for at serveren skal godta lydstrømmen. Dette finner du ved å logge inn på [radio.srib.no](https://radio.srib.no) |
| Password | Passordet som skal assosieres med lydstrømmen. Dette trengs for at serveren skal godta lydstrømmen. Dette finner du ved å logge inn på [radio.srib.no](https://radio.srib.no) |
| Mount/Stream ID | Det designerte "stedet i serveren" lydstrømmen skal sendes til. Det tilsvarer "slug"-en som skal legges til domene-navnet for å aksessere lydstrømmen. (I https://domene.eksempel.no/**lolololol.kek**, er det merkede "slug"-en) "Slug"-en må inkludere en filformat-utvidelse som korresponderer med filformatet i "Type"-feltet |
| Title Mode | Hvorvidt tittelen assosiert med strømmen skal vises, samt hvilken tekst-dekoder som skal brukes. |
| Type | Her velger du lydfilformatet som enkoderen skal omgjøre lydkilden til. |
| Bitrate | Her velger du bitraten som lydstrømmen skal sendes i. Jo høyere bitrate, jo bedre kvalitet på lyden. Men lytteren bruker også mer data for å lytte på strømmen jo høyere bitraten er |
| Channels | Her velger du om lydstrømmen skal være i mono eller stereo |

3. Når alt er fylt inn, lagrer du. Om du får noe feil, kan du lett endre det i ettertid. 
4. for å starte lydstrømmingen, trykker på på "play"-knappen.

NB: For å slette enkoderen, trykker du først på enkoderen. Deretter trykker du på det gule minus-tegnet. 
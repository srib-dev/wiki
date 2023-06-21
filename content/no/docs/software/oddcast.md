---
title: "OddCast V3"
linkTitle: "OddCast V3"
date: 2023-06-21
weight: 2
description: >
  En forklaring om lydkringkastingsprogrammet Oddcast.
---

### Kort forklaring

OddCast V3 er en "standalone" programvare for Windows. "Standalone" betyr at den ikke kommer med et installasjonsprogram og kan bare kjøres ved å starte `.exe`-filen i mappen.

Såvidt jeg har sett på interwebzen, er ikke det mulig å finne filene til dette programmet lenger, siden OddCast V3 har endret navn til [AltaCast](http://www.altacast.com/). Så ta godt vare på disse programfilene, så lenge det er aktuelt. 

Dette programmet kan brukes til å opprette en lydstrøm fra en lokallydkilde, omgjøre det til en viss lyd-kodek og sende det til lydstrøm-server. I vårt tilfelle bruker vi en kanal på det lokale lydkortet til [opptaks-PC'en](/docs/computers/serverrom/opptak) for å opprette lydstrømmer med diverse lyd-kodeker. Vi sender de lydstrømmene til en IceCast2-server på [radio.srib.no](/docs/webservices/radio) for internett-kringkasting.

En viktig ting å kunne er hva en "enkoder" er. Med "enkoder" menes egentlig bare en lydstrøm. Når du oppretter en "enkoder" i OddCast V3 oppretter du en kanal som konverterer lydkilden til den gitte lydkodeken. En lydkodek er et program som implementerer en algoritme som komprimerer og dekomprimerer digital lyd data  i følge et visst lydfilformat. 

Du kan se på det som at OddCast V3 er en fabrikk, mens enkoderne er samlebånd hvor ting pakkes automatisk inn i pakker. For hvert samlebånd i fabrikken, er det en ulik innpakkingsmetode av varene som kommer på samlebåndet. Fabrikken pakker altså inn de samme tingene inn i pakker som ser ulike ut, og åpnes på ulike måte.

NB: Dette er ikke den foretrukne lydstrømkringkasteren. Bruk heller [SE Caster](/docs/software/soundempire). I skrivende stund brukes OddCast V3 bare for å strømme i filformatet FLAC. 

### Konfigurering

Når en først kjører programmet, er det et par ting en trenger å fikse. Trykk deg inn på generelle innstillinger for OddCast V3 og...

1. Sørg for at riktig kanal på lydkortet er valgt som inngangskilde.
2. Endre "YP Info", inne på konfigureringen til enkoderen, til å være aktuelt for radioen. 
3. Sørg for at "Autostart" er krysset av

### Hvordan lage ny enkoder

For å lage en ny enkoder gjør du følgende:

1. Trykk på "Add Encoder".
2. Høyreklikk på den nye enkoderen og velg "Configure" 
3. Under "Basic Settings", fyll inn riktig informasjon:

| Parameter | Forklaring |
| --------- | ---------- |
| Bitrate | Her velger du bitraten som lydstrømmen skal sendes i. Jo høyere bitrate, jo bedre kvalitet på lyden. Men lytteren bruker også mer data for å lytte på strømmen jo høyere bitraten er |
| Quality | Bare relevant for OggVorbis. Du kan velge dette i stedet for Bitrate |
| Sample Rate | Her velger du sample rate for lydstrømmen |
| Channels | Her velger du om lydstrømmen skal være i mono eller stereo |
| Encoder Type | Her velger du lydfilformatet som enkoderen skal omgjøre lydkilden til. |
| Server type | Hvilken lydstrømmingsservertjeneste serveren bruker | 
| Server IP | IP-adressen eller domenenavnet til IceCast2 |
| Server Port | Hvilken port som serveren skal motta lydstrømmen på |
| Encoder Password | Passordet som skal assosieres med lydstrømmen. Dette trengs for at serveren skal godta lydstrømmen. Dette finner du ved å logge inn på [radio.srib.no](https://radio.srib.no) |
| Mountpoint | Det designerte "stedet i serveren" lydstrømmen skal sendes til. Det tilsvarer "slug"-en som skal legges til domene-navnet for å aksessere lydstrømmen. (I https://domene.eksempel.no/**lolololol.kek**, er det merkede "slug"-en) "Slug"-en må inkludere en filformat-utvidelse som korresponderer med filformatet i "Type"-feltet |
| Reconnect Seconds | Hvor mange sekunder OddCast skal vente før den prøver å tilkoble enkoderen til serveren på nytt igjen |

3. Når alt er fylt inn, lagrer du. Om du får noe feil, kan du lett endre det i ettertid. 
4. for å starte lydstrømmingen, trykker på på "Connect".

NB: For å slette enkoderen, høyreklikker du først på enkoderen. Deretter velger du "Delete encoder" 
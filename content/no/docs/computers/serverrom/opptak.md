---
title: "Hjemmesnekret PC: Opptak"
linkTitle: "Opptak"
date: 2023-02-05
weight: 2
description: >
  En beskrivelse av Opptaks-PC'en.
---

### Funksjon

Funksjonen til denne PC-en er tredelt. Den første oppgaven er å ta automatiske opptak av hva enn som sendes ut på luften (FM, DAB og nettradio). Den andre er å kringkaste det aktuelle lydsignalet ut på DAB og nettradio. Den tredje er å være en kilde for stille-alarm innhold. 

### Automatiske opptak

Automatiske opptak blir gjort gjennom et program som heter MultiCoder. Det er et av DigaSystem sine tilleggsprogrammer. [Det er forklart mer om her](/docs/digasystem/multicoder)

### Kringkasting på nett/DAB

Kringkasting på nettradio og DAB gjøres gjennom et program som heter [SoundEmpire Caster](https://www.mediafire.com/file/wh2xwpcl3mx839s/SECaster128.zip/file)(Utvikleren er ukrainsk, så den originale nettsiden er ikke å finne, av åpenbare grunner). I tillegg strømmes det også ved å bruke Oddcast V3, hvilket ikke utvikles lenger. 

I disse programmene kan du lage en liste av lydstrøm-elementer, som kalles "enkodere", for å strømme lyd fra en valgt lydkanal til et valgt domene/IP-adresse. 

Gjennom disse to programmene strømmes et lydsignal til IP-adressen til en IceCast2-server, som er [radio.srib.no](https://radio.srib.no). Mer spesifikt så kjører det en tjeneste på radio.srib.no som heter [AzuraCast](https://docs.azuracast.com/en/home). 

Det er denne nettsiden som nettradioen, [lytt.srib.no](https://lytt.srib.no), henter lyd fra. 

For å sende lydsignalet ut på DAB, har vi en egen enkoder i et av disse programmene som sender til DAB-sentralen sin tilsvarende nettside. 

### Stille-alarm

Stille-alarmen er en lydkilde som byttes til om de planlagte sendingene går stille. Den består av en liste av lydklipp, hovedsakelig sanger, som spilles av i VLC. 

Avspillingen er dedikert til en spesifikk kanal på PCIe-lydkortet som er installert på maskinen. Den kanalen er koblet direkte opp mot kanalvelgeren som en AES-innfôrskilde.

Det som bestemmer om kanalvelgeren skal bytte til stille-alarmen er et hjemmesnekret script som måler hvor stille det er på den aktive kanalen. Om det er for stille for lenge, bytter den til stillealarm-kanalen. 

### Sjekkliste

En liten sjekkliste av hva du må forsikre deg om faktisk kjører, når du skrur på maskinen igjen.

1. Start MultiCoder. [Detaljer her](/docs/digasystem/multicoder)
2. Start stillealarm-spillelisten.
   1. Åpne mappen med alle lydklippene.
   2. Dra -og slipp alle filene over VLC-programmet.
   3. Gå til "Audio Settings > Aduio Device" og sørg for at riktig lydkanal er valgt.
3. Start Sound Empire Caster. [Detaljer her](/docs/software/soundempire)
4. Start Oddcast V3. [Detaljer her](/docs/software/oddcast)

### Spesifikasjoner

| Feature | Value |
| ------- | ----- |
| Prosessor | AMD A10-6790K APU with Radeon HD Graphics, 4000 MHz, 2 kjerner, 4 logiske prosessorer |
| Hovedkort | Asus A88XM-A |
| Minne | 16 GB RAM |
| Lydkort | RME HDSP AES |
| Skjermkort | AMD Radeon HD 8670D |
| Lagring | Corsair Force GS |
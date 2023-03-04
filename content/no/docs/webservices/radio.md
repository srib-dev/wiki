---
title: "Lydstrømserver: IceCast2"
linkTitle: "radio.srib.no"
date: 2023-03-04
weight: 1
description: >
  En detaljert forklaring om serveren som sørger for digital lydstrømming av radiosendinger.
---

### Kort forklaring

Dette er en av nettressursene til radioen. Det er en versjon av en standard IceCast2-server som heter [AzuraCast](https://docs.azuracast.com/en/home). Den driftes av friByte, og er [åpen kildekode](https://github.com/AzuraCast/AzuraCast).

Hensikten med denne tjenesten er å generere lydstrømmer som kan deles over nettet. De genereres hovedsakelig for å sende ut på nettet det som er på luften akkurat nå. Det som sendes ut på nettradio er det samme som sendes ut på FM.

### Hvordan fungerer det?

Selv om du lytter på nettradioen på [lytt.srib.no](/docs/webservices/lytt), så er det radio.srib.no som skaper lydstrømmen som du kan lytte på. [Opptaksmaskinen](/docs/computers/serverrom/opptak) bruker 2 programmer som heter [Oddcast](/docs/software/oddcast) og [SoundEmpire](/docs/software/soundempire) til å skape en lydstrøm fra lyden den spiller av på det dedikerte lydkortet sitt. 

Den lydstrømmen sendes til en spesifikk IP-adresse (eller domene), som i vårt tilfelle er radio.srib.no. Radio.srib.no tar imot lydstrømmen, behandler det, sikrer den med SSL og skaper en URL som andre nettsider kan hente lydstrømmen fra. 

I vårt tilfelle sendes en lydstrømm av hva som spilles av på luften til enhver tid (enten [preprod](/docs/computers/serverrom/preprod), [stillealarm](/docs/computers/serverrom/opptak/#stille-alarm), eller direktesendt fra ett av studioene) til radio.srib.no. Den lydstrømmen implementeres da på [lytt.srib.no](/docs/webservices/lytt) gjennom et `iframe`-element. Det `iframe`-elementet har "radio.srib.no/_navn-på-strøm_._filformat_ (eks: radio.srib.no/srib.mp3) som en lydkilde. I tillegg sender vi også en lydstrøm til en ShoutCastV1-server som driftes av DAB-sentralen i Haugaland.

I AzuraCast kan en opprette flere "Mountpoints" for ulike lydstrømmer. I vårt tilfelle har vi én mountpoint for hvert filformat vi strømmer (MP3, AAC, OGG og FLAC). Mountpoint og ".../_navn-på-strøm_._filformat_" er det samme.

### Tips

For at lydstrømmene som sendes fra opptaksmaskinen skal aksepteres av lydstrømserveren, må lydstrømmen oppgi det riktige passordet og brukernavnet i metadataen til lydstrømmen. Denne infoen står skrevet inne på admin-panelet til AzuraCast. 

For å skrive inn dette passordet, bare åpner du "enkoderen", hvilket er hva Oddcast/SoundEmpire kaller et lydstrøm-element, og skriver infoen i de respektive feltene. 
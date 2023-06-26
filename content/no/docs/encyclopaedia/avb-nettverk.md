---
title: "AVB-nettverk"
linkTitle: "AVB-nettverk"
date: 2023-06-19
weight: 2
description: >
  En forklaring av Presonus sitt AVB-nettverk.
---

### Kort forklaring

Et AVB-nettverk er en av Presonus sine oppfinnelser for å skape synkronisering på tvers av ulike lyd-enheter som støtter AVB-nettverksprotokoller. Det er utfordereren til en litt eldre protokoll som kalles "Dante".

Formålet med AVB-nettverket er å sende lyd mellom enheter med en synkronisert klokke mellom alle enhetene. Siden det er nettverksprotokoller, kan kommunikasjonen mellom enheter opprettholdes over lengre distanser på vanlige Ethernet-kabler. 

Dette er en enorm fordel for oss, siden vi har en direkte Ethernet-kobling mellom studioene og serverrommet. AVB-nettverk blir derfor den ryddigste og enkleste løsningen for vår situasjon. 

### Vår oppkobling

Vår oppkobling nå (24.06.23) er slik:

- Det er en [Presonus StudioLive 32SC](/docs/machines/soundprocessing/studiolive) i hvert studio.
- Hver Studiolive 32SC er tilkoblet en [Presonus NSB 8.8](/docs/machines/soundprocessing/nsb8) sceneboks. 
- Hver sceneboks er konfigurert slik at utgangskildene speiler Aux-miksene til miksebordet. 
- Inngangskildene til sceneboksene tar imot lyd fra studio-PC'ene

Siden det er en sceneboks, og ikke en miksekonsoll, kommer den ikke til å krangle med miksekonsollen om å være master i klokke-synkroniseringen.

**NB**: Om du kobler to eller flere miksekonsoller i samme AVB-nettverk, må du definere én av dem til å være master og de andre til å være slave. Da kommer klokke-synkroniseringen mellom dem i nettverket til å stemme. 

### Hvordan koble til en sceneboks

Om du lurer på hvordan å koble til en sceneboks til miksebordet, [kan du se her for en instruksjon](/docs/instructions/sceneboks)

### Kilder
[Presonus StudioLive Series III AVB Networking Guide](https://www.fmicassets.com/Damroot/Original/10015/OM_2779300202_NSB-8.8_StudioLive-Series-III-AVB-Networking-Guide_EN.pdf), sist lest 26.06.23
---
title: "Hvordan installere TurboPlayer"
linkTitle: "Installere TurboPlayer"
date: 2023-01-22
weight: 2
description: >
  En gjennomgang av hvordan en kan installere avviklingsprogrammet TurboPlayer, samt MultiPlayer på en Windows 10 maskin.
---

### Hvorfor vi gjør det

For at vi skal gå direkte på luften, samt ha en automatisert prosess for å sende ut forhåndsproduserte sendinger, må Turboplayer brukes.

### Hvordan vi gjør det

1. Installer DigaSystem
2. Kopier de nyeste versjonene av .exe-filene og .dll-filene til TurboPlayer inn i `C:\DigaSystem`.
3. Kjør installasjonsprogrammet til den nyeste versjonen av MultiPlayer og følg veiviseren.
   
4. I veiviseren:
  - Skift alle lydenhetene fra `WASAPI` til `WaveOut`.
  - Skift Sampling Rate fra 48 KHz til 44.1 KHz
  - Skift Bit-dydbe fra 16 til 24
  - Velg `Turbo Pipe`

  NB: _Forsikre deg om at Sampling rate og Bit-dybde er den samme som hva som lydkortet bruker._ 

5. Til slutt ber veiviseren deg om en lisensnøkkel. Den finner du ved å gå åpne CodeMeter-programmet som kjører i bakgrunnen. Gå til `WebAdmin > MultiPlayer VX Pro Student Radio Bergen Academy License`. Da står lisensnøkkelen under `License Information`.

  NB: _Vi bruker en CmDongle fra Wibu Systems for å verifisere lisensnøkkelen til MultiPlayer. Dette er en fysisk usb-chip som må være tilkoblet maskinen til enhver tid. Iblant, for eksempel ved strømbrudd, skjer noe galt med tilkoblingen. Da bare drar du ut USB-en og stapper han inn igjen i samme høl._

6. Profitt.
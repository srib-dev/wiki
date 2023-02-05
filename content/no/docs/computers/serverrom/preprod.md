---
title: "Hjemmesnekret PC: Preprod"
linkTitle: "Preprod"
date: 2023-02-05
weight: 2
description: >
  En beskrivelse av datamaskinen som avvikler forhåndsproduserte sendinger.
---

### Funksjon

Denne datamaskinen har som eneste funksjon å spille av forhåndsproduserte radiosendinger, slik som sendeplanen tilsier. 

### Sendingsavvikling

Datamaskinen bruker [Turboplayer + Multiplayer](/docs/digasystem/turboplayer/) til å avvikle sendinger. Hvilke sendinger som skal spilles av til enhver tid, er definerte i [DigAIRange](/docs/digasystem/digairange).

På lik måte som på Studiomaskinene, kjøres en hjemmesnekret funksjon hver gang et lydklipp spiller av i Turboplayer. Den hjemmesnekrede funksjonen bruker et PCIe-relékort til å sende et elektrisk signal til Arduinoen som kontrollerer kanalvelgeren. Den funksjonen sier til arduinoen at det nå skal byttes til preprod-kanalen på kanalvelgeren.

På den måten, tar preprod luften hver gang et lyd-element starter i Turboplayer. Så lenge elementer legges inn i sendeplanen riktig, er dette en helt automatisert prosess.

### Spesifikasjoner

| Feature | Value |
| ------- | ----- |
| Prosessor | Intel i5-4670K, 3.40 GHz, 3401 MHz, 4 kjerner, 4 logiske prosessorer |
| Hovedkort | Asus Z87MX-DH3 |
| Minne | 8 GB RAM |
| Lydkort | RME HDSPe AIO |
| Skjermkort | Intel HD Graphics 4600 |
| Lagring | Kingston SV300S37A120G |
| Relékort | AdLink PCI7250 |
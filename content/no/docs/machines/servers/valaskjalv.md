---
title: "Valaskjalv"
linkTitle: "NAS: Valaskjalv"
date: 2023-07-26
weight: 2
description: >
  En beskrivelse av videolagrings-NAS'et 
---

### Kort forklaring

Valaskjalv er et NAS av samme typen som [Kvasir](/docs/machines/servers/kvasir) og [Mimir](/docs/machines/servers/mimir), men har 4 flere brønner for harddisker, hvilket gir et totalt antall brønner på 12. Hver brønn er installert med en 8TB harddisk. Disse harddiskene er konfigurert slik at det gir oss rundt 69 TB (nice) disponibelt for lagring.

Formålet med dette NAS-et er å lagre videoklipp som spilles inn i studio 1 & 2, samt fungere som en backup for Kvasir og Mimir.

### Konfigurering

NAS-et er konfigurert slik at alle 12x8TB HDD'ene er i samme volum, hvilket er et "tynt volum", i to RAID-grupper, som begge er RAID 5. Det betyr at lagringsvolumet kan tåle at maks 1 harddisk feiler. Om 2 eller flere feiler på samme tid, kommer det til å forekomme tap av data. 

På hver produsent-PC så er det installert OBS for å ta opp og strømme video. OBS er innstilt slik at standard lagringsplass for alt av råopptak er en mappe på Valaskjalv. Dette gjelder begge studioene.

### Backup for Kvasir og Mimir

Det har blitt gjort én enveissynkronisering fra både Mimir og Kvasir til Valaskjalv. Men det er ikke en planlagt regelmessig rutine.

### Spesifikasjoner

| Feature | Value |
| ------- | ----- |
| CPU | AnnapurnaLabs Alpine AL324 64-bit ARM® Cortex-A57 4-core 1.7GHz processor |
| CPU Architecture | 64-bit ARM |
| Floating Point Unit | Yes |
| Encryption Engine | Yes |
| System Memory | 4 GB UDIMM DDR4 (1 x 4 GB) |
| Maximum Memory | 16 GB (1 x 16 GB) |
| Memory Slot | 1 x UDIMM DDR4 |
| Flash Memory | 512 MB (Dual boot OS protection) |
| Drive Bay | 12 x 3.5-inch SATA 6Gb/s, 3Gb/s |
| Drive Compatibility | 3.5-inch bays: |
| | 3.5-inch SATA hard disk drives |
| | 2.5-inch SATA hard disk drives |
| | 2.5-inch SATA solid state drives |
| Hot-swappable | Yes |
| M.2 Slot | Optional via a PCIe adapter |
| SSD Cache Acceleration Support | Yes |
| 2.5 Gigabit Ethernet Port (2.5G/1G/100M) | 2 (2.5G/1G/100M/10M) |
| 10 Gigabit Ethernet Port | 2 x 10GbE SFP+ |
| Wake on LAN (WOL) | Yes |
| Jumbo Frame  | Yes |
| PCIe Slot | Slot 1: PCIe Gen 2 x2 |
| USB 3.2 Gen 1 port | 4 |
| Form Factor  | 2U Rackmount |
| LED Indicators | HDD 1-12, Status, LAN, Storage expansion |
| Buttons | Power, Reset |
| Dimensions (HxWxD) | 89 × 482 × 534 mm |
| Weight (Net) | 11.34 kg |
| Weight (Gross) | 17.27 kg |
| Operating Temperature | 0 - 40 °C (32°F - 104°F) |
| Storage Temperature | -20 - 70°C (-4°F - 158°F) |
| Relative Humidity | 5-95% RH non-condensing, wet bulb: 27˚C (80.6˚F) |
| Power Supply Unit | 250W (x2) PSU, 100 - 240V |
| Power Consumption: Operating Mode, Typical | 83.57 W |
| Fan | 2 x 70mm, 12VDC |
| System Warning | Buzzer |
| Max. Number of Concurrent Connections (CIFS) | with Max. Memory 700 |


### Kilder

[QNAP TS-1232PXU-RP Datasheet](https://web.archive.org/web/20230726171911/https://www.qnap.com/en/product/ts-1232pxu-rp/specs/hardware/TS-1232PXU-RP-4G.pdf), sist lest 26.07.23
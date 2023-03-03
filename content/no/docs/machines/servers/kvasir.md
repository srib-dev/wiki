---
title: "Kvasir"
linkTitle: "NAS: Kvasir"
date: 2023-01-02
weight: 2
description: >
  En beskrivelse av NAS-et som heter Kvasir.
---

---
title: "QNAP TS-853BU - Mimir"
linkTitle: "NAS: Mimir"
date: 2023-01-02
weight: 2
description: >
  En beskrivelse av NAS-et som heter Mimir.
---

## Kort forklaring 

Dette er ett av radioens "Network Attached Storage", eller NAS. Den brukes hovedsakelig til å lagre alt på en sentral lagringsplass for [DigaSystem](/docs/digasystem/). Dette er nødvendig for at parameterfilene og lydfilene skal være tilgjengelig for alle arbeidsstasjoner og maskintjenere. 

Dette er det "passive" NAS-et som skal brukes som avløser i de tilfellene Mimir er nede for telling. 

Det er et QNAP NAS med 8 bukter med HDD-er på 4 TB hver. De er konfigurert i RAID5. 

Det er viktig at det kjøres regelmessig RAID-skrubbing og systemfilsjekker for å forsikre seg om at dataen ikke blir korrupt over tid. Dette kan gjøres i web GUI-en til NAS-et. 

## NFS-mounting

NFS står for "Network File Sharing". For at podcast-serveren, som driftes av friByte, skal kunne ha tilgang på podcast-filene, må den mappen NFS-mountes. 

Dette er ikke relevant for Kvasir, men i de tilfellene Mimir er nede for telling, må dette konfigureres i Kvasir også.

## Sikkerhetskopiering

Dette NAS-et er én av 2 NAS som brukes til dette formålet. Det andre NAS-et, [Mimir](/docs/machines/servers/mimir), Kopierer innholdet sitt direkte til Kvasir. Enhver forandring som gjøres på Mimir kopieres over til Kvasir. Dette er en automatisert rutine gjennom "HBS 3 Hybrid Backup Sync" i web GUI-en til Mimir. 

## Spesifikasjoner

| Feature | Value |
| ------- | ----- |
| CPU | Intel Celeron J3455, 1500 MHz, 4 kjerner, 4 tråder |
| CPU Architecture | 64-bit x86 |
| GPU | Intel HD Graphics 500 |
| System Memory | 4 GB DDR3L (2 X 2 GB) |
| Maximum Memory | 8 GB (2 x 4 GB) |
| Memory Slot | 2 x SODIMM DDR3L |
| Flash Memory | 4GB (Dual boot OS protection) |
| Drive Bay | 8 x 3.5-inch SATA 6Gb/s, 3Gb/s |
| Drive Compatibility | 3.5-inch bays: 3.5-inch SATA hard disk drives, 2.5-inch SATA hard disk drives, 2.5-inch SATA solid state drives |
| Hot-swappable | Yes |
| M.2 Slot | Optional via a PCIe adapter |
| SSD Cache Acceleration Support | Drive bays 1 to 2 |
| Gigabit Ethernet Port (RJ45) | 4 |
| Wake on LAN (WOL) | Yes |	
| Jumbo Frame | Yes |	
| PCIe Slot | 1 // Slot 1: PCIe Gen 2 x2 |
| USB 3.2 Gen 1 port | 4 |
| USB 3.2 Gen 2 (10Gbps) Port | Optional via a PCIe adapter |
| HDMI Output | 1, HDMI 1.4b (up to 3840 x 2160 @ 30Hz) |
| Form Factor | 2U Rackmount |
| LED Indicators | HDD 1-8, Status, LAN, Expansion, Power |
| Buttons | Power, Reset |
| Dimensions (HxWxD) | 3.5 × 18.98 × 21.02 inch |
| Weight (Net) | 22.09 lbs |
| Weight (Gross) | 30.09 lbs |
| Operating Temperature | 0 - 40 °C (32°F - 104°F) |
| Storage Temperature | -20 - 70°C (-4°F - 158°F) |
| Relative Humidity | 5-95% RH non-condensing, wet bulb: 27˚C (80.6˚F) |
| Power Supply Unit | ATX 250W (x1), Input: 100V-240V ~ / 5A-2.5A, 50Hz-60Hz |
| Power Consumption: HDD Sleep Mode | 30.9 W |
| Power Consumption: Operating Mode, Typical | 52.1 W |
| Fan | 2 x 70mm, 12VDC |
| System Warning | Buzzer |
| Max. Number of Concurrent Connections (CIFS) - with Max. Memory | 1500 | 

## Kilder

[QNAP TS-853BU Hardware Specifications](https://www.qnap.com/en-us/product/ts-853bu/specs/hardware), sist lest 03.03.23
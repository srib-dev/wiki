---
title: "Hjemmesnekret PC: Studiomaskin"
linkTitle: "Studiomaskin"
date: 2023-03-03
weight: 2
description: >
  En beskrivelse av datamaskinen som brukes i studio for innspilling/avspilling.
---

## Kort forklaring 

Studiomaskinene er skreddersydde datamaskiner. På mange måter er de lik arbeidsstasjonene, men på mange måter er de også ulike.

Hvor de er like er at de er installert med Windows 10 og DigaSystem. 

Hvor de er ulike er at de er installert med [Turboplayer + Multiplayer](/docs/digasystem/turboplayer/), har et dedikert PCIe-lydkort for å håndtere lydavspilling og opptak, samt et PCIe-relékort for å kontrolle stillealarm-boksen.

Studiomaskinen bruker 2 KVM-bokser til å videresende Tastatur/datamus-innfôr inn til maskinen, samt sende videosignal fra maskinen til 2 skjermer (én for hver KVM) som står i studio.

Dette er tilfellet for studiomaskinen i begge studioene. 

## Programvare

| Navn | Kort Forklaring |
| ---- | ---------- |
| DigaSystem | Databasehåndteringsprogram som kommer med ulike moduler for media-redigering |
| TurboPlayer | Program for avvikling av lydfiler på luften i forhåndslaget sendeplan |
| Multiplayer | Kommer med Turboplayer. Bruker lydkortet til å spille av lydfilene på ordre fra Turboplayer. |
| WinHotKey | Program for å programmere inn makroer slik at en kan bruke tastaturet til å utføre ulike kommandoer raskt. |
| RealVNC Server | Fjernstyringsprogram som brukes av produsenten for å se hva programlederen gjør. |
| Universal Control | Kontrollpanel for [Presonus-miksebordet](/docs/machines/soundprocessing/studiolive) |
| Audacity | Lydopptaksprogram |

## Komponenter

| Type | Navn |
| ---- | ---- |
| Lydkort | Marian Seraph 8+ |
| Relékort | AdLink PCI7250 | 
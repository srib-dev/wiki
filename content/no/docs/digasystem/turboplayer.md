---
title: "TurboPlayer"
linkTitle: "TurboPlayer"
date: 2023-01-10
weight: 2
description: >
  En beskrivelse av TurboPlayer.
---

TurboPlayer er programmet som brukes til avvikling av sendinger. Altså, dette er programmet som henter laster inn lydklipp, slik som de er listet i sendeplanen. Turboplayer trenger derfor tilkobling med BCS for å kunne hente ut sendeplanen, samt tilgang til NAS-et for å hente ut lydklipp.

TurboPlayer er helt avhengig av et program som heter MultiPlayer for å kunne starte. MultiPlayer er et program som spiller av lydklippene den har hentet fra NAS-et. 

TurboPlayer har veldig høy kapasitet for skreddersying. Men kommer med en god del innebygde moduler som kan rigges opp i brukerpanelet. 

TurboPlayer bruker et relékort, som heter AdLink PCI-7250. Ved å bruke dette kortet, kan TurboPlayer sende kommandoer til arduinoboksen som kontrollerer kanalvelgeren. Så når en trykker på "Ta luften"-knappen i brukerpanelet, eller kaller på "OnAir01"-funksjonen på noe vis, sendes en kommando om å ta luften til arduinoboksen, som deretter bytter kanal på kanalvelgeren. Dette er for øyeblikket tilfellet for alle installasjoner av TurboPlayer. 
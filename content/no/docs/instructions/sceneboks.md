---
title: "Hvordan koble en sceneboks til miksebordet"
linkTitle: "Sceneboks-tilkobling"
date: 2023-06-26
weight: 2
description: >
  En gjennomgang av hvordan man kobler en Presonus NSB 8.8 til en Presonus StudioLive 32SC gjennom et AVB-nettverk.
---

Gjør følgende: 

1. Sørg for at både miksekonsollen og sceneboksen er installert med nyeste fastvare-versjon.
2. Koble ethernet-porten `Audio Networking` på miksebordet til ethernet-porten `A` på sceneboksen. (Ethernet-porten `B` på sceneboksen er for å seriekoble scenebokser)

På konsollen:

3. Trykk på `Home` -> `Audio Routing` -> `Stagebox Setup`
4. Trykk på sceneboksen i listen av tilgjengelige enheter
5. Trykk på `Preamp Control` og velg miksekonsollen.
6. Trykk på `AVB Output Sends` og velg faderkanalene du har lyst til å sende til utgangskildene på sceneboksen. (I vårt tilfelle er dette 41-48 siden dette korresponderer med de 8 første aux-miksene)
7. Når du er ferdig, trykk `Apply`. Nå har du konfigurert å sende lyd til sceneboksen.
8. Naviger til `AVB Inputs`-fanen.
9. Velg den aktuelle faderkanalen på venstre siden av skjermen.
10. Velg deretter den aktuelle inngangskilden på sceneboksen på høyre side av skjermen. 
11. Gjør dette for hver faderkanal. Når du er ferdig, har du koblet inngangskildene på sceneboksen til faderkanalene på miksebordet.
12. Naviger deretter til `Home` -> `Audio Routing` -> `Digital Patching`. Her velger du hvor faderkanalen skal hente signal fra.
13. På venstresiden av skjermen, velg de de aktuelle faderkanalene.
14. Trykk på nettverks-ikonet. Nå har du satt faderkanalen til å hente lyd fra AVB-nettverket.
15. Til slutt, må du trykke på den fysiske `Input`-knappen på hver av de aktuelle faderkanalene og aktivere nettverkstilkoblingen ved å trykke på `Network`. Når dette er gjort, skal faderkanalen nå ta imot lyd fra sceneboksen sine inngangskilder.


I [Universal Control](/docs/software/uc)

3. Gå inn i Universal Control og velg den aktuelle miksekonsollen.
4. Gå til `Network`-fanen, og velg `Stagebox setup`.
5. Velg sceneboksen i listen med tilgjengelige enheter.
6. Velg deretter `Preamp control` og velg den aktuelle mikseren.
7. Velg deretter `AVB Output Sends` og velge de aktuelle faderkanalene. (41-48 er de første 8 aux-miksene på mikseren)
8. Trykk `Apply`
9. Trykk på `AVB Inputs`-fanen
10. Velg de aktuelle faderkanalene, og tildel dem de aktuelle sceneboks-inngangene. 
11. Naviger deretter til `Digital Patching` -> `Input Source` -> `AVB`
12. Endre deretter de aktuelle faderkanalene til å ha nettverksikonet. Når dette er gjort, skal faderkanalen nå ta imot lyd fra sceneboksen sine inngangskilder.

### Kilder
[StudioLive Series III AVB Networking Guide - 4: Configuring Your AVB Network](https://www.fmicassets.com/Damroot/Original/10015/OM_2779300202_NSB-8.8_StudioLive-Series-III-AVB-Networking-Guide_EN.pdf#StudioLive%20Series%20III%20AVB%20Networking%20Guide%20V2_EN.indd%3A.271270%3A19881), sist lest 26.06.23
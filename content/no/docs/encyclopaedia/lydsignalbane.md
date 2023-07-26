---
title: "Lydsignalbane"
linkTitle: "Lydsignalbane"
date: 2023-06-18
weight: 2
description: >
  En beskrivelse av signalbanen til lyden. Hvilken retning lyden går og hvilke maskiner den går igjennom.
---

### Kort forklaring



### Studio 1 & 2

Den letteste måten å forstå signalbanen i studioene, er å se et diagram. Tilfeldigvis har jeg laget et diagram av det nøyaktig for denne wikien. 

![Fysisk oppkobling i begge studioene](/img/lydsignalbane/studio.png)

Dette diagrammet er gjeldende for både studio 1 og studio 2. 

I sentrum av studio er miksebordet, [Presonus StudioLive 32 SC](/docs/machines/soundprocessing/studiolive). Dette er hva de følgende forklaringene tar utgangspunkt i. 

#### Konfigurering

Alle Aux-mikser har muligheten til å settes i en konfigurasjon hvor de enten operer uavhengig eller avhengig av nivået på faderen til **Main**. Det kalles *pre-fade* eller *post-fade*. 

Ved å sette Aux-miks (1-2) og Aux-miks (3-4) i *post-fade* gjør vi begge miksene avhengig av **Main**. Det betyr det at inne i miksene kan f.eks. alle faderne stå oppe, men det vil ikke sendes ut lyd før faderne til **Main** er oppe. Så alle justeringer man gjør i **Main**, som volumkontroll, demping, EQ, osv, sendes til begge miksene samtidig. 

På denne måten, selv om utgangene er fysisk koblet til å gå forskjellige steder, kan vi ta opp lyd lokalt på studio-pc'en samtidig som vi styrer lyden mens vi er på luften. Signalene i begge fysiske oppkoblede retninger får samme lydnivåer. 

#### Lyd inn

Fire mikrofoner, [Røde Podmic](/docs/machines/microphones/rode-podmic), er koblet til miksebordet. Det er åpenbart hva de er der for. Disse mikrofonene har ganske lavt volum på opptak. Derfor bruker vi en [Triton FetHead](/docs/machines/soundprocessing/triton-fethead) for å forsterke mikrofon-signalet med rundt 27dB ekstra. 

Utenom det kommer det lyd inn i miksebordet gjennom en [AVB-nettverkstilkobling](/docs/encyclopaedia/avb-nettverk). Miksebordet er koblet til gjennom AVB-nettverksprotokoller til en sceneboks, [Presonus NSB 8.8](/docs/machines/soundprocessing/nsb8). Denne sceneboksen fungerer som en utvidelse av miksebordet. Miksebordet mottar lyd fra studio-pc'en sine lydkanaler gjennom sceneboksen. 

#### Lyd ut

Mest åpenbart, går det lyd ut av miksebordet til høyttalerne som står i studio. Disse høyttalerne henger på veggen og peker rett mot mikrofonene. Det er derfor anbefalt å ikke ha høyttalerne på samtidig som mikrofonene, da dette fører til en fôringsløkke. 

I tillegg går lyden ut til en øreklaff-forsterker, [Behringer HA6000](/docs/machines/soundprocessing/ha6000), som fordeler lyden ut til fem øreklaffer; fire [Presonus HD7](/docs/machines/headphones/presonus-hd7) i studio og én til produsenten. Samtidig er også en annen øreklaff-forsterker, [Behringer HA8000 V2](/docs/machines/soundprocessing/), koblet til. Den mottar lyd fra et mindre miksebord i produsentboden. 

Når produsenten snakker, ender det først opp i HA8000 og fordeles utover alle øreklaff-kanalene på den enheten. Deretter sendes lyden fra hver øreklaff-kanal på HA8000 til hver Aux-inngang på hver øreklaff-kanal på HA6000. Dette er på grunn av en funksjon på HA6000, hvor en kan styre volum mellom "main input" og "aux input" med en vriknapp. På den måten kan programleder bestemme hvem som skal høre produsenten. 

Miksebordet sender også lyd ut gjennom AVB-nettverkstilkoblingen. Sceneboksen har blitt programmert slik at de 8 utgangskildene på sceneboksen, speiler de 8 første aux-miksene på miksebordet. Aux-miks 1+2 er fysisk koblet opp, gjennom sceneboksen, mot studio-pc'en sitt analoge PCIe-lydkort, [Marian Seraph 8+](/docs/computers/components/marian-seraph8). Aux-miks 3+4 er fysisk koblet opp, gjennom sceneboksen, mot kanalvelgeren. Aux-miks 1+2 er for å ta opp innspillingen, mens aux-miks 3+4 sender lyden direkte ut på luften. 

#### Produsentboden

I produsentboden er det ganske enkelt. Det er ett [Behringer Xenyx Q502USB](/docs/machines/soundprocessing/xenyx502), med én mikrofon, [Shure SM58](/docs/machines/microphones/shure-sm58), koblet til. Miksebordet mottar lyd på 2-track inngangskilden fra HA6000-forsterkeren, hvilket blir sendt til produsenten sine øreklaffer. 

### Serverrom

Jeg lagde, faktisk helt tilfeldig, enda et diagram av serverrommet.

![Fysisk oppkobling i serverrommet](/img/lydsignalbane/serverrom.png)

Det er selvfølgelig mye mer inne på serverrommet, men det som er i fokus her er enhetene som lyden passerer gjennom. 

Som sagt, er utgangskildene på sceneboksen en speiling av aux-miksene på miksebordet. Aux-miks 1+2 går til studio-PC'en, mens aux-miks 3+4 går til kanalvelgeren. Inngangskildene på sceneboksen tar imot lyd fra tre stereo kanaler fra studio-pc'en sitt PCIe-lydkort; turboplayer kanal 1 (1+2), turboplayer kanal 2 (3+4) og vanlig PC-lyd (5+6). Disse lydinngangene er programmert til å være faderkanaler på miksebordet. Denne oppkoblingen gjelder for begge studioene.

Med [preprod](/docs/computers/serverrom/preprod) menes en hjemmesnekret pc, installert med [Turboplayer](/docs/digasystem/turboplayer), som kontinuerlig spiller av forhåndsproduserte sendinger gjennom turboplayer. Den sender AES-lyd til en egen AES-kanal på kanalvelgeren.

Opptaks-PC'en bedrar navnet sitt litt og er ansvarlig for å spille av [stillealarmen](/docs/encyclopaedia/stillealarm). Vår stillealarm består av en mappe med lydfiler som spilles av i VLC i tilfeldig rekkefølge og i en evig løkke. Slik som preprod sender opptaks-PC'en AES-lyd til en egen AES-kanal på kanalvelgeren.

Det gjør at vi har følgende lydkilder for kanalvelgeren:

- Studio 1
- Studio 2
- Preprod
- Stillealarm

Bare én av disse kanalene kan være den aktive kanalen til enhver tid. Dette styres av [Arduino-maskinen](/docs/machines/custom/arduino). Uansett hvilken kanal som er aktiv på kanalvelgeren, så sendes den lyden ut til 2 mottakere; Opptaks-PC'en og FM-utsenderen. 

Opptaks-PC'en mottar all lyd som sendes ut på luften, deler det opp i lydfiler som korresponderer med sendeplanen og lagrer det i [DBM](/docs/digasystem/dbm). Samtidig tar den det samme lydsignalet og sender det det ut til både en IceCast2-server på [`radio.srib.no`](/docs/webservices/radio) og DAB-sentralen i Haugaland. Til dette brukes programvare som heter [Oddcast V3](/docs/software/oddcast) og [SoundEmpire](/docs/software/soundempire).

Fra `radio.srib.no` videresendes lyden til [`lytt.srib.no`](/docs/webservices/lytt), hvilket er den som hovedsiden, [`srib.no`](/docs/webservices/srib) lenker til.

Før lydsignalet sendes til FM-utsenderen, sendes det først igjennom en [BW Broadcast RDS2](/docs/machines/soundprocessing/rds2) og deretter igjennom en [BW Broadcast DPSX-FM](/docs/machines/soundprocessing/dspx-fm). DSPX-FM har en del funksjoner som kan anvendes lydsignalet før det sendes ut på FM. For øyeblikket anvender vi ingen andre funksjoner enn å bare øke volumet med rundt 18dB. 

Når det kommer frem til FM-utsenderen, en [Electrolink Orchestra](/docs/machines/broadcasting/electrolink), moduleres signalet til å ha de riktige egenskapene som trengs for at lydsignalet skal kunne kombineres med frekvensen. I tillegg kan en også styre hvilke frekvenser lydsignalet skal kombineres med. Deretter, sendes det videre til en FM-kombinator som er ansvarlig for å faktisk kombinere lydsignalet med frekvensen. Etter det, sendes lydsignalet videre til en antenne som står festet på taket til Studentsenteret. Denne antennen er den eneste FM-antennen som brukes av Studentradioen i dag (19.06.2023). 


### Hele bildet

For referanse legger jeg ved dette diagrammet av hele lydsignalbanen.

![Hele lydsignalbanen](/img/lydsignalbane/lydsignalbane.png)

### Innspillingsrom

Innspillingsrommet (hvilket er det varmeste innspillingsrommet i universet) er helt separert fra resten lydsignalet. Dette er et rom som både fungerer som et ekstra studio og som et rom for å lage jingler, musikk og lydklipp. 

![Fysisk oppkobling i innspillingsrommet](/img/lydsignalbane/innspillingsrom.png)

Det er et ganske standard opplegg. Miksebordet, en [Behringer Xenyx 1002b](/docs/machines/soundprocessing/xenyx1002b), er tilkoblet 3 mikrofoner, [Se Electronics X1S](/docs/machines/microphones/se-x1). Main output går fra miksebordet inn i kompressoren, en [Drawmer DL441 Quad Auto Compressor](/docs/machines/soundprocessing/dl441), mens phones output går til øreklaff-forsterkeren, en [Behringer HA8000](/docs/machines/soundprocessing/ha8000v2). 

Fra kompressoren går lyden til USB-lydkortet, en [Focusrite Scarlett 2i2](/docs/machines/soundprocessing/scarlett2i2) som transformerer lyden fra analogt til digital, og videresender det til innspillings-PC'en. Fra USB-lydkortet sendes også lyden til 2 høyttalere og et par øreklaffer. 

Det er også koblet til et piano, [SubZero ControlKey 49s](/docs/machines/instruments/controlkey49s), for å kunne spille inn melodier i [Reaper](/docs/software/reaper). 
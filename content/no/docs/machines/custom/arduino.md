---
title: "Stillealarm: Arduino"
linkTitle: "Arduino"
date: 2023-06-18
weight: 2
description: >
  En beskrivelse av arduino-kortet, hvordan den er koblet opp og hvordan en kan laste opp ny kode.
---

### Kort forklaring

Vi bruker en litt eldre Arduino til å fungere som stillealarm. Den er hjemmesnekret av en tidligere teknisk sjef i radioen. Formålet med arduinoen er at den skal kjøre koden som fungerer som logikken til stillealarmen. Den er koblet direkte opp mot [kanalvelgeren](/docs/machines/soundprocessing/adms44-22). Den følger med på lydnivåene på den aktive kanalen. Om det er stille nok på kanalen i rundt 10 sekunder eller mer, skifter den over på stillealarm-kanalen. 

I tillegg er den koblet opp mot relékortene i PC-ene til alle [Turboplayer](/docs/digasystem/turboplayer)-instansene. Det er på denne måten medarbeidere i studio kan ta luften fra studio gjennom Turboplayer. Det samme gjelder `OnAir01`-funksjonen som legges på lyd-elementer i [DigAIRange](/docs/digasystem/digairange). 

### Oppkobling

Når en ser på Arduinoen, ser det ut som en stor bolle med spaghetti (uten saus 😢) som en viss tidligere teknisk sjef har kastet i veggen på serverrommet. Nevner ingen navn. 

Det kan derfor være litt vanskelig å se hva som går til hva. så her er et diagram av hvordan det logisk er koblet opp.

![Fysisk oppkobling mellom Turboplayer-instansene, arudionen og kanalvelgeren](/docs/machines/custom/arduino-oppkobling.png)

I [Turboplayer](/docs/digasystem/turboplayer) er det mulig å knytte funksjoner en lager opp mot spesifikke knapper i brukergrensesnittet. Hvilket er tilfellet med "Ta luften"-knappen.

Funksjonen tilknyttet "Ta luften"-knappen heter `OnAir01`. Den funksjonen er laget slik at den sender ut strøm på spesifikke kanaler på relékortet i maskinen. De spesifikke kanalene korresponderer med spesifikke porter på utgangskilden til kortet. Strømmen går derfor inn i spesifikke kobbertråder i ledningen som kobles til utgangskilden.

De spesifikke kobbertrådene er koblet inn i spesifikke porter på arduino-kortet. Når disse portene mottar strøm, tolkes det kode som kjører på arduino-kortet. Avhengig av hvilken port som mottar strøm, sender arduino-kortet strøm ut av spesifikke porter på arduino-kortet og inn i kanalvelgeren.

Arduino-kortet er koblet opp mot inngangskilder på kanalvelgeren som kalles "General Purpose Parallell Input" (PIP). Strømmen som sendes av arduino-kortet, som følge av mottak av strøm fra relékortet, mottas av kanalvelgeren gjennom disse inngangskildene. Hver PIP er tilknyttet en spesifikk knapp på kanalvelgeren. Så en kan si at hvis strøm sendes inn i en PIP, så er det som å faktisk trykke på knappen. 

Arduino-kortet mottar også lydsignaler fra kanalvelgeren. Lydsignalet kommer fra en vanlig AES output gjennom en kabel som har blitt splittet opp i ulike kobbertråder. Koden som kjører på arduino-kortet måler verdiene til lydsignalet og følger med om det kommer under visse verdier. Om lydsignalet går under en viss verdigrense, sender arduino-kortet strøm inn i PIP-en som korresponderer med stillealarm-knappen. 

### Hvordan laste opp kode

NB: Såvidt jeg vet er det **ikke mulig å hente ut kode** som allerede kjører på Arduinoen.

For å laste opp kode må du gjøre følgende:

1. Installer [Arduino IDE](https://www.arduino.cc/en/software) på din egen maskin.
2. Koble din egen maskin til arduino-kortet med USB Type-B.
3. Åpne arduino IDE programmet.
3. Velg riktig "Board" og "Port" under "Tools"-fanen.
3. Skriv koden og trykk "verify"-knappen
4. Trykk "Upload".

**Når du trykker "Upload", overskriver du koden som allerede er der.**

### Kilder

[Upload a sketch in Arduino IDE](https://support.arduino.cc/hc/en-us/articles/4733418441116-Upload-a-sketch-in-Arduino-IDE), sist lest 18.06.23

[Broadcast Tools ADMS 44.22 Installation And Operation Manual - 1.7 External Control](https://www.manualslib.com/manual/748995/Broadcast-Tools-Adms-44-22.html?page=10#manual), sist lest 18.06.2023
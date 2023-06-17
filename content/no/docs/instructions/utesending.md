---
title: "Hvordan rigge til utesending"
linkTitle: "Utesending"
date: 2023-06-17
weight: 2
description: >
  En gjennomgang av hvordan en rigger opp til utesending.
---

### Hvorfor vi gjør det

Fordi det er gøy :)

### Utstyrsliste

Dette er et forslag til utstyrsliste for en standard utesending:

- Lydmikser
- 4 mikrofoner
- 2 høyttalere
- Utesending-PC
- USB-lydkort
- Produsent-PC
- 6x 30m XLR-kabler
- 2x 1m 1/4'' TRS-kabler
- (valgfritt) Ruter for mobilt bredbånd

### Rigge opp utstyr

Her følger en bare vanlig konvensjon for å rigge opp til en innspilling. Det er bare et eksempel på hensiktsmessig rekkefølge.

1. Pakk ut alt utstyr som skal brukes
2. Velg deg en plass for lydmikseren. 
    - Helst foran høyttalerene, men bak publikum. 
3. Still opp høyttalerne
4. Velg en plass hvor mikrofonene skal stå. 
    - Det må være bak høyttalerne for å unngå en fôringsløkke.
5. Trekk aktuelle kabler fra lydmikseren til scenen
6. Koble alle mikrofoner og høyttalere opp mot lydmikseren. 
    - God praksis er at plasseringen av mikrofonene stemmer med rekkefølgen av faderkanalene. feks. Faderkanal 1 som er lengst til venstre er koblet mot mikrofon en som er lengst til venstre på scenen. 
    - Høyttalerne burde være koblet opp mot "Main out" eller "Auxiliary out".
7. Koble opptaksenheten til lydmikseren. 
    - Den burde kobles opp mot "Main out" eller "Auxiliary out".
8. Test lyden. 
    - På dette tidspunktet burde det være god tid igjen til starten av sending. La produsenten koble til PC-en sin for å spille av musikk kontinuerlig. Om det ikke kommer lyd inn i opptaksenheten og/eller ut på høyttaleren, er det åpenbart noe galt.
    - Få alle innlederne opp på scenen, i den rekkefølgen de skal sitte, og test lyden én og én. Du må gjerne equalize lyden slik du vil.
    - Til slutt test lyden når de alle snakker samtidig, og justér volum slik at én av dem ikke snakker høyere/lavere enn de andre.
    - Om du bruker en PC som opptaksenhet, test også om lyden dukker opp i opptaksprogrammet på PC-en. Et typisk problem her kan være at USB-lydkortet ikke er valgt som inngangsenhet i opptaksprogrammet

#### Direktesendinger

Om det er en direktesending må du gjøre følgende for at lydsignalet skal komme på luften. Det er med forbeholdet at PC-en mottar lydsignalet.

1. Åpne oddcast på utesending-PC'en
    - Sjekk alle detaljene på "codec"-en og dobbeltsjekk at de stemmer.
    - Et typisk problem er at relay-passord ikke er riktig, eller at mountpoint er feil.
2. Åpne RealVNC og logg inn med preprod-brukeren.
3. Åpne VNC-tilkoblingen til Preprod-maskinen
4. Start programmet som heter `openStreamUtesending`.
    - Dette programmet åpner en VLC-strøm som lytter på en spesfikk IceCast2-URL. Hvilket er URL-en som Oddcast på utesending-PC'en kringkaster til. 
    - Når det er startet, spiller den umiddelbart av hva den mottar. Den lyden spilles samtidig som programmet i TurboPlayer.
5. Start kringkasting fra Oddcast.
    - Start kringkastingen et par sekunder før trailerskillet er ferdig.
    - Akkurat nå trailerskillet er ferdig, trykk på "ta luften" i Turboplayer på preprod.
6. Feilsøk.
    - Om det er stille på luften, selv om du kringkaster, må du feilsøke. Ikke få panikk. Bare la stillealarmen ta over og begynn å feilsøk.
    - Be produsenten spille av musikk kontinuerlig mens du feilsøker, for å forsikre deg om at du alltid har signal. 
    - Når du mener du har fikset problemet, trykk på "ta luften" igjen og hør etter på lytt.srib.no om lyden kommer igjennom. 

### Radiovettregler

1. Sørg for at det er strømkilder tilgjengelig hvor dere skal gjøre innspillingen.
2. **Sjekk været på forhånd!**
3. Ha et møte med programmet som skal ha utesending og få kontroll på følgende:
  - Hvor og når?
  - Hvor mange skal snakke samtidig?
  - Skal det være spørsmål fra tilskuere?
  - Skal det spilles musikk/jingler under sendingen?
  - Hvor lenge varer det?
  - Er det andre spesielle behov? som f.eks. instrumenter som skal tas opp?
  - Skal det være direkte på luften?

  Basert på disse svarene du får, må du planlegge hva som trengs til sendingen og hvor lang tid opprigget tar.

4. Du burde alltid ha i hvert fall 1 time disponibelt for å rigge opp før sendingen starter. Dette innebærer også å teste lyden. 
   
  **Alltid beregn i hvert fall 1.5 timer til opprigget første dagen på FiB**. 
   
5. Avtal med stedet hvor dere skal være, hva de kan levere av utstyr. Da slipper du å drasse med deg absolutt hele lagerrommet. 

6. **Vær 3000% sikker på at det tas opptak av sendingen.** Sjekk regelmessig om Audacity tar fremdeles tar opp, eller om dere fremdeles er på luften.
   
7. Ha en medhelper med deg. Det kommer til å lette på arbeidsmengden og hjelpe på kjedsomheten i dødtid.  

### Tips til produsenten

1. Planlegg alle sangene/jinglene som skal spilles under sendingen. Ha et par sanger til overs for om det blir problemer med utstyret.
2. Last ned sangene på forhånd slik at du har dem lokalt på din egen maskin. Da fjerner du et uro-element for den som styrer lyden.
3. Ha god kommunikasjon med den som styrer lyden om når stikket er ferdig og sang begynner.
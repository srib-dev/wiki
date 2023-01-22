---
title: "Hvordan å installere DigaSystem"
linkTitle: "Installere Digas"
date: 2023-01-22
weight: 2
description: >
  En gjennomgang av hvordan en kan installere databasesystemet DBM og tilhørende moduler på en Windows 10 maskin.
---

### Hvorfor vi gjør det

DBM og alle de tilhørende modulene og funksjonene some er tilgjengelig gjennom DBM, er det viktigste redskapet for at radioen skal kunne produsere innhold. 

### Hvordan vi gjør det

NB: _Sørg for at du har nyeste versjon av DigaSystem fra leverandøren vår. For øyeblikket er rutinen å sende dem et ebrev og be om nyeste versjon, hvilket burde gjøres årlig._

1. Kjør installasjonsprogrammet til DBM og følg veiviseren. 
2. Installer ODBC Connector 3.51 (32-bit)
3. Kjør installasjonsprogrammet til MultiTrack og følg veiviseren.
4. Kopier `C:\programfiles(x86)\DigaSystem` til `C:\DigaSystem`. Du trenger ikke den originale mappen.
5. Åpne admin-panelet i `C:\DigaSystem`-mappen.
6. Åpne `Parameterfiler`-fanen, oppe til høyre.
7. Legg inn parameterfilene for "Global", "Computer", "User", "Rights". 
   
  Du må skrive inn korrekt path til hver fil/mappe. De er som følger:
  
  | Type | Path |
  | ---- | ---- |
  | Global | `mimir\nas\parameterfiler\digas\DIGAS.PAR` |
  | Computer | `mimir\nas\parameterfiler\digas\*.par` |
  | User | `mimir\nas\parameterfiler\digas\User` |
  | Rights |  `mimir\nas\parameterfiler\digas\RIGHTS.PAR` |

  NB: _Om en parameterfil ikke eksisterer for "Computer", kan du bare kopiere en som tilhører en annen datamaskin._

  Når det er gjort, lagrer du og lukker vinduet. 

8. Åpne `Database > Manage Data Sources` og trykk på `System DSN`.
9. Legg til en ny "Database Connection" med ODBC 3.51 Connector som driver.
10. Fyll ut tilkoblingen med følgende informasjon:

  | Parameter | Verdi | Forklaring |
  | --------- | ----- | ---------- |
  | Data Source Name | SRDB | Arbitrært navn på tilkoblingen |
  | Description | Srib Database | Kort beskrivelse av tilkoblingen |
  | TCP/IP Server | XXX.XX.X.XX | IP-addressen til Databasen. Kontakt friByte om hvilken som gjelder. |
  | Port | XXXX | Port som er tilgjengelig for tilkobling. Kontakt friByte om konfigurasjonen. |
  | User | XXXX | SQL-brukernavn |
  | Password | XXXX | SQL-passord |
  | Database | digas | Hvilken tabell du skal hente/lagre informasjon fra/i |

  NB: _Trykk "Test" for å teste tilkoblingen. Naturligvis, om den ikke er suksessfull, er noe galt i informasjonen til tilkoblingen_

11. Naviger til `Local Settings > Programs`. 
12. Trykker du på `Programs` får du opp en liste med programmer og en tihørende path. Du må fjerne "_" fra navnet på programmet du vil skal være tilgjengelig i DBM. Samt sørge for at path-en til .exe-filen er korrekt.
13. Lukk admin-panelet og åpne `C:\DigaSystem`.
14. Nå kommer den kjedelige delen... Du må nå finne alle de nyeste filversjonene til hver .dll-fil, samt hver .exe-fil i DigaSystem-mappen, kopiere dem over til `C:\DigaSystem` og erstatte de gjeldende filene. Du burde kunne finne disse filene i NAS-et under `...\nas\teknisk\digasystem\alle filversjoner`. NB: husk `regsvr32.exe`
15. Når dette er gjort, må du registrere alle .ocx-filene i Windows-registeret. Dette gjør du ved å merke alle .ocx-filene i `C:\DigaSystem`, navigere ned til `regsvr32.exe`, holde musen over filen og slippe dem på filen. 
16. Profitt.
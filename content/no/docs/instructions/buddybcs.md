---
title: "Hvordan å konfigurere Buddy BCS for Master BCS"
linkTitle: "Konfigurere BCS"
date: 2023-01-10
weight: 2
description: >
  En gjennomgang av hvordan en kan konfigurere en buddy BCS.
---

### Hvorfor vi gjør dette

Siden hele avviklingen av sendinger ut på luften er så avhengig av BCS som den er, er det nødvendig å ha en avløser i nødsituasjoner. Hvis ikke, er det ikke mulig å drive radio i det hele tatt.

### Hvordan vi gjør dette

1. Installer DigaSystem som vanlig.
2. Dra og slipp .exe-filene til BCS inn i `C:\DigaSystem`.
3. NB: Alltid kjør BCS i admin-modus
4. Åpne admin-panelet (admin.exe)
5. Navigér til `Local Settings/BroadcastServer/Default/Buddy` og endre følgende verdier:

   - Address = Master PC-en sin IP
   - IAmPreferredMaster = FALSE
   - Password = admin-passordet
   - Port = 1000
   - TreePath = `\\<Master PC sin IP>\Digas\SeplServTree`
  
6. Deretter gå over til Master-installasjonen og endre følgende verdier:

   - Address = Buddy PC-en sin IP
   - IAmPreferredMaster = TRUE
   - Password = admin-passordet
   - Port = 1000
   - TreePath = `\\<Buddy PC sin IP>\Digas\SeplServTree`
 
NB: _`TreePath` er hvor Buddy-en sin lokale kopi av XML-databasen er lagret. Det kan være hvor som helst, så lenge riktig path er skrevet inn her._

Etter dette skal det være en tilkobling mellom Master og Buddy. Som sagt er det veldig viktig at **begge** disse installasjonene kjører i admin-modus, slik at de har skrive-rettigheter på sin respektive maskin. 

Om Master kjører i admin-modus, mens Buddy ikke kjører i admin-modus, kommer ikke XML-databasen til å synkronisere seg skikkelig. Ingenting nytt blir da skrivd inn i Buddy sin XML-database.
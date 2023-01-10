---
title: "DigAIRange"
linkTitle: "DigAIRange"
date: 2023-01-10
weight: 2
description: >
  En overskrift av DigAIRange.
---

DigAIRange er en modul av DBM som brukes til å forvalte aktive sendeplaner. Den trenger kommunikasjon med BCS for at endringene en gjør skal manifestere seg i XML-databasen som ligger lagret på maskinen som BCS kjører på. Om kommunikasjonen er brutt, kan ikke DigAIRange-serveren en går inn på for å lage sendeplanen åpnes. 

Om BCS ikke kjører i Administrator modus, kan du fremdeles lage sendeplanen, men BCS skriver det ikke til sin lokale disk. Dette er fordi programmet da ikke har rettighetene til å redigere lokale filer.

I DigAIRange kan en:

- Lage/slette/redigere sendeplaner
- Lage jingle-lister for ulike programmer.
- Planlegge automatisk kryssfalming mellom sendeplan-elementer
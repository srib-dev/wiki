---
title: "Hvordan legge inn sendeplan for automatiske opptak"
linkTitle: "Auto-opptak"
date: 2023-01-22
weight: 2
description: >
  En gjennomgang av hvordan en kan endre XML-filene for å oppdatere hvilke programmer som skal tas opp automatisk, samt til hvilke tider.
---

### Hvorfor vi gjør det

Hvert semester er det en ny sendeplan. Den sendeplanen innebærer programmer som er direkte på luften. Disse programmene er avhengige av at automatisk opptak fungerer for at de skal ha et opptak å redigere etter sending. 

I tillegg er vi også lovpålagt å ta opp alt vi sender ut på luften.

### Hvordan vi gjør det

Når du først starter MultiCoder, ber programmet deg velge en lydenhet. På den listen er alle lydenhetene nummerert på formatet "DeviceIDXX", hvor XX er et tall. 

NB: _Denne DeviceID-en er ikke permanent. Den kan endre seg i fremtiden._

Alle disse filene ligger under `C:/DigaSystem/Files/DeviceIDXX/BookingLists`. 

Alle disse filene er på formatet:

```xml
<BookingList>
  <Booking>
    ...
  </Booking>

  <Booking>
    ...
  </Booking>
</BookingList>
```

Oppgaven er da å endre følgende i hver `<booking>`:

- Klokkeslettet hvor opptaket skal gjøres
- Navnet på programmet
- UUID-en til å være en ny unik UUID

NB: _Det er viktig at klokkeslettet ikke overlapper med trailerskillet og ikke slutter for tidlig før trailerskillet. Alle programmer skal alltid begynne på hel time og slutte 30 sekunder før hel time._

Når du har gjort disse endringene slik at den stemmer overens med sendeplanen, lagrer du filen. 

Du kan også gjøre dette gjennom brukergrensesnittet til MultiCoder, men det er ikke garantert at klokkeslettet blir riktig. Det kan være at `XX:XX:30` blir lagret i XML-filen som `XX:XX:00`.  

Endringene kommer ikke til å endre noe på booking-listen som allerede er lastet inn, men laster du inn den nye endrede booking-listen blir den oppdatert. I skrivende stund lastes hver booking-liste inn kl. 23:59 hver dag. 

Om DeviceID-en endrer seg til å være en annen DeviceID, flytter du bare alle XML-filene over til den mappen som heter det samme som den nye DeviceID-en. 
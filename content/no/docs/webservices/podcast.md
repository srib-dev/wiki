---
title: "Podcast-server: Hjemmesnekret Django-program"
linkTitle: "podcast.srib.no"
date: 2023-03-04
weight: 1
description: >
  En forklaring av radioens podcast-server, skrevet i Django, som genererer RSS-strømmer for alle podcastene.
---

### Kort forklaring

Dette er en av nettressursene til radioen. Det er en podcast-server som driftes av friByte, og er [åpen kildekode](https://github.com/srib-dev/podkast.srib.no). Koden er i utgangspunktet skrevet av en tidligere teknisk sjef i radioen, men har blitt litt videreutviklet av medlemmer i friByte ut av nødvendighet.

Formålet med denne tjenesten er å generere nye RSS-strømmer som kan brukes for podcast-publisering. 

### Hvordan fungerer den?

Hver podcast får sin egen RSS-strøm. Denne RSS-strømmen kan gis videre til lydstrømmingsplattformer. RSS-strømmen er et langt XML-dokument som blir lengre for hver podcast-episode som produseres. 

Podcastserveren henter podcast-episoder fra en spesifikk mappe i [Mimir](/docs/machines/servers/mimir)/[Kvasir](/docs/machines/servers/kvasir). Den mappen er også synlig i [DBM](/docs/digasystem/dbm). 

Rutinen for radioens medlemmer er da at de legger inn en ferdigklippet podcast-episode med riktig metadata i podcast-mappen i DBM. Podcast-serveren genererer da automatisk en ny seksjon i RSS-strømmen for den nye episoden. 

Lydstrømmingstjenestene som lytter på den RSS-strømmen, mottar da forandringen og oppdaterer sin egen server som håndterer servering av episodene på sin side. 

### Tips

Slik som koden fungerer nå, om podcastserveren ikke klarer å hente ut episoden, må episoden slettes fra podcast-mappen i DBM og legges inn på nytt igjen. Episoden må legges inn på nytt igjen, først når podcast-serveren faktisk fungerer igjen.

Nettsiden brukes aktivt og [er å finne her](https://podcast.srib.no).
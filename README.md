# Via ROMA

Involveds månedlige ROMA-samtale som en interaktiv nettside: 3 minutter per prosjekt. Sju signaler med trafikklys, et par tall, tre linjer med viktigste punkter, og en Teams-tekst leder leser på 30 sekunder. Excel-eksport i samme oppsett som ROMAsamtaleskjema V1.10.

## Bruk

Åpne `index.html` i en nettleser. Ingen installasjon, ingen server. Alt lagres lokalt i nettleseren; ta sikkerhetskopi (JSON) fra Oversikt-fanen før du bytter maskin.

Nettsiden publiseres automatisk med GitHub Pages ved hvert push til `main`:

**https://forzacode00.github.io/ROMA/**

Hvis siden ikke svarer etter første push: Settings → Pages → Source: «GitHub Actions», og kjør workflowen «Publiser Via ROMA» på nytt under Actions.

## Hva den gjør

- **Dagens runde**: velg 1–3 prosjekter, kjør dem etter hverandre. Forrige måned ligger klar, du endrer bare det som er nytt.
- **Sju signaler** (R Ressurs, O Oversikt, M Menneske, A Ansvar): belastning, fremdrift, økonomi, omfang og rolle, kunde, trygghet, neste fase. Grønt, gult eller rødt. Økonomi-signalet følger kontraktstypen (timer uten ramme, timer med ramme, fastpris).
- **Viktigste punkter**: tre linjer per prosjekt: endret siden sist, risiko nå, trenger fra Involved. Diktering på mobil.
- **Puls** én gang per person: belastning og trivsel 1–5 med terskler for oppfølging.
- **Røde flagg** som alltid meldes til leder og Planner.
- **Full ROMA** (30 spørsmål) som frivillig dybde ved gult/rødt, og kvartalsvis.
- **Lever**: Teams-tekst per prosjekt, Excel per prosjekt (Prosjektinfo, ROMA-samtale, Tiltak & Oppfølging, Statusoversikt), ledereksport med prosjektkort og puls.
- **Oversikt**: prosjekter med neste samtale, trend, tiltakslogg, historikk, sikkerhetskopi og «Slett alle mine data».

## Personvern og sikkerhet

Appen er én HTML-fil uten backend. Alt lagres kun i brukerens egen nettleser (localStorage) og sendes aldri til noen server. Lenken kan derfor deles åpent: hver kollega ser bare sine egne data. Data forlater maskinen kun når brukeren selv kopierer Teams-teksten eller laster ned Excel/JSON, og disse filene må brukeren selv håndtere. Teams-tekst og ledereksport inneholder puls og Trygghet-signal og er kun ment for nærmeste leder. Prosjekt-Excel inneholder ikke dette. Diktering bruker nettleserens innebygde taletjeneste (Google/Microsoft). «Slett alle mine data» i Oversikt fjerner alt appen har lagret. Bibliotekene for Excel og konfetti ligger i `vendor/` i repoet, så siden fungerer også der eksterne CDN er blokkert.

Råd til kollegaene: bruk den offisielle lenken i vanlig nettleser (ikke som Teams-fane), ta sikkerhetskopi før maskinbytte, og bruk «Slett alle mine data» på delt maskin. Safari kan slette lokale data etter 7 dager uten besøk.

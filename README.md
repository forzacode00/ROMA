# Via ROMA

Involveds månedlige ROMA-samtale som en interaktiv nettside: 3 minutter per prosjekt. Sju signaler med trafikklys, et par tall, tre linjer med viktigste punkter, og en Teams-tekst leder leser på 30 sekunder. Excel-eksport i samme oppsett som ROMAsamtaleskjema V1.10.

## Bruk

Åpne `index.html` i en nettleser. Ingen installasjon, ingen server. Alt lagres lokalt i nettleseren; ta sikkerhetskopi (JSON) fra Oversikt-fanen før du bytter maskin.

Nettsiden publiseres automatisk med GitHub Pages ved hvert push til `main`:

**https://forzacode00.github.io/ROMA/**

Hvis siden ikke svarer etter første push: Settings → Pages → Source: «GitHub Actions», og kjør workflowen «Publiser Via ROMA» på nytt under Actions.

## Hva den gjør

- **Dagens runde**: velg prosjektene du tar nå, kjør dem etter hverandre. Forrige måned ligger klar som referanse, du setter fargene på nytt.
- **Ulike konsulenter, samme runde**: kundeoppdrag, salgsarbeid (tilbud og muligheter som kan ta måneder, uten kontraktskrav, med tilbudsfrist og «Vunnet → kundeoppdrag») eller intern rolle (kvalitetsleder, tilbud, faggruppe), alle med egne signaltekster. Andel av tiden per prosjekt: under 10 % gir kort runde med bare økonomi, omfang og kunde. Mange prosjekter gir samlet ledertekst med én linje per prosjekt. Ingen prosjekt gir runden «Mellom oppdrag» (neste oppdrag, innhold i dagene, hva du trenger). «Avslutt prosjekt» tar tre linjer sluttevaluering og beholder historikken.
- **Seks signaler per prosjekt** (O Oversikt, M Menneske, A Ansvar): fremdrift, økonomi, omfang og rolle, kunde eller internt, trygghet, neste fase. Grønt, gult eller rødt. Økonomi-signalet følger kontraktstypen (timer uten ramme, timer med ramme, fastpris).
- **Deg denne måneden** (R Ressurs), én gang uansett antall prosjekter: puls (belastning og trivsel 1–5), belastning som signal med timer per uke, og om du har hatt reell kontakt med Involved. Modus Travel, Balansert, Rolig eller Mellom oppdrag styrer hvor mye appen ber om; rolige måneder åpner en utviklingsmeny.
- **Viktigste punkter**: tre linjer per prosjekt: endret siden sist, risiko nå, trenger fra Involved. Diktering på mobil.
- **Røde flagg** som alltid meldes til leder og Planner.
- **Full ROMA** (30 spørsmål) som frivillig dybde ved gult/rødt, og kvartalsvis.
- **Lever**: Teams-tekst i jeg-form med «Fra deg»-linje øverst (det leder skal gjøre), én linje per prosjekt og samlet tekst ved tre eller flere. Excel per prosjekt med hele historikken (Forside med revisjonsspor, Prosjektinfo, Månedslogg med fargede signaler, ROMA-samtale, Tiltak & Oppfølging med datavalidering, Full ROMA, Sluttevaluering, Statusoversikt) uten puls og Trygghet. Ledereksport (Excel) med dashboard, «Dette må du gjøre denne uken» med kolonner leder fyller selv, prosjektkort, tiltak, ROMA-samtale og en Team-rad som kan slås sammen på tvers av konsulenter. Månedsrapport og prosjektutskrift som PDF (A4, ampel som symbol og farge), og årsutskrift som PDF med tolv måneders ampelrad, pulstrend og tre spørsmål til medarbeidersamtalen.
- **Oversikt**: aktive og avsluttede prosjekter med neste samtale, siste 12 måneder som prikker, tiltakslogg, årsutskrift til medarbeidersamtalen, sikkerhetskopi og «Slett alle mine data».

## Personvern og sikkerhet

Appen er én HTML-fil uten backend. Alt lagres kun i brukerens egen nettleser (localStorage) og sendes aldri til noen server. Lenken kan derfor deles åpent: hver kollega ser bare sine egne data. Data forlater maskinen kun når brukeren selv kopierer Teams-teksten eller laster ned Excel/JSON, og disse filene må brukeren selv håndtere. Teams-tekst og ledereksport inneholder puls og Trygghet-signal og er kun ment for nærmeste leder. Prosjekt-Excel inneholder ikke dette. Diktering bruker nettleserens innebygde taletjeneste (Google/Microsoft). «Slett alle mine data» i Oversikt fjerner alt appen har lagret. Bibliotekene for Excel (ExcelJS) og konfetti ligger i `vendor/` i repoet, og siden laster ingen eksterne fonter eller skript, så ingen tredjepart ser at du bruker den.

Råd til kollegaene: bruk den offisielle lenken i vanlig nettleser (ikke som Teams-fane), ta sikkerhetskopi før maskinbytte, og bruk «Slett alle mine data» på delt maskin. Safari kan slette lokale data etter 7 dager uten besøk.

## Til leder: kvittering etter Teams-teksten

Det som gjør at konsulenten fortsetter å svare ærlig, er at svaret fører til noe. Regel: svar innen 2 virkedager, rødt samme dag. Ledereksporten inneholder et forslag til første setning per prosjekt.

- **Grønn**: «Lest, takk. Alt grønt på [prosjekt]. Én ting jeg noterer: [ett punkt fra teksten]. Snakkes neste måned.»
- **Gul**: «Lest. Ser [signal] er gult. Jeg gjør [handling] innen [dato]. Si fra hvis det blir verre før det.»
- **Rød**: «Lest, ringer deg i dag kl [tid]. Tiltak: [hva], jeg eier det, frist [dato]. Legger det i Planner nå.»
- **Rolig måned**: «Lest, takk for ærlig puls. Rolig nå er ok, vi bruker det. Er du med på [utviklingsaktivitet], ca. [timer]? Jeg sjekker [kunde/tilbud] for neste fase innen [dato].»

Appen spør konsulenten neste måned om leder svarte. Ett «nei» vises øverst i neste ledertekst, to på rad ber om kopi til daglig leder. Utvikling konsulenten velger i rolige måneder sendes som forslag, og blir avtale når leder svarer.

## Hvem appen er laget for

Appen skiller på oppdragstype (kundeoppdrag med rådgivning eller innleie, salgsarbeid, intern rolle, mellom oppdrag) og på personen bak: stillingsprosent og avtalt kapasitet gir egne timegrenser, startdato gir en oppstartsrunde de første tre månedene i stedet for «mellom oppdrag», teamledere merker seg som det og rapporterer til daglig leder med en linje om teamet, og den som selv har kunde- og salgsansvar ber ledergruppen i stedet for «Involved». Måneder med ferie, permisjon eller annet fravær merkes med én knapp og teller ikke som hull. Prosjekter kan settes på pause med forventet gjenopptak. Kontrakt kan være signert, avrop i kundens portal, under arbeid eller mangle; opsjoner og forlengelser registreres med om de er utløst skriftlig; prosjekt overtatt fra kollega får egen overleveringssjekk. Tilbud og forlengelser, vunnet eller tapt, følger samme spor.

Runden avsluttes med «Klar til å sende», og først når teksten er kopiert eller Teams-chatten åpnet, står det «Sendt». Leders e-post gir en knapp som åpner riktig Teams-chat med teksten klar. «Legg ROMA-dagen i Outlook» lager en månedlig kalenderhendelse med varsel. Etter tre runder uten sikkerhetskopi minner appen om det. Når noe har stått rødt to måneder på rad, trivsel er lav to måneder, eller leder ikke har svart to ganger, finnes en egen eskaleringstekst til daglig leder uten puls og trygghet. «Prøv med eksempel» på første skjerm gir en demo med tre måneders fiktiv historikk for opplæring. Appen kan legges til på hjemskjermen (PWA) og fungerer uten nett etter første besøk.

## Forslag til oppdatert rutine

Appen har endret praksisen fra 30–45 minutter til 3 minutter per prosjekt med en kvartalsvis full ROMA. Rutinedokumentet bør oppdateres tilsvarende, så det ikke er et avvik ved revisjon. Forslag til formuleringer:

1. **Frekvens og form.** «ROMA-samtalen gjennomføres månedlig i to deler: en kort skriftlig runde i Via ROMA på ca. tre minutter per prosjekt som ressursen sender til nærmeste leder i Teams, og leders svar innen tre virkedager. Ved tunge signaler (belastning 4–5, trivsel 1–2, rødt på Trygghet, timer godt over avtalt) ringer leder innen tre virkedager. Full ROMA med 30 spørsmål gjennomføres kvartalsvis, ved oppstart og ved avslutning, og som samtale når leder eller ressurs ber om det.»
2. **Omfang.** «Rutinen gjelder alle kundeoppdrag uansett varighet, innleie og rådgivning, interne roller, tilbudsarbeid og perioder mellom oppdrag. Avrop under samme rammeavtale følges som ett oppdrag.»
3. **Ansvar, leder.** «Leder svarer på hver runde med Lest, Ringer eller Tar videre innen tre virkedager, følger opp tiltak der leder er ansvarlig, og bekrefter utviklingsforslag. Uteblir svar to måneder på rad, går runden også til daglig leder.»
4. **Ansvar, ledergruppen.** «Ledergruppen mottar eskaleringstekst når et signal har stått rødt to måneder på rad, trivsel er lav to måneder, eller en ressurs har vært mellom oppdrag i to måneder, og følger opp på tvers. Fagbidrag samles til fag- og erfaringsrapporten i november.»
5. **Gjennomføring.** Legg til trinn «Full ROMA (kvartalsvis, oppstart, avslutning)» og «Sluttevaluering i tre linjer: levert, lærdom, uavsluttet, pluss om kunden kan brukes som referanse».
6. **Dokumentasjon.** «Prosjekt-Excel og PDF fra Via ROMA lagres i prosjektmappen og inneholder ikke puls, belastning, restitusjon eller trygghet. Ledereksport med disse opplysningene lagres i leders HR-mappe med hjemmel i arbeidsmiljøloven § 4-1. Ressursen har innsyns- og sletterett. Puls, timer og Trygghet brukes ikke i lønnsvurdering.»
7. **Rapportering.** «Røde flagg legges i Planner av leder samme uke. Klager og reklamasjoner meldes i avvikssystemet, uønsket atferd i varslingsrutinen. Kvalitetsleder sender kundeundersøkelse ved avslutning av oppdrag og årlig for oppdrag over tolv måneder; appen lager tiltaket.»

## Kvalitetssikring

Versjon 5.1 er gjennomgått av 15 fagroller (prosjektsikring, arbeidsmiljø, kvalitet og miljø, ledelse, personvern, interaksjonsdesign, spilldesign, psykologi, kode) og fire konsulentpersonaer (mange små prosjekter, ett stort, intern rolle, mellom oppdrag) som testet flere måneders bruk i nettleser. Rundt 60 funn er rettet, blant annet: puls som forsvant når man la til prosjekt, «Mellom oppdrag» som ble utløst ved et uhell, kort runde som skjulte Trygghet og utløp av oppdrag, kontraktsflagg som forsvant etter oppstartssjekk, sluttevaluering som aldri nådde leder, kroniske gule og røde signaler uten eskalering, og personflagg som farget alle prosjekter røde.

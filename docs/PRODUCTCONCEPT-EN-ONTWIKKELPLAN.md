# Workstr: productconcept en ontwikkelingsplan

Status: voorstel ter besluitvorming, geen beschrijving van reeds gebouwde backendfunctionaliteit.

## 1. Visie en positionering

**Workstr maakt zichtbaar wat je kunt en brengt je in contact met relevant werk, zonder eindeloze vacaturelijsten.**

Een visueel werkprofiel combineert CV, projectfoto's, skills, beschikbaarheid en voorkeuren. Kandidaten ontdekken werk via een verticale feed. Werkgevers en recruiters ontdekken uitsluitend toegankelijke kandidaten via een uitlegbare zoek- en suggestielaag. Wederzijdse interesse opent de weg naar persoonlijk contact.

### Aanbevolen eerste markt

Start met freelancers en kleine teams in één visueel vakgebied en één regio, bijvoorbeeld ontwerp/content in de Randstad. Dit is een hypothese om met interviews te toetsen, geen bewezen marktkeuze. De huidige fictieve design-, horeca- en techvacatures illustreren de interface, niet een vastgestelde lanceringstrategie.

Begin niet tegelijk met alle beroepen, alle landen en alle recruitmentdatabases. Een relevante, actuele lokale markt is waardevoller dan een grote lege feed. Onderscheid opdrachten voor freelancers van banen in loondienst in datamodel, filters en voorwaarden.

### UVP voor freelancers en kandidaten

- Laat bewijs van je werk zien: projecten, eigen rol, foto's, skills en resultaat naast je CV.
- Geef tariefband, gewenste opdrachtduur, regio, werkvorm en beschikbaarheid zelf aan.
- Ontdek snel relevante opdrachten en teams via scrollen, bewaren en interesse tonen.
- Houd controle over profielzichtbaarheid, contactgegevens en vindbaarheid.
- Houd je profiel actueel met een reminder iedere drie kalendermaanden.

**Belofte:** minder herhaald invulwerk en een rijkere eerste indruk. Geen garantie op werk of perfecte matches.

### UVP voor werkgevers en recruiters

- Zoek op aantoonbare skills, beschikbaarheid en opdrachtvoorwaarden in plaats van alleen functietitels.
- Eén shortlist over eigen, toegestane bronnen, met herkomst en actualiteitsdatum.
- Zie ontbrekende of onbevestigde informatie voordat je contact opneemt.
- Voorkom bulkspam met contactlimieten, blokkeren/melden en wederzijdse interesse.
- Laat recruiters de uiteindelijke selectie en vervolgstap bepalen.

**Belofte:** minder handmatig zoek- en administratiewerk. Tijd- en kostenbesparing worden pas geclaimd na meting in de pilot.

## 2. Verdienmodel

### Aanbevolen model

| Doelgroep | Voorstel | Grenzen |
|---|---|---|
| Freelancer/kandidaat | Gratis basisprofiel, portfolio, ontdekken en contact bij wederzijdse interesse | Niet betalen om normaal zichtbaar te zijn; geen verkoop van persoonsgegevens |
| Werkgever | Maandabonnement per actieve vacature/opdracht | Transparante limiet en archivering; voorwaarden en tarieven eerst toetsen |
| Recruiter/team | Teamabonnement met seats, actieve zoekopdrachten en toegestane bronkoppelingen | Geen onbeperkte bulkexport of contactspam |
| Enterprise | Inrichting plus abonnement voor extra koppelingen, SSO en afgesproken ondersteuning | Integratiekosten en datalicenties apart zichtbaar |

Geen betaalde ranking vermengen met inhoudelijke geschiktheid. Als gesponsorde vacatures later worden toegevoegd, moeten ze herkenbaar en afzonderlijk worden aangeboden.

**Pilot:** begin met overeengekomen pilotvoorwaarden en interviews over betalingsbereidheid. Zet nog geen verzonnen prijzen op de website. Meet kosten van opslag, media, bron-API's, zoekindex, AI-verwerking, ondersteuning en acquisitie per actief klantaccount.

Een succesfee is niet aanbevolen voor het eerste MVP: het maakt attributie, facturatie en geschillen complexer. Herbeoordeel na product-marktvalidatie.

## 3. Feature-roadmap en acceptatiecriteria

### Wat er al is

Responsieve React/Vite-conceptwebsite, verticale fotofeed, fictieve vacatures, lokale favorieten, zoekveld en sectorfilter, werkvibe-keuzehulp, licht/donker, functietabs en contact via e-mailconcept. Geen accountbackend, bestandsuploads, echte AI, chat, pushnotificaties of App Store-app.

### MVP: één volledige, betrouwbare keten

| Onderdeel | MVP-scope | Acceptatiecriterium |
|---|---|---|
| Accounts en rollen | Kandidaat, werkgever/recruiter; tenantgrenzen en bevestigde e-mail | Een account kan nooit een profiel, bestand of shortlist van een onbevoegde tenant lezen |
| CV-profiel | Handmatig bewerkbaar werkverleden, skills, opleiding, beschikbaarheid, tarief en voorkeuren; optionele PDF-import met controle | Gebruiker controleert geïmporteerde velden vóór publicatie; onzekere velden worden niet verzonnen |
| Portfolio | Projecttitel, eigen rol, beschrijving, skills, datum, foto's en optionele link | Uploadvoortgang, validatie, opnieuw proberen, volgorde aanpassen, alttekst en verwijderen werken |
| Privacy | Vindbaarheid en contactgegevens afzonderlijk instelbaar | Niet-vindbare profielen verschijnen niet in zoekresultaten of afgeleide indexen |
| Vacatures/opdrachten | Aanmaken, bewerken, publiceren, pauzeren, sluiten | Alleen bevestigde bevoegde organisaties kunnen publiceren; statuswijzigingen werken door in feed |
| Ontdekken | Verticale feed; filters voor vakgebied, locatie, beschikbaarheid en opdracht/loondienst | Kerngegevens staan vóór de interesseknop; ook volledig met toetsenbord bedienbaar |
| Interesse | Rechts/interesse, links/overslaan, bewaren en ongedaan maken | Een herhaalde actie veroorzaakt geen dubbel verzoek; overslaan is geen permanente afwijzing |
| Matching en zoeken | Eigen opt-in database; harde filters plus tekst/semantische zoekopdracht | Elke suggestie bevat bron, actualiteit, passende skills en onbekende informatie; geen automatische afwijzing |
| Contact | Eenvoudige tekstchat na wederzijdse interesse, blokkeren/melden | Onbevoegde contacten kunnen geen berichten lezen of sturen; misbruik is meldbaar |
| Kwartaalreminder | In-app melding, e-mailvoorkeuren, updateflow en uitschakelen | Eén reminder per profiel/periode; geen melding na uitschrijven of accountverwijdering |
| Beheer | Organisatiecontrole, meldingen, uploadmoderatie, auditlog | Beheertoegang is beperkt en gelogd; gebruiker kan fouten melden |

**Bewuste fasering:** één interne database in het MVP. Hoogstens één externe connector in de pilot als contract, API en toegangsmodel vooraf duidelijk zijn. Een ambitie voor multi-database-search is geen reden om de eerste lancering ervan afhankelijk te maken.

### Na het MVP

1. Meerdere ATS/partnerconnectors met licenties, incremental sync, deduplicatie en operationeel beheer.
2. Pushnotificaties, betere profiel-import en beschikbaarheidsreminders; verantwoord gemeten zoekverbeteringen.
3. Korte vacature-/portfoliovideo's met transcodering, ondertiteling en moderatie.
4. Native mobiele app, bijvoorbeeld Expo/React Native met gedeelde TypeScript-domeinlogica en API-client. De bestaande DOM/CSS-interface wordt niet automatisch native.
5. Teamrollen, SSO, meertaligheid en enterprise-integraties.

Geen harde lanceringsdatum zonder teamcapaciteit, API-toegang en privacy-/securityreview. Verdeel levering in onderstaande fasen met beslispoorten, niet in beloofde kalenderweken.

## 4. UX/UI-flows

### Freelancer: onboarding en CV

Welkom → rol kiezen → account bevestigen → zichtbaarheid uitleggen → CV invullen of PDF importeren → extractie controleren → skills/beschikbaarheid/tarief aanvullen → portfolio toevoegen → profielpreview → publiceren.

CV-import is een assistent, geen waarheid: toon de oorspronkelijke bron, markeer onzekerheden en laat velden corrigeren. Foto, leeftijd of geboortedatum zijn geen verplichte selectiecriteria. Foto's van werk zijn iets anders dan portretfoto's.

### Portfolio uploaden

Profiel → Project toevoegen → titel/eigen rol/beschrijving → foto selecteren of camera openen → lokale preview → bijsnijden en volgorde → alttekst → upload → scan/verwerking → preview → publiceren.

Voorgestelde startlimiet: 8 foto's per project, 10 MB per foto. Deze waarden zijn productkeuzes, geen technische garanties. Start met JPEG/PNG/WebP; HEIC moet expliciet ondersteund worden via veilige conversie of een duidelijke foutmelding geven.

- Draft blijft behouden bij een netwerkfout; per bestand opnieuw proberen.
- Alleen succesvolle, goedgekeurde uploads zijn publiceerbaar.
- Toon bestandsspecifieke foutmeldingen, geen algemene 'iets ging mis'.
- Verwijderen haalt het bestand ook weg uit thumbnails, zoekindexen en caches volgens vastgelegd beleid.
- Vraag bevestiging dat gebruiker rechten heeft om materiaal te delen; waarschuw voor klantgeheimen en herkenbare personen.
- Server controleert daadwerkelijke inhoud/MIME, bestandsgrootte, malware en metadata; een bestandsextensie alleen is niet voldoende.
- Verwijder EXIF-locatiegegevens en maak veilige afgeleide afbeeldingen. Gebruik private opslag en kort geldige signed URLs.

### Swipe en scroll

Verticale beweging = volgende/vorige vacature of kandidaat. Horizontale beweging = interesse of overslaan, pas na een duidelijke afstandsdrempel. De interface toont vooraf welke actie wordt uitgevoerd. Bij twijfel over de richting blijft de beweging verticaal; geen onbedoelde sollicitatie.

Elke kaart toont: opdracht/functie, organisatie, locatie/remote, tarief of salaris, uren, contracttype en relevante skills. Eén tik opent details zonder de feedpositie te verliezen.

Onderin staan altijd zichtbare alternatieven: Overslaan, Bewaren en Interesse. Een interesseactie verstuurt niet direct het volledige CV of privécontactgegevens. Als een formele sollicitatie gewenst is, volgt een afzonderlijke bevestiging met te delen gegevens.

Werkgever toont ook interesse → match → korte chat → uitnodiging/kennismaking. Een AI-ijsbreker is optioneel en bewerkbaar; nooit ongemerkt namens iemand versturen.

Toegankelijkheid: geen informatie alleen via kleur/animatie, grote aanraakvlakken, schermlezerlabels, toetsenbordbediening, reduced motion en optionele haptiek. Geen eindeloze auto-animaties die beweging afdwingen.

### Kwartaalreminder

Voorgestelde regel: drie kalendermaanden na laatste profielbevestiging, niet automatisch na alleen een login. Bij datums aan het eind van een maand normaliseren naar de laatste geldige dag. Tijdzone en zomertijd worden expliciet verwerkt.

'Hey, update je CV. Kloppen je ervaring, portfolio en beschikbaarheid nog?'

Acties: Bijwerken / Alles klopt nog / Later herinneren. 'Alles klopt nog' vernieuwt confirmed_at, maar claimt geen nieuw werkproject. Snoozen wijzigt alleen het volgende meldmoment. E-mail en latere push hebben eigen voorkeuren en kunnen worden uitgezet.

Verstuur met een idempotente period key, quiet hours en opt-outcontrole vlak voor aflevering. Herhaalde jobs mogen niet dubbel versturen. Behandel verwijderde accounts, bounces en ingetrokken push-toestemming.

## 5. AI-searcharchitectuur

### Ontwerpprincipe

Niet: een taalmodel dat bij iedere swipe willekeurig alle externe databases doorzoekt.

Wel: een gecontroleerde connectorlaag die toegestane gegevens normaliseert, een beveiligde zoekindex en een gerangschikte shortlist met bewijs. Het LLM helpt vacaturecriteria structureren en resultaten uitleggen; het bepaalt niet wie rechten heeft.

### Gegevensstroom

Werkgever publiceert vacature
→ transactionele outbox registreert event met tenant/job/version
→ queue start zoekopdracht
→ autorisatie bepaalt welke bronnen/velden zijn toegestaan
→ interne index zoekt met harde filters en hybride ranking
→ optionele beperkte live-verificatie bij toegestane bronnen
→ deduplicatie en geschiktheidscontrole
→ shortlist met bron + bewijs + actualiteit + onzekerheden
→ recruiter beoordeelt en kiest vervolgstap.

Los daarvan:

Bron-API/webhook → connectorworker → schema-validatie/normalisatie → brongebonden records → ACL/zichtbaarheid → indexupdate.

### Aanbevolen technische basis

- Bestaande React/Vite-frontend behouden; domeinlogica stapsgewijs naar gedeelde TypeScript-types.
- Een modulaire backend/API in TypeScript, geen microservicecluster als startpunt.
- PostgreSQL voor accounts, organisaties, rollen, profielen, vacatures en interacties.
- PostgreSQL full-text plus pgvector als eerste hybride zoekindex; pas een aparte zoekengine toevoegen als volume/latentie daar aantoonbaar om vragen.
- Object storage voor CV's/portfolio; private buckets, signed uploads en async scan/verwerking.
- Duurzame jobs voor reminders, indexering, import, connector-sync en notificaties. Een beheerde queue of bewezen jobrunner, niet een timer in de frontend.
- Provider-onafhankelijke AI-adapter voor parsing, embeddings en uitleg. Geen API-sleutels in de browser.
- SSO/push/betalingen later als modules; tenantisolatie en logging vanaf het begin.

### Connectorcontract

Per connector: bron-ID, organisatie/tenant, credentialreferentie, toegestane acties, toegestane velden, licentie-/doelbinding, sync-cursor, rate limits, dataregio, last_success_at en verwijderingsmogelijkheden.

Toegestane bronnen kunnen zijn: eigen opt-in Workstr-profielen, het eigen ATS van een klant via OAuth, of een gelicentieerde partnerdatabase. Publieke vindbaarheid is geen algemene toestemming voor hergebruik. Geen scraping van afgeschermde databases en geen omzeiling van API- of toegangsbeperkingen.

Als een bron lokale opslag of embeddings niet toestaat, gebruik een federated query die alleen toegestane resultaten tijdelijk verwerkt. Laat die bron buiten de index. Geen connector is 'klaar' zonder technische én contractuele validatie.

### Canoniek datamodel

User; Organization; Membership; Profile; Experience; Skill; Availability; PortfolioProject; MediaAsset; Vacancy; SourceRecord; Connector; SearchRun; MatchSuggestion; Interest; Conversation; Message; NotificationPreference; ReminderSchedule; ConsentRecord; AuditEvent; DeletionJob.

SourceRecord bewaart source_id/external_id, tenant/ACL, fetched_at, source_updated_at, valid_until, provenance en toepasselijke beperkingen. Scheid geïmporteerde brondata van door gebruiker bevestigde profieldata. Houd consenthistorie naast een gecontroleerde rechtsgrond per verwerkingsdoel; een vinkje vervangt geen privacyanalyse.

### Efficiënt zoeken en ranking

1. Structureer vacaturetekst naar vaardigheden en voorwaarden. Recruiter bevestigt harde eisen. Onderscheid verplicht, gewenst en onbekend.
2. Pas tenant, bronrechten, profielzichtbaarheid en harde criteria toe vóór kandidaten een AI-service bereiken. Hercontroleer bij ophalen van records en bij tonen/exporteren.
3. Combineer tekstzoekresultaten met semantische nabijheid voor synoniemen en projectervaring. Haal een begrensde top-K op; de grens wordt in tests afgestemd.
4. Rangschik op aantoonbare skills, relevante ervaring, beschikbaarheid en voorkeuren. Ontbrekende gegevens betekenen 'onbekend', niet automatisch 'ongeschikt'.
5. Ontdubbel voorzichtig met stabiele bron-ID's en geverifieerde koppelkenmerken. Voeg niet stilzwijgend mensen met dezelfde naam samen.
6. Toon bewijs per criterium met bron en datum. Een percentage mag pas verschijnen na validatie/calibratie en met uitleg; aanvankelijk liever 'sluit aan / onbekend / wijkt af'.
7. Recruiter controleert. Geen volledig geautomatiseerde afwijzing of bulkcontact.

Sla embeddings op per teksthash + modelversie; herbereken alleen gewijzigde toegestane tekst. Synchroniseer via webhooks waar mogelijk en delta-polling met cursors waar nodig. Queueworkers respecteren rate limits en retries met backoff. Cache uitsluitend binnen tenant/ACL/visibility-context; invalidatie bij permissie- of profielwijziging.

### Betrouwbaarheid, privacy en veiligheid

- Timeouts, circuit breakers en een partial-result-status: '2 van 3 toegestane bronnen bijgewerkt' in plaats van doen alsof alle bronnen doorzocht zijn.
- Contactgegevens alleen tonen na passende toestemming/bevoegdheid; publieke portfolio, zoekprofiel en privévelden scheiden.
- Taalmodellen krijgen geminimaliseerde velden, geen onnodige identificatie- of gevoelige gegevens.
- CV-teksten, afbeeldingen en externe records zijn onbetrouwbare input, nooit systeeminstructies. Geen modelgestuurde toolacties op basis van instructies in een CV.
- Geen afleiding van afkomst, gezondheid, religie of andere gevoelige eigenschappen uit tekst of foto's. Geen geschiktheidsscore op uiterlijk.
- Verwijdering verspreidt naar object storage, index/vectoren, caches en bronkoppelingen binnen afgesproken termijnen; backups hebben eigen retentiebeleid.
- Log modelversie, zoekcriteria, gebruikte bronnen en rankingredenen zonder volledige CV's in algemene logs.
- Regel bewaartermijnen, verwerkersafspraken, rechten van betrokkenen en een passende privacy-/impactbeoordeling. Laat vóór pilot en livegang juridisch toetsen welke AVG- en AI-regels op deze concrete inzet van toepassing zijn. Dit plan is geen juridische goedkeuring.

## 6. Ontwikkeling in beslisbare fasen

### Fase A: productvalidatie

Eigenaren: product/oprichters. Interview freelancers en hiring teams, kies een eerste markt, test portfolio- en swipeprototypes, leg succescriteria en pilotvoorwaarden vast. Beslismoment: voldoende aanbod en aantoonbare behoefte aan het specifieke probleem.

### Fase B: veilige basis

Eigenaren: backend/full-stack en frontend. Accounts, tenantisolatie, CV-profiel, portfolio-uploadpipeline, vacaturebeheer, privacyinstellingen en migraties. Beslismoment: upload-/autorisatie-/verwijdertests slagen en herstelprocedure is getest.

### Fase C: matching en contact

Eigenaren: backend/search plus product/UX. Interne hybride search, shortlistuitleg, feed, wederzijdse interesse en tekstchat. Beslismoment: geblindeerde menselijke evaluatie toont nuttige resultaten; geen bron- of tenantlekkage.

### Fase D: actualiteit en pilot

Eigenaren: engineering/operations met pilotklanten. Reminders, notificatievoorkeuren, moderatie, support en monitoring. Indien gereed: één toegestane externe connector. Beslismoment: pilotervaring, betrouwbaarheid, kosten en privacy-/securityreview verantwoorden opschaling.

### Fase E: uitbreiding en app

Eigenaren: mobile/engineering. Native app, push, extra databronnen en eventueel video. Eerst TestFlight/gesloten tests, daarna store-inzending met correcte privacyinformatie, accountverwijdering, moderatie en demo-toegang voor review. Goedkeuring en publicatiedatum niet vooraf garanderen.

Benodigde competenties: product/UX, frontend, backend/search, operationeel beheer en externe privacy/securityexpertise. De daadwerkelijke planning hangt af van beschikbaar team, gekozen pilotmarkt en bron-API's.

## 7. Meetplan en teststrategie

**Noordster:** relevante wederzijdse connecties die tot een daadwerkelijk gesprek leiden; niet het aantal swipes.

Meet: profielvoltooiing, portfolio-publicatie, bevestigde beschikbaarheid, zoekresultaatkwaliteit, wederzijdse interesse, tijd tot eerste reactie, gesprek→kennismaking, gebruikersrapportages, reminder-opt-out en kosten per actieve vacature. Verzamel alleen noodzakelijke productmetingen met een passend privacyontwerp.

Testen:
- Autorisatiematrix voor rollen/tenants/bronnen/velden; inclusief negatieve tests en signed URLs.
- Upload: verkeerde extensie, MIME-mismatch, te groot, netwerkonderbreking, scan failure, EXIF, verwijderen.
- Herhaalde interesse- en reminder-events; rate limits, timezonegrenzen en einde-maanddatums.
- Feed: muis, toetsenbord, touch, richtingsambiguïteit, undo en reduced motion.
- Search: gelabelde beoordelingsset, rankingrelevantie, onbekende criteria, deduplicatie, provenance en verwijdering uit embeddings.
- Externe bronnen: 401/403, rate limiting, onvolledige sync, schemawijzigingen en ingetrokken toegang.
- Echte apparaatproeven voor push, camera/HEIC en zwakke mobiele verbindingen.

Stel doelwaarden vóór de pilot samen vast op basis van een meetbare nulmeting; geen verzonnen succespercentages.

## 8. Besluiten die nu nodig zijn

1. Eerste doelgroep: freelancers, loondienst of één scherp afgebakend segment?
2. Eerste branche en regio, plus wie pilotkandidaten en werkgevers aanbrengt.
3. Welke concrete ATS/partnerbron mag gekoppeld worden en onder welke voorwaarden?
4. Wie bouwt/beheert de backend en welke teamcapaciteit is beschikbaar?
5. Welke publieke profielvelden, contactregels en reminderkanalen zijn acceptabel?
6. Welk experiment valideert dat werkgevers willen betalen?

**Aanbevolen eerstvolgende implementatie:** CV-profiel + portfolio + vacaturebeheer bovenop een veilige accountbackend. Daarna de bestaande feed op echte, toegestane data aansluiten. Niet starten met een oncontroleerbare 'AI die overal zoekt'.

## Question 1

*What are the main differences between Enterprise and Solution Architecture.<br>
Describe the different roles that these play in designing large scale Systems?<br>
You can use resources like the video Enterprise Architecture vs Solution Architecture to help you answer.*

---

**Enterprise Architecture** (EA) og **Solution Architecture** (SA) har forskellige fokusområder og roller i design af store systemer. EA er strategisk og ser på hele virksomheden, mens SA er mere taktisk og fokuserer på at løse specifikke forretningsproblemer.

* **Enterprise Architecture**
    * **Fokus**: EA har et holistisk overblik over hele organisationens IT-landskab. Deres primære mål er at sikre, at IT-strategien er i overensstemmelse med forretningens overordnede mål og mission.
    * **Rolle**: EA'er er strategiske ledere, der definerer standarder, retningslinjer og rammer for IT-systemer på tværs af organisationen. De fokuserer på langsigtet optimering, risikoreduktion og sikring af, at nye projekter passer ind i det eksisterende systemlandskab. De er som "politichefen, der ser på at reducere den samlede kriminalitet i byen" i stedet for at løse én specifik sag.
    * **Output**: EA'er skaber roadmaps, principper og strategier, der styrer teknologivalg og investeringer for hele virksomheden.

* **Solution Architecture**
    * **Fokus**: SA er mere målrettet og koncentrerer sig om at designe og implementere tekniske løsninger til et specifikt forretningsproblem eller et enkelt projekt.
    * **Rolle**: SA'er agerer som broen mellem forretningsbehov og den tekniske implementering. De tager de overordnede retningslinjer fra EA og oversætter dem til en detaljeret plan for en enkelt applikation eller løsning, der sikrer, at den er funktionel, sikker og pålidelig. De er specialisterne, der "løser en enkelt sag" og sikrer, at projektet leveres inden for budget og tidsplan.
    * **Output**: SA'er skaber detaljerede tekniske designs, diagrammer og specifikationer for en bestemt løsning, herunder valg af teknologi, integrationer og komponenter.

Kort sagt, EA giver den overordnede strategiske retning, mens SA leverer den praktiske, projektspecifikke implementering. De to roller supplerer hinanden og er begge afgørende for succesfuld systemudvikling.

---

## Question 2

*In his video called Practical Architecture what does Stefan Tilkov say about the role of teams in modern architecture.<br>
He refers to a book Team Topologies - what "team topologies" does the book describe?<br>
Do you agree from your own experience that the team is a core part of a successful project?*

---

I videoen understreger Stefan Tilkov, at den moderne arkitektur ikke er en statisk plan, men derimod et resultat af den måde, teams er organiseret på. Han pointer til, at succesfulde arkitekturer afhænger af at give autonome teams ejerskab og beslutningskraft, især over de systemer de bygger. Det klassiske hierarki, hvor en central arkitekt dikterer alt, er ineffektivt og skaber friktion. Tilkov mener, at systemgrænser bør afspejle teamgrænser, da manglende overensstemmelse herimellem fører til synkroniseringsproblemer og unødvendige møder. I stedet for at have et separat arkitekturteam, der tager alle beslutninger, skal arkitekter fungere som "enabling teams" der hjælper de selvorganiserede teams med at træffe de rigtige arkitekturvalg.

Bogen **Team Topologies** af Matthew Skelton og Manuel Pais, som Tilkov henviser til, beskriver fire grundlæggende teamtyper og tre interaktionsmønstre, som kan optimere en organisations flow af værdi.

De fire grundlæggende teamtyper er:
1.  **Stream-aligned teams**: Disse teams er organiseret omkring en konstant strøm af arbejde, der er justeret efter en forretningsmæssig værdistrøm. De har fuldt ejerskab af en forretningsfunktion og kan levere værdi med minimal afhængighed af andre teams.
2.  **Enabling teams**: Disse teams består af specialister, der hjælper andre teams med at overkomme tekniske forhindringer eller forbedre deres færdigheder. De fungerer som mentorer og undervisere.
3.  **Complicated Subsystem teams**: Disse teams har specialiseret viden og ansvar for at bygge og vedligeholde et komplekst system, som kræver dyb ekspertise.
4.  **Platform teams**: Disse teams leverer og vedligeholder en intern platform som en service for andre teams i organisationen, hvilket reducerer deres kognitive byrde.

Fra min egen erfaring er det helt afgjort, at teamet er en kernekomponent i et succesfuldt projekt. Autonome, tværfaglige teams med klart ejerskab og et fælles mål kan træffe hurtigere og bedre beslutninger, fordi de har fuld kontekst og direkte ansvar for resultaterne. Deres evne til at tilpasse sig og lære på tværs af team- og systemgrænser er afgørende for, at et projekt kan forblive smidigt og effektivt.

I vores gruppe har vi i Datamatiker uddannelsen oplevet (I systemudviklings faget) at 'diktere' gennem lead-developers for et større team skaber friktion da det kan føre til misforståelser og en følelse af manglende ejerskab blandt teammedlemmerne. Pull-requests kom hist of pist og friktionen mellem "det er godt nok" og "nej, lav det om" langsommeliggjorde udviklingsprocessen.

Med dette sagt er vores erfaring, at teams skal kunne fungere selvstændigt, magen til "devide and conquer" i programmering; jo mere selvstændige solutions er på tværs af en entitet, jo bedre kan de tilpasse sig ændringer og nye krav.

---

## Question 3

*Also in this video Stefan Tilkov explains why some things are best done centrally (for example at 23 min 30 seconds).<br>
Why do you think he is saying this?<br>
What does he claim are the benefits?*

---

I videoen argumenterer Stefan Tilkov for, at selv i en moderne, decentraliseret arkitektur med autonome teams, er der stadig visse ting, som er bedst at beslutte centralt. Han forklarer dette ved at sige, at centraliserede beslutninger er nødvendige for de aspekter, der er relevante "at the seams"(~19:20) – altså de steder, hvor systemer og teams interagerer med hinanden.

Han siger dette, fordi hvis mere end to teams skal samarbejde om et fælles element, som et interface eller en standard, vil en decentraliseret tilgang føre til en "...explosion of interactions or negotiations". Disse gentagne forhandlinger vil spilde tid, skabe uoverensstemmelser og resultere i en ineffektiv proces.

Altså, reduceres kompleksiteten markant, da man undgår, at hvert team opfinder sin egen løsning til standarder og fælles grænseflader, hvilket mindsker den samlede systemkompleksitet. Dette leder til større effektivitet ved at fjerne behovet for konstante bilaterale forhandlinger mellem teams, hvilket frigiver værdifuld tid, som teams i stedet kan bruge på deres primære opgaver. Derved sikrer teamsne centraliserede beslutninger en ensartethed gennem hele systemet, som gør det betydeligt lettere for teams at genbruge både komponenter og viden på tværs af organisationen.

Tilkov anerkender, at centralisering kan betragtes som en "nødvendig ondskab," men han argumenterer for, at ved at begrænse de centrale regler til et absolut minimum og samtidig håndhæve dem konsekvent og strengt, opnår man en effektiv balance mellem teamautonomi og organisatorisk styring.

Igen kan man danne parallel til vores Datamatiker forløb, hvor vi faktisk havde lidt negativt feedback af at vi tog initiativ da grupperne ikke fulgte et fælles regelsæt. Dette initiativ endte så med at virke lidt diktatorisk, og i sig selv kunne argumenteres at være en "hårdere ondskab". 

Vi mener derfor at Tilkovs "nødvendig ondskab" ville have fungeret bedre i vores tilfælde, da en centraliseret og aftalt ondskab er bedre end en diktatorisk ondskab.

---

## Question 4

*In the video Architecting for Outcomes Simon Rohrer describes old fashioned and modern enterprise architecture.<br>
He talks about the A B C D E of modern architecture to compare modern and legacy ways of working.<br>
Do you find his arguments persuasive and if so why?*

---

Ja. Rohrers argumenter virker overbevisende, fordi de stemmer overens med, hvordan succesfulde tech‑virksomheder arbejder i dag, som er med fokus på outcomes og kontinuerlig adaptation gør Enterprise Architecture (EA) til en praktisk enabler fremfor en teoretisk begrænsning.

ABCDE‑modellen omstiller EA som samarbejdende og iterativ (ligesom agile), med fokus på løbende levering af værdi, styring gennem conversation og automation, og løbende udvikling af både teknologi og organisation.

Det henviser til typiske svagheder ved gammel EA, som var for langsom, misaligned med delivery, og ignorering af menneskelige faktorer.

Rohrers vægt på målbare outcomes (fx BVSSH) og praktiske mønstre som Domain‑Driven Design forklarer også, hvorfor tilgangen kan reducere risiko og accelerere value delivery i organisationer som Saxo Bank.

Så kort sagt, så bør moderne EA være Active, outcome‑driven og integreret i den continuous delivery‑proces i stedet for at være en statisk plan på hylden.

---

## Question 5

*In the same video he explains the concept of the "Continuous Conversation".<br>
In what ways does he say it benefits Saxo Bank?<br>
How does he connect the Continuous Conversation to the Devops Infinity Loop.*

---

Rohrers "Continuous Conversation" beskrives som en løbende, tværfaglig dialog mellem teams, arkitekter og stakeholders, og det gavner Saxo Bank på flere måder:

- **Hurtig feedback**: arkitekter deltager i sprint demos, pull requests og chats, så teams får arkitekturinput på timer/dage i stedet for uger.
- **Governance uden bureaukrati**: automatiserede checks (policy-as-code) og GitOps‑style merge‑requests fanger anomalier og gør approvals til en del af CI/CD‑flowet.
- **Bedre alignment og læring**: en Architecture Community of Practice og brug af Architecture Decision Records sikrer, at teams forstår rationale og arkitekter får real‑world input til at justere standarder.
- **Drift‑tilbagemelding i design**: arkitekter følger Operate/Monitor‑data og bruger disse indsigter i næste plan/design‑iteration, hvilket reducerer "big upfront" beslutninger.
- **Agility med kontrol**: Continuous Conversation skaber en kontinuerlig strøm af mindre, målbare beslutninger, så Saxo Bank kan kombinere hastighed fra DevOps med Enterprise Architecture‑styring.

Rohrer kobler Continuous Conversation direkte til DevOps Infinity Loop ved at gøre arkitektur til en del af hele loopet (plan -> code -> build -> test -> release -> deploy -> operate -> monitor -> plan). Continuous Conversation fungerer som broen mellem left‑side og right‑side i loopet: operationel feedback (monitor) føder designvalg (plan) hurtigt tilbage, og arkitekturstyring er løbende indlejret i CI/CD via automation og konversation.

---

## Question 6

*In the course we will focus on building integrated Enterprise scale applications using messaging and there are a number of core Integration Patterns for messaging.<br>
Using the Powerpoint Presentation for this week called Enterprise Architecture and Integration patterns describe 5 integration patterns for messaging and provide a use case for them.<br>
You can add more depth to your answer by coding the examples (you may have done some of this for OLA1).<br>
You should include Pipes and Filters and the Request Reply patterns as part of your answer.*

---

**Pipes and Filters**

- Dette pattern bryder en kompleks proces i en sekvens af uafhængige filtre forbundet af pipes, der tillader modular data transformation.
- Use case: I en data analytics pipeline filtreres rå logs for errors, transformeres til struktureret format og aggregeres for rapportering.

**Request-Reply**

- En afsender sender en request message og venter på en reply, der muliggør synkron-lignende adfærd i asynkrone systemer.
- Use case: En frontend service requester user data fra en backend database service og venter på response for at rendere en profilside.

**Publish-Subscribe**

- En publisher udsender en besked til et topic, og flere subscribers modtager hver deres kopi. Mønstret skaber løs kobling mellem producent og forbrugere og gør det nemt at skalere og tilføje nye abonnenter.
- Eksempel: Et aktiehandels‑system publicerer price updates til en aktie, så alle klientapplikationer modtager real‑time notifikationer.

**Message Router**

- En router undersøger beskedens indhold og sender den videre til den rette kanal eller endpoint efter faste regler. Det centraliserer routing‑logikken og undgår, at afsenderen skal kende alle modtagere.
- Eksempel: Kundehenvendelser rutes automatisk til salg eller support afhængig af keywords i beskeden.

**Point-to-Point**

- Beskeder lægges på en kø, hvor kun én consumer henter og behandler hver besked. Dette sikrer eksklusiv håndtering af job og understøtter load‑balancing mellem workers.
- Eksempel: Jobfordeling i en worker‑pool, hvor flere workers konkurrerer om at behandle opgaver fra samme kø.

---

## Question 7

*In Gregor Hohpe's talk Enterprise Integration Patterns 2 he describes the idea of conversations in a messaging architecture (from 18 minutes).<br>
He explains how a 'messaging' and 'conversation' architecture are different.<br>
What differences are there and what challenges does he describe for conversation based solutions (for example what is the difference between pub-sub and subscribe-notify).*

---

Messaging er enkeltstående messages gennem pipes & filters i overvejende stateless komponenter med høj decoupling, scalability og enkel sammensætning. Conversations ser på participants over time og kræver delt state, herunder både conversation state og lokale projektioner, så man kan definere rules/ordering, lave reel error handling og sikre consistency. Det gør designet sværere, når du designer en protocol, skal undgå deadlocks, tænke completeness/termination, håndtere lifecycle ved crash/restart samt discovery/trust.

Forskellen mellem Publish-Subscribe og Subscribe-Notify er, at Publish-Subscribe handler om at route det enkelte event til alle subscribers, subscribe er en engangs composition, publish er runtime-mens Subscribe-Notify derimod handler om forholdet over tid: duration, lease/renewal og overlevelse ved genstarter.

---

## Question 8

*Also in Gregor Hohpe's video he explains the history and role of the idea of Patterns and Pattern Languages.<br>
How would you summarise what he explains – what do you see as the core requirements for patterns to be useful (see about 45 minutes in).*

---

### Hvad han forklarer:

Hohpe viser, at messaging er den fundamentale at tænke i distributed systemer på. Explicit channels giver rumlig og tidslig afkobling, begrænser error propagation og optimerer throughput. Men fordi runtime behavior ikke ligner code structure, bliver design sværere og netop derfor bruger vi patterns som et fælles sprog.

### Messaging → Conversations

Real processes er ofte dialoger med anmodning, kvittering og forhandling. Ser man over tid, så vil state og fejlretning blive centrale. Derfor skelner han mellem publish–subscribe som route selection for en enkelt besked og subscribe–notify som et varigt forhold med leases. Samtaler kan kædes, encapsulated i lag eller køre parallelt.

### Core requirements for useful patterns:

Hohpe peger på, at et brugbart pattern kræver mere end “a solution to a common problem in a context”. Core requirements er:

- **Recurring**:

    Mønstret skal være baseret på gentagne, virkelige problemer og ikke bare være opfundet bag skrivebordet

- **Forces**: 

    Det skal forklare hvorfor og hvordan løsningen afvejer dem og ikke bare “gør sådan”.

- **Name**

    Et klart, mindeværdigt navn gør det muligt at tænke, tale og designe hurtigere.

- **Human-to-human communication**

    Patterns skal kunne bruges som et fælles sprog mellem mennesker. Patterns er små enheder til menneskelig kommunikation, ikke code generatorer.

- **Context**

    Hvad er situationen, begrænsningerne og konsekvenserne? 
    Hvad virker, hvornår og hvad koster det?

- **Belonging to a language**

    Mønstret skal indgå i et pattern language med klare relationer som alternativer og komplementer, med komposition og med en navigerbar struktur fra makro til mikro med tydelige fremadrettede henvisninger, så designere kan kombinere mønstre uden at overse afgørende beslutninger.

- **Intent matters**

    Selv hvis to løsninger ser ens ud, kan de være forskellige patterns, hvis intentionen er forskellig (f.eks. proxy for anonymitet vs. proxy for policy-enforcement).

- **Evidence & examples**

    Vis at mønstret lever i moderne platforme (Kafka, Pub/Sub, SQS, serverless) og kan implementeres uden unødig kompleksitet.

### Hvorfor har det betydning?

Når de krav er opfyldt, hjælper patterns os med at kombinere løsninger til robuste conversations og systemer uden at forveksle abstraction med farlig illusion.

---

## Question 9

*In Simon Rohrer's article on modern enterprise architecture (https://modernenterprisearchitecture.substack.com/p/modern-enterprise-architecture-a also on Moodle in the folder for slides for this week) he goes in to more detail about the ABCDE of modern EA he discusses the 'strangler' pattern for moving away from legacy systems – why is this seen as a complex problem and what does the strangler pattern do to help?*

---

At bevæge sig væk fra legacy-systemer ses som et komplekst problem, fordi de ofte er monolitiske, rigide og tæt knyttede til forretningen, med begrænset tilpasningsevne til moderne krav som cloud-integration og hyppige, agile ændringer. Det fører til høje vedligeholdelsesomkostninger, integrationsudfordringer og en betydelig risiko for driftsforstyrrelser under udskiftning.

Strangler pattern hjælper ved at erstatte legacy-funktionalitet step by step, hvor man encapsulate det gamle system bag en facade/gateway, bygger nye komponenter omkring core og redirects gradvist trafikken, mens forældede dele fjernes. Herved undgår man en big-bang-omskrivning, reducerer risikoen, minimerer nedetid og muliggør løbende modernisering.

---

## Question 10

*In Jesper Lowgren's video Solution vs Enterprise Architecture Tutorial he describes three core diagrams that can be used to describe an architecture.<br>
What are they and what role do the play?<br>
Include examples.*

---

De tre core diagrams der beskrives af Jesper Lowgren i Solution vs Enterprise Architecture Tutorial er:

1. **Solution Overview**:
   
   Rolen for dette diagram er at oversætte business requirements til et forretningsvenligt billede af løsningen. Den fanger core processes og hvordan mennesker, systemer og teknologi interagerer. Den skal være forståelig for virksomhedens interessenter.

   Hvad den typisk kan indeholde er f.eks.:
   - Key use cases / user journeys
   - A conceptual architecture of actors → processes → systems

2. Landscape Diagram:

    Rolen for dette diagram er at vise hvordan hvordan applikationer og data stores integrate og interagerer. Den bruges til impact analyse, dependency mapping, og planning.

    Hvad den typisk kan indeholde er f.eks.:
    - Applikationer, databaser, integrationer.
    - Interfaces (REST, events, files), data contracts, og directions of flow

3. Solution Design:
    
    Rolen for dette diagram er at agere som et blueprint for udvikling og implementering. Den beskriver konteksten på tværs af mennesker, processer, data, applikationer, teknologi og etc.

    Hvad den typisk kan indeholde er f.eks.:
    - Application architecture: apps, komponenter og services, deres grænseflader.
    - Data architecture: data stores/tables og relationships
    - Teknologi og infrastruktur: cloud/on-prem, networks, runtime platforms. Her kunne reference architectures også indgå for at align med standarder.
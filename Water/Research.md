# Research Water 
## Ontsmetten van mixreservoir 
Heel wat oplossingen voor het ontsmetten/zuiveren van het mixreservoir is duur en niet meteen beschikbaar.

Een zandfilter is een effectief systeem, maar moet regelmatig vervangen worden en brengt mogelijks hoge onderhoudskosten met zich mee.

Het gebruik van UV-C lampen, is effectief, onderhoudsvriendelijk en heeft een levensduur van 8000 uur wat goed is voor onze toepassing. Voor een effectieve werking mikken we op een golflengte tussen de 254 en 265 nm.

Voor de UV-C ontsmetting zijn er drie mogelijke plaatsingen besproken:

1. Boven alle reservoirs
  - Voordeel: Eén lamp kan meerdere reservoirs ontsmetten.
  - Nadeel: Grotere afstand en minder afscherming zorgen voor lagere effectiviteit en verhoogd risico op blootstelling van mens en dier aan schadelijk licht. Ook zou dit de levensduur van de tubes verlagen.

2. In het mengreservoir
  - Voordeel: Direct contact met het meest besmette water.
  - Nadeel: Enkel het mengreservoir wordt gezuiverd, en er is geen interne reflectie die de effectiviteit verhoogt.

3. Extern via tubes
  - Voordeel: Veelzijdig inzetbaar met pompsystemen en maakt gebruik van interne reflectie, wat zorgt voor een efficiëntere werking.
  - Nadeel: Meer externe hardware en coördinatie nodig, wat de kosten verhoogt.

Bij de keuze van de lamp houden we rekening met het benodigde vermogen, gebaseerd op het volume van de reservoirs en de concentratie voedingsstoffen. We streven naar een vermogen van ongeveer 10 watt.
Wij hebben gekozen voor optie 2, in het mengreservoir. Dit was het beste te implementeren in ons systeem. 

Ten slotte wensen we de lamp aan te sturen via een PCB met ESPHome, gekoppeld aan Home Assistant. Hiervoor kiezen we bewust voor een eenvoudige lamp zonder ingebouwde timer, die via een relais en schakelaar kan worden bestuurd.

De eerst bestelde UVC-lamp via AliExpress gaf problemen: deze ontplofte al na zeven minuten gebruik. Dit onderstreept het belang van kwaliteitsvolle componenten en betrouwbare leveranciers.

## Waterniveau Sensor

Er zijn verschillende opties voor waterniveau meting:

| Kenmerk | Waterniveau Sensor | DFRobot Contactloze Sensor | Ultrasone Sensor |
|---------|--------------------|--------------------------|-----------------|
| Meetprincipe | Weerstand (direct contact) | Capacitief (contactloos) | Ultrasoon geluid |
| Contactloos? | Nee | Ja | Ja |
| Output | Analoog | Digitaal | Analoog |
| Meetbereik | Verschillende niveaus | Alleen "aan/uit" detectie | 2-450 cm |
| Nauwkeurigheid | Afhankelijk van vloeistofconductiviteit en corrosie | Betrouwbaar, maar geen niveau-indicatie | 3mm |
| Geschikt voor alle vloeistoffen? | Nee, alleen geleidende vloeistoffen | Ja | Ja |
| Corrosiegevoelig? | Ja | Nee | Nee |
| Prijs | Goedkoop | Duurder | 1-3 euro |
| Toepassing | Waterniveau meten | Vloeistofniveau detecteren zonder contact | Zeer nauwkeurig vloeistofniveau opmeten |

Zie onderstaande links voor verschillende sensoren:
- [Waterniveau Sensor](https://www.tinytronics.nl/nl/sensoren/vloeistof/waterniveau-sensor)
- [DFRobot Contactloze Sensor](https://www.tinytronics.nl/nl/sensoren/vloeistof/dfrobot-gravity-contactloze-vloeistofniveau-schakelaar-sensor)
- [Ultrasone Sensor](https://www.tinytronics.nl/en/sensors/distance/ultrasonic-sensor-hc-sr04)

We kozen voor de ultrasone sensor. De waterniveausensor was ook een goede keuze maar leek ons toch net niet helemaal geschikt. Beiden hebben nadelen en voordelen.

## Mixer
Er zijn verschillende opties voor watercirculatie:

- *Aquariumpomp*  
  - Voordelen: Sterke circulatie  
  - Nadelen: turbulentie veroorzaken en kan verstopt geraken  

- *Luchtpomp + luchtsteen*  
  - Voordelen: Zachte menging, weinig energieverbruik  
  - Nadelen: Trage menging en schuimvorming  

- *Mechanische mixer*  
  - Voordelen: Efficiënt mengen zonder veel turbulentie  
  - Nadelen: Mechanisch => onderhoud nodig  

We kozen voor een luchtpompje bij de reservoirs beneden. Dankzij een luchtsteen zal het water voldoende gecirculeerd worden.

Voor het reservoir kozen we een aquariumpompje. Dit heeft niet veel water nodig om een voldoende turbulente stroom te voorzien die het water mengt. Dit pompje sturen we aan op basis van de hoogte in dit bovenste reservoir.

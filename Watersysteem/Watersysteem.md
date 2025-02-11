# Watersysteem
## Plan
![Schematische tekening van het watersysteem](./assets/Schema_Watersysteem.png)

Het systeem bestaat uit onderstaande componenten, aan elkaar gekoppeld:

- **Reservoirs**:
1 waterreservoir & 1 voedingsstofreservoir. Uiteindelijk wordt het gerecycleerde water uit het systeem teruggebracht in dit waterreservoir.  
Beide reservoirs worden aangevuld door een klep te openen aan de kast en hebben een sensor om de hoogte van de vloeistof op te meten.

- **Pompen**:
1 pomp voor het water omhoog te pompen en 1 pomp voor de voedingsstof omhoog te pompen.

- **Mengreservoir**:
Hierin worden de voedingsstoffen gemengd met het water.  
Dit reservoir bevat dus een mixer, eventuele sensoren om de concentratie voedingsstoffen te meten en een sensor om de hoogte van de vloeistof op te meten.

- **Ventielsysteem**:
Dit bevat zoveel ventielen als er bevestigingsplaatsen zijn voor de plantenmodules. Het laat toe om per module water te voorzien, eventueel telkens met eigen verhoudingen van voedingsstoffen.

- **Common connector**:
Deze aansluitingen zijn de verbinding tussen het interne watersysteem en de plantenmodules. Hiermee wordt eveneens de stroom doorgegeven.  
Er is een verbinding om het water naar de plantenmodule te brengen. Ook is er een retourverbinding om de wateroverschot te recycleren.

- **UV-filter**:
Het gerecycleerde water passeert door een UV-filter om algengroei te voorkomen. Hierna stroomt het verder naar het waterreservoir.

## Reservoirs
![Reservoir](./assets/reservoir.JPEG)
We hergebruiken enkele van de bloembakken als reservoir. Deze zijn ruim genoeg en kunnen makkelijk geïntegreerd worden in het ontwerp.

## Sensoren en Actuatoren

### Waterpomp

![Waterpomp](./assets/Waterpomp.jpg)

De [waterpomp](https://www.tinytronics.nl/nl/mechanica-en-actuatoren/motoren/pompen/waterpomp-12v) heeft een maximale spanning van 12VDC en gebruikt ~400mA (= 4,8W). Het heeft een maximale opvoerhoogte van 3m en aanzuighoogte van 1,5m. Deze is geschikt voor slangen met ongeveer 6mm binnendiameter.

### Magneetventiel

![Magneetventiel](./assets/Magneetventiel.jpg)

Het [magneetventiel](https://www.tinytronics.nl/nl/mechanica-en-actuatoren/solenoids/magneetventielen/magneetventiel-normaal-gesloten-12v-dc-nylon-6mm) heeft een maximale spanning van 13VDC (12VDC aangeraden) met een gemiddeld stroomverbruik van ~300mA (= 3,6W). Deze is geschikt voor slangen met 6mm binnendiameter en is normaal gesloten (NC).

### Mixer

Er zijn verschillende opties voor watercirculatie:

- **Dompelpomp**  
  - Voordelen: Sterke circulatie  
  - Nadelen: Kan schuim of turbulentie veroorzaken  

- **Luchtpomp + luchtsteen**  
  - Voordelen: Zachte menging, weinig energieverbruik  
  - Nadelen: Lichte menging  

- **Mechanische mixer**  
  - Voordelen: Efficiënt mengen zonder veel turbulentie  
  - Nadelen: Mechanisch => onderhoud nodig  

### NO3- Sensor

![NO3- Sensor](./assets/Voedingsstofsensor.png)

De [NO3- Sensor](http://www.measureteq.com/electrode-and-sensor/ion-selective-electrode/ise-2922-no3-nitrate-ion-selective-electrode.html) wordt aangesloten met een BNC-connector.

### Ca2+ Sensor

![Ca2+ Sensor](./assets/Voedingsstofsensor.png)

De [Ca2+ Sensor](http://www.measureteq.com/electrode-and-sensor/ion-selective-electrode/ise-2923-calcium-ion-selective-electrode-ise.html) wordt aangesloten met een BNC-connector.

### K+ Sensor

![K+ Sensor](./assets/Voedingsstofsensor.png)

De [K+ Sensor](http://www.measureteq.com/electrode-and-sensor/ion-selective-electrode/ise-2920-potassium-ion-selective-electrode.html) wordt aangesloten met een BNC-connector.

### UV licht

Een gebruiksklare oplossing is zeer duur en niet direct beschikbaar. We zouden een eigen UV-filter kunnen maken door de tube langsheen een UV-ledstrip te laten gaan.  
De effectiviteit van deze filter zou zelfs beter kunnen zijn als we de leds ook boven het waterreservoir hangen. Op deze manier komt het water gedurende een langere periode in contact met het UV-licht.  
Voorbeeld: [UV LED-strip](https://www.amazon.com.be/-/nl/MASUNN-ultraviolet-violet-zwart-lichtstrip/dp/B077G5TS62)  
Deze moet een golflengte hebben tussen de 254-265nm.

### Waterniveau Sensor

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

## Common Connector

![Common Connector](./assets/Common_connector.png)

De common connector heeft 2 wateraansluitingen: WATER IN en WATER UIT. Deze worden elk voorzien met Quick-disconnects om makkelijk nieuwe plantenbakmodules aan te sluiten of te verwijderen.

# Watersysteem
## Plan
![Schematische tekening van het watersysteem](/assets/Schema_Watersysteem.png)

## Sensoren and Actuatoren

### Waterpomp

![Waterpomp](/assets/Waterpomp.jpg)

De [waterpomp](https://www.tinytronics.nl/nl/mechanica-en-actuatoren/motoren/pompen/waterpomp-12v) heeft een maximale spanning van 12VDC en gebruikt ~400mA (= 4,8W). Het heeft een maximale opvoerhoogte van 3m en aanzuighoogte van 1,5m. Deze is geschikt voor slangen met ongeveer 6mm binnendiameter.

### Magneetventiel

![Magneetventiel](/assets/Magneetventiel.jpg)

Het [magneetventiel](https://www.tinytronics.nl/nl/mechanica-en-actuatoren/solenoids/magneetventielen/magneetventiel-normaal-gesloten-12v-dc-nylon-6mm) heeft een maximale spanning van 13VDC (12VDC aangeraden) met een gemiddeld stroomverbruik van ~300mA (= 3,6W). Deze is geschikt voor slangen met 6mm binnendiameter en is normaal gesloten (NC).

### Mixer

TBD

### NO3- Sensor

![NO3- Sensor](/assets/Voedingsstofsensor.png)

De [NO3- Sensor](http://www.measureteq.com/electrode-and-sensor/ion-selective-electrode/ise-2922-no3-nitrate-ion-selective-electrode.html) wordt aangesloten met een BNC-connector.

### Ca2+ Sensor

![Ca2+ Sensor](/assets/Voedingsstofsensor.png)

De [Ca2+ Sensor](http://www.measureteq.com/electrode-and-sensor/ion-selective-electrode/ise-2923-calcium-ion-selective-electrode-ise.html) wordt aangesloten met een BNC-connector.

### K+ Sensor

![K+ Sensor](/assets/Voedingsstofsensor.png)

De [K+ Sensor](http://www.measureteq.com/electrode-and-sensor/ion-selective-electrode/ise-2920-potassium-ion-selective-electrode.html) wordt aangesloten met een BNC-connector.

### UV licht

Deze moet een golflengte hebben tussen de 254-265nm.

### Waterhoogte

[Deze soort](https://www.tinytronics.nl/en/sensors/liquid/water-level-sensor) waterhoogte sensoren kunnen gebruik worden, maar er moet opgepast worden aangezien de concentratie ionen en pH invloed hebben op de geleidbaarheid van het water. Hierdoor hangt de gelezen waarde niet enkel van de hoogte af, maar ook van de concentratie ionen en de pH van het water.

## Common Connector

![Common Connector](/assets/Common_connector.png)

De common connector heeft 2 wateraansluitingen: WATER IN en WATER UIT. Deze worden elk voorzien met Quick-disconnects om makkelijk nieuwe plantenbakmodules aan te sluiten of te verwijderen.
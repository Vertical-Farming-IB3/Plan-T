---

## Research en vergelijking van sensoren

In deze sectie vergelijken we enkele van onze gekozen sensoren met alternatieve opties, op basis van nauwkeurigheid, prijs, beschikbaarheid, duurzaamheid en gebruiksgemak. Op basis van deze vergelijkingen motiveren we ook telkens onze keuze.

---

### Luchtsensor (GY-SCD40)

#### Vergelijking met alternatieven:

| Sensor         | Parameters                   | Voeding | Interface | Nauwkeurigheid | Prijsindicatie | Opmerkingen |
|----------------|------------------------------|---------|-----------|----------------|----------------|-------------|
| GY-SCD40       | CO₂, temperatuur, vochtigheid| 3.3V/5V | I²C       | Hoog           | Hoog           | Compact, snel, nauwkeurig |
| MH-Z19B        | CO₂                          | 5V      | UART      | Matig          | Gemiddeld      | Alleen CO₂, trager, minder stabiel |
| CCS811         | eCO₂, TVOC                   | 3.3V    | I²C       | Laag tot gemiddeld | Laag        | Indirecte CO₂, inferieur aan GY-SCD40 |

Zie onderstaande links voor verschillende sensoren:
- [GY-SCD40](https://www.tinytronics.nl/nl/sensoren/lucht/vochtigheid/gy-scd40-module-co2-luchtvochtigheid-en-temperatuursensor-i2c)
- [MH-Z19B](https://www.tinytronics.nl/nl/winsen-mh-z19b-co2-sensor-met-kabel)
- [CCS811](https://www.adafruit.com/product/3566)

#### Voordelen:
- Hoge nauwkeurigheid  
- Meet drie parameters tegelijk  
- Compact en efficiënt  

#### Nadelen:
- Duurder  
- Heeft enkele seconden opwarmtijd nodig  

**Keuze-motivatie:** Ondanks de hogere kostprijs is de SCD40 superieur door de combinatie van nauwkeurigheid, snelheid en veelzijdigheid. Dankzij hergebruik van een vorig project was er bovendien geen extra kost.

---

### NFC-lezer (PN532)

#### Vergelijking met alternatieven:

| Sensor         | Interface     | Bereik | Compatibiliteit       | Prijsindicatie | Opmerkingen |
|----------------|---------------|--------|------------------------|----------------|-------------|
| PN532          | I²C/SPI/UART  | ~3 cm  | ISO/IEC 14443 A/B      | Gemiddeld       | Veelgebruikt, goede bibliotheekondersteuning |
| RC522          | SPI           | ~2 cm  | ISO/IEC 14443 A        | Laag            | Korter bereik, minder robuust |
| MFRC630        | SPI/I²C       | ~5 cm  | 14443 A/B + NFC Forum  | Hoog            | Sneller en flexibeler, maar duurder en minder ingeburgerd |

Zie onderstaande links voor verschillende sensoren:
- [PN532](https://www.tinytronics.nl/en/communication-and-signals/wireless/rfid/rfid-nfc-kit-pn532-with-s50-card-and-s50-key-tag)
- [RC522](https://www.tinytronics.nl/nl/communicatie-en-signalen/draadloos/rfid/rfid-kit-mfrc522-s50-mifare-met-kaart-en-key-tag)
- [MFRC630](https://gr.mouser.com/c/semiconductors/wireless-rf-integrated-circuits/nfc-rfid-tags-transponders/?m=NXP&series=MFRC630)
  
#### Voordelen:
- Brede ondersteuning, meerdere protocollen  
- Betrouwbaar en compatibel met ESP  
- Goede bibliotheekondersteuning  

#### Nadelen:
- Duurder dan RC522  
- Groter formaat  

**Keuze-motivatie:** De PN532 was beschikbaar op de campus en heeft een goede compatibiliteit met ESP32 en ESPHome. Daardoor was het de beste keuze voor snelle implementatie.

---

### Energiemonitoring (ACS712)

#### Vergelijking met alternatieven:

| Sensor         | Meetprincipe     | Meetbereik | Interface | Nauwkeurigheid | Prijsindicatie | Opmerkingen |
|----------------|------------------|------------|-----------|----------------|----------------|-------------|
| ACS712         | Hall-effect       | ±5A/20A/30A| Analoog   | Gemiddeld       | Laag           | Beperkte resolutie, gevoelig aan ruis |
| INA219         | Shunt + ADC       | Tot 3.2A   | I²C       | Hoog            | Gemiddeld      | Beter voor lage stromen, nauwkeuriger |
| SCT-013        | Transformatorspoel| 100A       | Analoog   | Laag tot gemiddeld | Laag        | Alleen AC, extra burden resistor nodig |

Zie onderstaande links voor verschillende sensoren:
- [ACS712](https://www.tinytronics.nl/nl/sensoren/stroom-spanning/acs712-stroomsensor-module-20a)
- [INA219](https://www.tinytronics.nl/en/sensors/current-voltage/ina219-i2c-dc-current-and-voltage-meter-3.2a-module)
- [SCT-013](https://www.tinytronics.nl/nl/sensoren/stroom-spanning/ac-stroom-sensor-sct013-030-30a)

#### Voordelen:
- Simpel aan te sluiten (analoog)  
- Meet zowel AC als DC  
- Goedkoop en goed beschikbaar  

#### Nadelen:
- Gevoelig voor ruis  
- Lage resolutie, niet geschikt voor hele kleine stromen  

**Keuze-motivatie:** Omdat het systeem op lage stroom werkt, was de ACS712 accuraat genoeg voor onze noden. Bovendien had een teamlid deze sensor al thuis liggen, waardoor we dus budget konden sparen.

---

### Bodemsensor (Capacitive Soil Sensor v2)

#### Vergelijking met alternatieven:

| Sensor                    | Meetprincipe         | Interface | Waterbestendig | Levensduur | Prijsindicatie | Opmerkingen |
|---------------------------|----------------------|-----------|----------------|------------|----------------|-------------|
| Capacitive Soil Sensor v2 | Capacitatief         | Analoog   | Spatwaterdicht | Gemiddeld  | Laag            | Goede optie voor hydroponics |
| Resistive sensor (YL-69)  | Weerstandsmeting     | Analoog   | Nee            | Laag       | Zeer laag       | Roest snel, onnauwkeurig |
| DFRobot SEN0193           | Capacitief digitaal  | UART/I2C/analog  | Waterdicht | Zeer goed  | Hoog (± €25–€35)| Professionele sensor, waterdicht, nauwkeurig |

Zie onderstaande links voor verschillende sensoren:
- [v2](https://www.tinytronics.nl/en/sensors/liquid/capacitive-soil-moisture-sensor-module-with-cable)
- [YL-69](https://nl.aliexpress.com/item/1005004305871722.html)
- [DFRobot SEN0193](https://be.farnell.com/dfrobot/sen0193/analog-capacitive-soil-moisture/dp/2946124?srsltid=AfmBOooL5i8PC0d12YCaEzV8PJMQsMimocrb--_qA2ahPNOhw57yElFl)


#### Voordelen:
- Capacitatieve meting is nauwkeuriger dan resistieve  
- Redelijk bestand tegen vocht  
- Werkt goed met ESPHome  

#### Nadelen:
- Niet volledig waterdicht  
- Niet geschikt voor diepe grondlagen  

**Keuze-motivatie:** Voor hydroponics volstaat een gemiddelde nauwkeurigheid. Deze sensor was reeds aanwezig in de klas en biedt een goed evenwicht tussen betrouwbaarheid en kost.

---

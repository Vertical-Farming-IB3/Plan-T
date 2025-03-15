# PCB Watersysteem

In dit document sommen we de requirements op voor de PCB.

## Inputs
- Analoog (x3) voedingstoffen => via 1 ADC (ADS1115) met BNC connectoren voor de probes
- Analoog (x3) Ultrasone hoogtesensoren (HC-SR04)
- Digitaal (x3) eindeloopschakelaars

## Outputs
- Digitaal LED indicator waterniveau
- Digitaal LED indicator voedingsstofniveau
- Relais UV lamp (230V/100mA)
- Relais mixer pompje (3V/200mA) of (6V/200mA)
- Relais pompjes lade en reservoirs (4x) (12V/400mA)
- Relais luchtpomp (12V/220mA)



# Power inputs

12V DC / 3A

230V AC / 100mA

Dit wordt op de PCB door een buck converter (MP1584) van 12V naar 5V omgezet voor de relais. De 5V wordt verder omgevormd naar 3.3V door een LDO (AMS1117) voor de ESP32.
## Vermogen 12V
- 4x pompje van 400mA
- 1x luchtpomp 220mA
- 1x mixer pompje 100mA
- relais (200mA bij 5V) => 100mA
- Buck converter (1500mA bij 5V) => 800mA

Afgerond maakt dit 3000mA bij 12V
=> P = 40W

# Pinout
Nummers: ESP32

A/B: IO expander
IO expander is met I2C verbonden met de ESP32

### LEDs
Pin| Description
---|------------
2  | Onboard LED (IO2)
A7 | Nutriënten LED (IO2)
B0 | Nutriënten LED (IO2)

### Hoogtesensoren (ultrasoon)
Pin| Description
---|------------
26 | Trigger Hoogtesensor Nutr
25 | Echo Hoogtesensor Nutr
33 | Trigger Hoogtesensor Water
32 | Echo Hoogtesensor Water
14 | Trigger Hoogtesensor Mix
27 | Echo Hoogtesensor Mix

### Eindeloopschakelaars
Normaal open

Open = Hoog, Gesloten = Laag

 Pin | Description
-----|------------
 B1  | Schakelaar 1
 B2  | Schakelaar 2
 B3  | Schakelaar 3

### Relais

 Pin | Description
-----|------------
 A0  | Mixer
 A1  | UV lamp
 A2  | Luchtpomp
 A3  | Pomp 4
 A4  | Pomp 3
 A5  | Pomp 2
 A6  | Pomp 1

### Backup IO

Pin| Description
---|------------
B4 | B4
B5 | B5
B6 | B6
B7 | B7


### IO expander
I2C adres: 0X27

herinstelbaar via JP1, JP2 en JP3 (verbind de jumpers voor een 0, ze zijn standaard 1):
0b0100\<JP1>\<JP2>\<JP3>


### ADC en probes
I2C adres: 0x48 \
Verbind JP4 voor adres 0x49

Pin| Description
---|------------
A0 | Nutriënten 3
A1 | Nutriënten 2
A2 | Nutriënten 1
A3 | Referentie

Testpunten zijn aangeduid op de PCB
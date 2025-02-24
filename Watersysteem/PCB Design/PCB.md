# PCB Watersysteem

In dit document sommen we de requirements op voor de PCB.

## inputs
- Analoog (x3) voedingstoffen => via 1 ADC (ADS1115)
- Analoog (x3) Hoogtesensoren
- Digitaal (x3) eindeloopschakelaars

## outputs
- Digitaal LED indicator waterniveau
- Digitaal LED indicator voedingsstofniveau
- Relais UV lamp (230V/100mA)
- Relais mixer pompje (3V/200mA) of (6V/200mA)
- Relais pompjes lade en reservoirs (4x) (12V/400mA)
- Relais luchtpomp (12V/220mA)



# Power inputs

12V DC / 3A

230V AC / 100mA

## Vermogen 12V
- 4x pompje van 400mA
- 1x luchtpomp 220mA
- 1x mixer pompje 100mA
- relais (200mA bij 5V) => 100mA
- Buck converter (1500mA bij 5V) => 800mA

afgerond 3000mA bij 12V
=> P = 40W
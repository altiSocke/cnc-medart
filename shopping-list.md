# Shopping List


| Category | Item | Item Price | Quantity | Total $ |
|----------|------|------------|----------|---------|
| [Controller](#controller)    | [mesanet 7I96S](https://store.mesanet.com/index.php?route=product/product&product_id=374) | 149$ | 1 | 149$|
| [Driver](#driver)        |[DM856](https://www.reichelt.com/ch/de/shop/produkt/schrittmotortreiber_nema_23_34_24_-_80_v_5_6_a_2_4-phasig-285311) | 3 | 38.82 | 116.46 |
| [Power Supply](#power-supply)  |  |  |  |  |
| [Misc](#misc)          |  |  |  |  |

## Controller

[mesanet 7I96S](https://store.mesanet.com/index.php?route=product/product&product_id=374)

## Driver

### Steppers
Key Specifications:

Nema 23
Voltage: 3.52 V DC
Current: 3.3 A DC
Wattage: V * A = 11.616 W
Vfmax : 65 Vrms
Po: 104 W
Type: Unipolar: This refers to the type of motor winding configuration, which is simpler to drive than bipolar motors but may have slightly lower performance.

Total Power 3x: 34.84 W ()
Po 3x = 312 W 
Total Power 4x: 46.464 W 
Po 4x = 416 W


8 Pin Unipolar Driver? not a thing. Leadshines and other drivers are 4 lead configurations. 

8 to 4 lead configurations: 
[8 lead](https://www.pololu.com/docs/0J88/4)


1. Series Connection:
Higher Torque, Lower Speed:
Wiring: Connect the two windings of each phase in series.   
Driver: You can use a 4-lead driver, but you'll need to adjust the current and voltage settings to account for the higher resistance of the series-connected windings.
1. Parallel Connection:
Higher Speed, Lower Torque:
Wiring: Connect the two windings of each phase in parallel.   
Driver: A 4-lead driver can be used, but again, you'll need to adjust the current and voltage settings to handle the lower resistance of the parallel-connected windings.

Choosing the Right Configuration:

The best configuration depends on your specific application requirements. Consider the following factors:

- Torque: If you need high torque, the series connection is a good choice.
- Speed: If you need high speed, the parallel connection is a good choice.
Current and Voltage: Ensure your driver and power supply can handle the current and voltage requirements of the chosen configuration.
Motor Specifications: Consult the motor's datasheet for specific recommendations.


[cnc zone:](https://www.cnczone.com/forums/stepper-motors-drives/285128-connect-8-wire-stepper-motor-motion-control.html)

> You need to pair the 8 off into 4 wires, usual pairs are red and blue, black and yellow, brown and white, green and orange. Green orange pair goes with brown and white across one channel, and red and blue and black and yellow across other channel. By across I mean one to negative and one to positive. Doesn't matter which way around you wire them, if it goes the wrong direction then simply reverse the wires on one of the channels.

### Calculations

```
Power_supply_current = Motor_Power / (Driver_Efficiency * Power_supply_Voltage)
```
driver_efficiency = 80%
motor_power = 104 W
driver power_supply_voltage = 24 V
power_supply_current = 104 W / (0.8 * 24 V ) = 5.4 A

--> EM1-556

| Specification       | Details                        |
|---------------------|--------------------------------|
| Model               | EM1-556                        |
| Series              | EM                             |
| Command Source      | PUL&DIR, CW&CCW                |
| Operation Voltage   | 20-50 VDC                      |
| Output Current      | 5.6 A (Peak)                   |
| Input Frequency     | 200kHz, 500kHz Configurable    |
| Logical Voltage     | 5~24Vdc compatible             |
| # of Inputs         | 3                              |
| # of Outputs        | 2                              |
| Characteristics     | Standard                       |
| Specification       | Details                        |
|---------------------|--------------------------------|
| Model               | EM556S                         |
| Series              | EM                             |
| Command Source      | PUL&DIR, CW&CCW                |
| Operation Voltage   | 20-50 VDC                      |
| Output Current      | 5.6 A (Peak)                   |
| Input Frequency     | 200 kHz                        |
| Logical Voltage     | 5 or 24 VDC                    |


Parameters	DM856
| Parameter              | Min | Typical | Max  | Unit |
|------------------------|-----|---------|------|------|
| Output current         | 0.5 | -       | 5.6  (4.0 RMS)  | A    |
| Supply voltage         | 20  | -       | 80   | VDC  |
| Logic signal current   | 7   | 10      | 16   | mA   |
| Pulse input frequency  | 0   | -       | 200  | kHz  |
| Isolation resistance   | 500 | -       | -    | Mohm |


Conclusion: EM1-556 could not find supplier
[3x DM856](https://www.reichelt.com/ch/de/shop/produkt/schrittmotortreiber_nema_23_34_24_-_80_v_5_6_a_2_4-phasig-285311)


### Spindle
[MEZ MOHELNICE 4AP71-2](https://shop.pagus.eu/Workshop-Equipment/Blower-/fan/Centrifugal-fan-0-55-kW-2820-rpm::13233.html?XTCsid=3vimstnqmbeic2ism9tl3fu1o6)
550 W / 0.75 HP --> 220V 
```
550 W / 220 V = 2.5 A 
```

TODO: clarify it this has to be controllable by software, throttle through a potentiometer or just on/off by switch.


## Power Supply

Rule of thumb: 25% over total req.
3*104W * 1.25 = 390W
24V --> 16.25 A

e.g. [450W 24V 18.8A - 112 Euro](https://www.reichelt.com/ch/de/shop/produkt/schaltnetzteil_geschlossen_450_w_24_v_18_8_a-148050)
Technische Daten:
Ausgangsspannung: 24 V DC
Ausgangsspannungbereich: 21,3 - 28,8 V
Ausgangsstrom: 18,8 A
Leistung: 451 W
Restwelligkeit: 150 mVp-p
Eingangsspannung: 85 ~ 264 V AC / 120 ~ 370 V DC
Effizienz: 88%
Einschaltstrom, max.: 35 A/115 V AC / 70 A/230 V AC
Arbeitstemperatur: -40  +85 °C
Größe: 218 x 105 x 41 mm
Gewicht: 1,19 kg

## Misc

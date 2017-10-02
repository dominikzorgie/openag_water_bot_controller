on psoc4000 micro, for power config, using unregulated external supply
see fig 9 in datasheet
why are we using 1uF instead of 0.1uF?

what logic level i2c should we use?
psoc4000 provides a separate voltage domain for P3.0, P3.1, P3.2 via VDDIO
P3.0 and P3.1 are also SDAT and SCLK respectively
enables communicating w/system running at different voltage (VDDIO < VDD)
e.g. VDD can be 3.3V and VDDIO can be 1.8V
---never mind, the 16 pin SOIC does not have a VDDIO pin

what is the current draw on micro?..trying to spec voltage regulator
input voltage is 12V, output voltage is 3.3V
I_dd_11 max 4.5mA (when in active mode executing from flash w/cpu at 16mhz...see table 4)
Idiode max 100uA (table 6)
Itot_gpio max 85 mA (table 6)
spec regulator for >100mA

current draw on relay coil?
- @12VDC, 33.3mA



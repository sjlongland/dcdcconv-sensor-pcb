# Voltage/Current sensor board

This is a differential I²C voltage and current sensing board using the TI
INA219 power monitor IC and the NXP PCA9615 differential I²C controller.  This
is intended to provide a high-accuracy voltage and current measurement for the
[DC-DC converter
controller](https://github.com/sjlongland/dcdcconv-controller-pcb).

There is a footprint for an on-board current shunt (e.g. TT Electronics
LRMAP5930B-R0002FT) as well as a connector for an off-board one.  The board
also has footprints for two screw terminal blocks (Phoenix Contact "Combicon"
1706785) to interface the board to up to 6AWG cables for power input/output.

Four two-way jumpers allow full freedom in selecting the I²C address used by
the INA219 according to combinations of settings chosen from its data sheet.

The underside has exposed copper areas to allow additional stranded cable to
be soldered over the traces to enhance the current carrying capability.

## Parts list

* C1, C3: 100nF ≥10V ceramic capacitor 0805 SMD (localised decoupling)
* C2: ≥100µF ≥10V electrolytic capacitor 6.3mm SMD (bulk decoupling)
* (**FIT ONE ONLY**) C4, C5, C6, C7: 100pF ≥20V ceramic capacitor (0V AC
  decoupling capacitor to chassis.  Choose the capacitor that best suits your
  mounting arrangements.)
* U1: NXP PCA9615 differential I²C controller.
* U2: TI INA219BIDR power monitor.
* R1, R6: (**NOT CONFIRMED**) 2k2 ohm 0805 SMD resistors (differential I²C
  pull-up)
* R4, R9: Spaces for additional pull-ups for differential I²C, do not fit
  unless found to be required.
* R5, R10: (**NOT CONFIRMED**) 2k2 ohm 0805 SMD resistors (differential I²C
  pull-down)
* R2, R7: Spaces for additional pull-downs for differential I²C, do not fit
  unless found to be required.
* R3, R8: (**NOT CONFIRMED**) 100 ohm 0805 SMD resistors (differential I²C
  termination)
* R12, R13: (**NOT CONFIRMED**) 2k2 ohm 0805 SMD resistors (I²C pull-up)
* J1: 6-pin 2.54mm "KK" connector (differential I²C bus)
* J2: 2-pin 2.54mm "KK" connector (external current shunt, **omit if fitting
  R11)

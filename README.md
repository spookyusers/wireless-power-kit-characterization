# wireless-power-kit-characterization
Educational reverse engineering and characterization of a low-cost wireless power transmission kit (resonant inductive / capacitive coupling).

## Objective
To understand how this kit works by measuring key parameters (power, frequency, range, efficiency), documenting the circuit, and sharing findings for educational purposes.

## Kit Overview
- Low-power (3-4.5V DC input) wireless power transfer kit (part of one of the Poraxy STEM kits).
- Demonstrates short-range wireless energy transfer: transmitter powers a resonant coil / antenna structure; receiver lights LEDs without its own power source.
- Two main units: transmitter (TX) with battery pack and driver circuit; receiver (RX) passive with LEDs.

### Transmitter (TX) Side
- Powered by a 3-AAA battery pack (black box with switch, red/black wires).
- Green PCB with:
  - NPN transistor marked BCP55 (pins labeled B/C/E).
  - Surface mount components including resistors (e.g. marked "810", "223" or similar), and red LED.
- Blue 3-pin screw terminal block labeled (in Chinese):
  - primary lower end
  - primary upper end
  - secondary coil (black wire soldered to bottom of coil)
- Primary coil: thicker insulated copper wire, ~2-3 turns around base of transmitter coil/antenna tube.
- Resonant coil: thin copper wire densely wound (~240 turns estimated over ~8cm length) on plastic tube, with thin wire protruding from top (likely for field emission).
- Wooden base for mounting.

### Receiver (RX) Side
- No battery or external power input; fully passive.
- Similar plastic tube with densely wound thin copper wire resonant coil (~240 turns estimated, identical appearance to TX).
- ~10-turn wire (possibly enameled but not obvious from color) wound at base.
- Green PCB with:
  - IC marked MB14F (likely bridge rectifier)
  - Ceramic capacitor, SMD resistor (marked "810").
  - Red LED
  - Connector for external white LED (under decorative lampshade).
- Blue 3-pin screw terminal block (similar layout to TX):
  - One black wire soldered to base/bottom of resonant coil.
  - Other twi pins for the ~10-turn base coil.
- Wooden base for mounting

### Observed Behavior (Initial)
- TX: Red LED lights instantly when powered, no sound, no visible oscillation or sparks or anything.
- RX: Red PCB LED + white lampshade LED light only when placed near TX
  - Red LED lights dimly at ~25cm
  - White lamphsade LED lights at ~18cm.
  - Rotating TX or RX components changes the intensity, with a 180 degree rotation completely eliminating transmission (both RX LEDs go dark).

## Tools and Equipment (Planned/Used)
- Digital multimeter
- Ruler (regular wooden 12-inch type for now)
- Phone camera for shots and reading small print on PCB/ICs
- Oscilloscope for frequency analysis

## Progress Log
See [progress-log.md](progress-log.md) for dated entries, measurements, and observations.

  

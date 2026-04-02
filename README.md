# Expression Pedal to CV Converter - Printable PCB

![PCB Layout](/images/PCB.png)

This design is meant to take the input of a standard expression pedal (typical type compatible with BOSS and other pedals with a TRS plug), and convert it to a CV (0-5V) output (TS). My primary reason for creating this is to be able to use a regular, $20(?) passive expression pedal with a Behringer Dual-Phase. The Dual-Phase is a clone of the Mu-Tron Bi-Phase (_"I put that sh*t on everything!" - Butch Vig_). The original version came with its own proprietary expression pedal that used a DIN plug. Behringer decided that for their version they would prioritize control by an external synthesizer, for some reason. So anyone using this as a guitar pedal is left asking where we can get active CV expression pedals, but they cost 2.5X the price of the Dual-Phase itself.

So this will take a 9V power input, your regular expression pedal input, and output CV, from 0 to 5V, swept by the movement of your pedal.

## Coming soon

3D Printable Enclosure

Updates to board silk-screening - I didn't realize those capacitor values are hard to find as alumin(i)um electrolytics

# Bill of Materials — v1.0

---

## Components

| Ref | Qty | Value | Description | Manufacturer | MPN | Supplier | Supplier PN |
|-----|-----|-------|-------------|--------------|-----|----------|-------------|
| U1 | 1 | 78L05 | IC, LDO Voltage Regulator, 5V, 100mA, TO-92-3 | Texas Instruments | LM78L05ACZ/NOPB | DigiKey | LM78L05ACZNS/NOPB-ND |
| D1 | 1 | 1N5817 | Diode, Schottky, 20V, 1A, DO-41 | SMC Diode Solutions | 1N5817 | DigiKey | 1655-1N5817TR-ND |
| C1 | 1 | 0.33 µF | Cap, Film (PET), 0.33 µF, ±10%, 63V DC, Radial, 2.50mm pitch | WIMA | MKS0C033300D00KSSD | DigiKey | 1928-1614-ND |
| C2 | 1 | 0.1 µF | Cap, Ceramic (X7R), 0.1 µF, ±10%, 50V DC, Radial, 2.54mm pitch | KEMET | C315C104K5R5TA | DigiKey | 399-C315C104K5R5TA-ND |
| J1 | 1 | 5.5x2.1mm | DC Barrel Jack, Panel Mount. 5.5x2.1mm | Too expensive on DigiKey - Check Amazon |
| J2 | 1 | 6.35mm | TRS Stereo Jack, Panel Mount | Check Amazon |
| J3 | 1 | 6.35mm | TS Mono Jack, Panel Mount | Check Amazon |

---

## Notes

- **C1** replaces an electrolytic footprint with a WIMA MKS02 film capacitor. Body dimensions: 4.60 × 3.80mm, 2.50mm lead pitch — compatible with the PCB's 2.50mm radial pads. Polarity doesn't matter with this replacement.
- **C2** replaces an electrolytic footprint with a KEMET X7R ceramic capacitor. Lead pitch is 2.54mm, which is compatible with 2.50mm pads in through-hole assembly. Polarity doesn't matter for this replacement either.
- **J1** is used to connect the DC power input. Don't forget that guitar pedal connectors are center negative! You may buy an already wired jack on Amazon and you'll need to remember that the red and black wires may not be + and - respectively.
- **J2–J3** are generic 2.54mm male pin headers. I did not intend for the 6.35mm (1/4") jacks to be mounted directly to the board, so solder 22AWG stranded wire to connect the jacks.
- All DigiKey stock levels confirmed in-stock as of 2026-04-01.

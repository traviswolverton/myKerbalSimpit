# myKerbalSimpit — Bill of Materials

Extracted from the "Parts List" title block in `KSP+Controller+Assembly+Drawing.pdf`.

## Purchase list (electromechanical parts)

| Qty | Part |
|---|---|
| 1 | Arduino Mega |
| 1 | MW RS-25-5 (Mean Well 5V power supply) |
| 1 | USB Type-B panel-mount connector |
| 1 | Power input switch |
| 2 | 30mm fan |
| 10 | 12mm switch |
| 1 | Slide potentiometer |
| 2 | 3-axis joystick, R400B-M4 v7 |
| 5 | 4-color LED bar |
| 20 | 6mm push button |
| 3 | 19mm LED push button — Red (large) |
| 3 | 19mm LED push button — Green |
| 2 | 19mm LED push button — White |
| 2 | 19mm LED push button — Blue |
| 2 | 19mm LED push button — Yellow |
| 1 | LED toggle switch, illuminated, covered, 12V — Red |
| 1 | LED toggle switch, illuminated, covered, 12V — Green |
| 7 | 5mm red LED |
| 11 | 5mm blue LED |
| 3 | 5mm green LED |
| 1 | 5mm yellow LED |
| 1 | 5mm white LED |
| 23 | LED holder, RTF-5010, 5mm press-fit |
| 4 | SPDT print-switch (verify against build guide — may be a mechanism part, not off-the-shelf) |
| 118 | M3×5mm socket-head screw (McMaster 91290A115) |
| 10 | M2×5mm socket-head screw, black oxide (McMaster 91290A012) |

## 3D-printed / self-fabricated

STL files already included in `STL/`, no shopping needed beyond filament.

- Bottom Brace ×2
- Back Only Brace ×2
- Combo Brace ×1
- Combo Brace 2 ×1
- Action Group Panel ×1
- Fuel Display Panel ×1
- Joystick Panel ×1
- Menu Panel ×1
- SAS Plate ×1
- Stage Panel ×1
- Abort Panel ×1
- Throttle Panel ×1
- Top Panel ×1
- Front Panel ×1
- Rear Panel ×1
- Bottom Panel ×1
- Left Side Panel ×1
- Right Side Panel ×1
- Joining Plate ×17
- Joining Plate – Large ×1

## Electronics not covered by the Parts List (custom PCB)

The assembly drawing's Parts List does not include the PCB's own components. Pulled from
`Circuit Board/SCH_Schematic1_2024-05-04.pdf`, which shows the board built around:

- 74HC595 shift-out registers (drive the LEDs)
- 74HC165 shift-in registers (read the buttons/switches)
- A bank of current-limiting resistors (R1–R32)

Exact IC/resistor quantities were not reliably extractable from the schematic PDF text (CAD
export layout scrambles reading order), and the resistor value printed ("220kΩ") looks
suspiciously high for LED current-limiting (typically 220Ω–330Ω) — likely a mislabeled
default in the EasyEDA export. Verify counts and resistor value directly in EasyEDA or
visually in the schematic before ordering.

Cross-referencing `Drawn Wiring Diagram 1 - Shift Registers.jpg` (hand-drawn pre-PCB wiring
notes) suggests at least **4× 74HC165** (daisy-chained in banks of 8: 0-7, 8-15, 16-23, 24-31)
and **5× 74HC595** (daisy-chained 0-7 through 32-39) as a starting point, plus one
current-limiting resistor per LED (60+ total across the panel).

The bare PCB itself can be ordered directly from the Gerbers in
`Circuit Board/Gerber_PCB1_2024-05-04.zip` (fab notes reference JLCPCB, part number
JLCPCB-002 per the schematic title block).

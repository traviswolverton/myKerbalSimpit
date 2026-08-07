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
| 4 | SPDT toggle switch, panel-mount, non-illuminated, no cover (generic — no vendor SKU in source files) |
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

The assembly drawing's Parts List does not include the PCB's own components. These are
confirmed straight from `Circuit Board/Kerbal Controller.eprj` (EasyEDA Pro's native project
file, which is a plain SQLite database — queried directly rather than relying on the schematic
PDF's OCR-scrambled text):

| Qty | Part | Role |
|---|---|---|
| 8 | 74HC165N | Input shift register (reads buttons/switches) |
| 4 | 74HC595N | Output shift register (drives LEDs) |
| 32 | Resistor, 220kΩ, 1/4W, ±5% (MFR part `MO1/4W-220K±5%-ST52`), designators R1–R32 | See note below |

**Note on the resistors:** 220kΩ is unusually high for LED current-limiting (typically
220Ω–330Ω; 220kΩ at 5V is ~0.02mA, well below the ~1mA needed for visible glow). This is the
value genuinely specified in the project file, not a mislabeled CAD default — but it's worth
visually confirming in the schematic what these resistors actually connect to before ordering,
in case they're serving a different role (e.g. pull-ups/pull-downs on shift-register control
lines) rather than being in series with the panel LEDs.

The bare PCB itself can be ordered directly from the Gerbers in
`Circuit Board/Gerber_PCB1_2024-05-04.zip` (fab notes reference JLCPCB, part number
JLCPCB-002 per the schematic title block).

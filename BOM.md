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

### Sourcing notes

None of the switches/buttons/LEDs/joystick carry a vendor SKU in the source files (unlike the
McMaster screws above, which do) — the designer modeled placeholder shapes in Fusion 360
without recording where they bought the real parts. The links below are real, current listings
found via web search that match the drawing's specs — not a specific endorsed product, just a
starting point to compare on Amazon/McMaster/AliExpress yourself.

- **Arduino Mega** — genuine [Arduino Mega 2560 REV3](https://www.amazon.com/Arduino-ATmega2560-Compatible-Advanced-Projects/dp/B0046AMGW0) or any ATmega2560-compatible clone (ELEGOO, SainSmart, KEYESTUDIO all show up on Amazon).
- **MW RS-25-5** — this is a real Mean Well part number, sold at [DigiKey](https://www.digikey.com/en/products/detail/mean-well-usa-inc/RS-25-5/7706180), [Mouser](https://www.mouser.com/ProductDetail/MEAN-WELL/RS-25-5), and [Newark](https://www.newark.com/mean-well/rs-25-5/power-supply-ac-dc-5v-5a/dp/99AC4268). 5V/5A/25W AC-DC supply.
- **USB Type-B panel-mount connector** — generic part, e.g. [rectangular panel-mount USB-B connector](https://www.amazon.com/QIANRENON-Rectangular-Connector-Bulkhead-Mounting/dp/B0DG2MD5L4) (23×18.5mm cutout).
- **Power input switch** — since the RS-25-5 takes mains AC input, this is likely an IEC C14 inlet with integrated rocker switch (and often a fuse holder), e.g. [IEC 320 C14 inlet + rocker switch panel socket](https://www.amazon.com/Antrader-Rocker-Switch-Socket-Connector/dp/B07F2SWY56). Worth confirming panel cutout size against the STL before buying.
- **30mm fan** — standard 30×30×10mm 12V brushless fan, e.g. [GDSTIME 30mm 12V fan](https://www.amazon.com/GDSTIME-30mm-Small-Brushless-Cooling/dp/B00MYNX0ZI).
- **12mm switch** — 12mm momentary metal panel-mount pushbutton, e.g. [12mm stainless SPST momentary switch](https://www.amazon.com/Momentary-Button-Switch-Waterproof-Mounting/dp/B07411Z79K).
- **Slide potentiometer** — 10kΩ linear-taper slide pot for the throttle, e.g. [Bourns 10K slide potentiometer, 100mm travel](https://www.amazon.com/BOURNS-Potentiometer-Travel-Single-Linear/dp/B079ZQ6T13) (pick travel length to match the Throttle Panel STL).
- **3-axis joystick, R400B-M4** — this is a real, specific part (a 10kΩ 4-axis potentiometer joystick module, sometimes sold as JH-D400B-M4), primarily found on **AliExpress** rather than Amazon, e.g. [R400B-M4 four-dimensional joystick potentiometer](https://www.aliexpress.com/item/1005006777915138.html). Also listed in [EasyEDA's component library](https://easyeda.com/components/JOYSTICK-R400B-M4_2746fd950f1e4884b7d537fe7571a120) if you want the footprint/symbol.
- **4-color LED bar** — closest match is a 10-segment, 4-color LED bar graph (red/yellow/green/blue), e.g. [AITRIP 10-segment 4-color LED bar graph](https://www.amazon.com/AITRIP-Segment-Display-2xSuper-3xYellow/dp/B0CB3JB3P8). The drawing just says "4-Color," not "10-segment" — confirm segment count against the panel design before buying.
- **6mm push button** — standard 6×6mm tactile switch, e.g. [100-pack 6×6mm tactile buttons](https://www.amazon.com/6x6x7mm-Momentary-Tactile-Button-Through/dp/B008DS1DPM). Pick a leg height that matches your mounting depth (5mm/6.5mm/7mm/9.5mm variants).
- **19mm LED push buttons (all colors)** — 19mm illuminated momentary pushbutton, e.g. [Quentacy 19mm 12V LED momentary pushbutton](https://www.amazon.com/Quentacy-Momentary-Waterproof-Stainless-Illuminated/dp/B075Q9QSX4) or the [DAIER 19mm series](https://www.daierswitches.com/products/19mm-lighted-latching-push-button-switch-with-pre-wired) — buy the **momentary** variant, not latching, and confirm LED voltage (commonly 12V in this product family, though not stated on the drawing).
- **LED toggle switch, illuminated, covered, 12V (Red/Green)** — this is the classic "missile switch" style: toggle + hinged safety cover with LED tip, e.g. [12V illuminated red toggle switch with aircraft missile-style flip cover](https://www.amazon.com/Illuminated-Toggle-Control-Aircraft-Missile/dp/B0DHPH2L38), or [SparkFun's illuminated toggle + cover](https://www.sparkfun.com/toggle-switch-and-cover-illuminated-red.html) for a green-buyable-separately version.
- **5mm LEDs (red/blue/green/yellow/white)** — standard 5mm T-1¾ THT LEDs, any electronics supplier.
- **LED holder, RTF-5010** — real Kingbright part number, confirmed 5mm/8.1mm-hole black nylon bezel, sold at [TME](https://www.tme.com/us/en-us/details/rtf-5010/holders/kingbright-electronic/), [RS Components](https://uk.rs-online.com/web/p/led-holders/2622999), and [Rapid Electronics](https://www.rapidonline.com/kingbright-rtf5010-led-bezel-clip-prominent-5mm-55-0260).
- **SPDT toggle switch (item 12)** — most likely a standard MTS-102 style mini toggle (6mm mounting hole, ON-ON), e.g. [MTS-102 mini SPDT toggle switch](https://www.amazon.com/10pcs-MTS-102-125VAC-Toggle-Switches/dp/B01H96PTRG). Confirm mounting-hole diameter against the panel STL before buying, since "mini toggle" switches range from ~6mm to 12mm hole sizes.

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

**Sourcing:** both ICs are common, multi-sourced logic parts — [74HC165 at DigiKey](https://www.digikey.com/en/products/base-product/texas-instruments/296/74HC165/16) and [74HC595 at DigiKey](https://www.digikey.com/en/products/base-product/onsemi/488/74HC595/2341) (any manufacturer's DIP-16 74HC165/74HC595 works interchangeably). The 220kΩ 1/4W resistors are a standard through-hole value available anywhere.

The bare PCB itself can be ordered directly from the Gerbers in
`Circuit Board/Gerber_PCB1_2024-05-04.zip` (fab notes reference JLCPCB, part number
JLCPCB-002 per the schematic title block).

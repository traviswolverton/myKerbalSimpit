# myKerbalSimpit — Bill of Materials

Extracted from the "Parts List" title block in `KSP+Controller+Assembly+Drawing.pdf`.

## Purchase list (electromechanical parts)

| Qty | Part | Shopping link |
|---|---|---|
| 1 | Arduino Mega | [Arduino Mega 2560 REV3, Amazon](https://www.amazon.com/Arduino-ATmega2560-Compatible-Advanced-Projects/dp/B0046AMGW0) |
| 1 | MW RS-25-5 (Mean Well 5V power supply) | [DigiKey](https://www.digikey.com/en/products/detail/mean-well-usa-inc/RS-25-5/7706180) · [Mouser](https://www.mouser.com/ProductDetail/MEAN-WELL/RS-25-5) |
| 1 | USB Type-B panel-mount connector | [Panel-mount USB-B connector, Amazon](https://www.amazon.com/QIANRENON-Rectangular-Connector-Bulkhead-Mounting/dp/B0DG2MD5L4) (23×18.5mm cutout) |
| 1 | Power input switch | [IEC C14 inlet + rocker switch, Amazon](https://www.amazon.com/Antrader-Rocker-Switch-Socket-Connector/dp/B07F2SWY56) — inferred part, confirm cutout first |
| 2 | 30mm fan | [GDSTIME 30mm 12V fan, Amazon](https://www.amazon.com/GDSTIME-30mm-Small-Brushless-Cooling/dp/B00MYNX0ZI) |
| 8 | 12mm switch (Menu Panel) | [DMWD 12mm anti-vandal pushbutton, Amazon](https://www.amazon.com/Super-Short-Momentary-Button-Switch/dp/B0GHN8CRMF) · [Evelta (more colors)](https://evelta.com/12mm-metal-push-button-switch-anti-vandal-momentary-ring-led-red-4-pin/) |
| 1 | 12mm switch — Red (Abort Panel) | same as above, **red** |
| 1 | 12mm switch — Green (Stage Panel) | same as above, **green** |
| 1 | Slide potentiometer | [Bourns 10K slide pot, 100mm travel, Amazon](https://www.amazon.com/BOURNS-Potentiometer-Travel-Single-Linear/dp/B079ZQ6T13) — match travel to the ~72mm slot |
| 2 | 3-axis joystick, R400B-M4 v7 | [R400B-M4 joystick, AliExpress](https://www.aliexpress.com/item/1005006777915138.html) |
| 5 | 4-color LED bar | [AITRIP 10-segment 4-color LED bar, Amazon](https://www.amazon.com/AITRIP-Segment-Display-2xSuper-3xYellow/dp/B0CB3JB3P8) — close but not exact match to the 10.3×27mm slot |
| 20 | 6mm push button (7mm actual cutout) | [Sunrom 7mm momentary, black](https://www.sunrom.com/p/black-push-button-switch-7mm-momentary) / [red](https://www.sunrom.com/p/red-push-button-switch-7mm-momentary) / [green](https://www.sunrom.com/p/green-push-button-switch-7mm-momentary) — non-illuminated; see note below for an 8mm illuminated alternative |
| 2 | 19mm LED push button — Red "Large" (20mm actual, Abort/Stage) | [WerFamily 22mm anti-vandal, red](https://www.amazon.com/WerFamily-Momentary-Button-Waterproof-Stainless/dp/B078J7JWH9) or [Aexit 20mm red LED](https://www.amazon.com/Aexit-Momentary-Stainless-Pushbutton-Terminals/dp/B07KVYBBBG) |
| 1 | 19mm LED push button — Red (regular, SAS Plate) | [PPOZYLPC 19mm anti-vandal, ring LED](https://www.amazon.com/PPOZYLPC-Anti-Vandal-Button-Stainless-Momentary/dp/B0DB864CDM) |
| 3 | 19mm LED push button — Green | same as above, **green** |
| 2 | 19mm LED push button — White | same as above, **white** |
| 2 | 19mm LED push button — Blue | same as above, **blue** |
| 2 | 19mm LED push button — Yellow | same as above, **yellow** |
| 1 | LED toggle switch, illuminated, covered, 12V — Red | [Illuminated missile-cover toggle, red, Amazon](https://www.amazon.com/Illuminated-Toggle-Control-Aircraft-Missile/dp/B0DHPH2L38) |
| 1 | LED toggle switch, illuminated, covered, 12V — Green | [SparkFun illuminated toggle + cover](https://www.sparkfun.com/toggle-switch-and-cover-illuminated-red.html) — buy the green cover separately |
| 7 | 5mm red LED | generic, any electronics supplier |
| 11 | 5mm blue LED | generic, any electronics supplier |
| 3 | 5mm green LED | generic, any electronics supplier |
| 1 | 5mm yellow LED | generic, any electronics supplier |
| 1 | 5mm white LED | generic, any electronics supplier |
| 23 | LED holder, RTF-5010, 5mm press-fit | [TME](https://www.tme.com/us/en-us/details/rtf-5010/holders/kingbright-electronic/) · [RS Components](https://uk.rs-online.com/web/p/led-holders/2622999) · [Rapid Electronics](https://www.rapidonline.com/kingbright-rtf5010-led-bezel-clip-prominent-5mm-55-0260) |
| 2 | SPDT toggle switch (Joystick Panel, confirmed 12mm) | [MTS-102 mini SPDT toggle, Amazon](https://www.amazon.com/10pcs-MTS-102-125VAC-Toggle-Switches/dp/B01H96PTRG) |
| 2 | SPDT toggle switch (location unconfirmed) | same as above — verify hole size before buying |
| 118 | M3×5mm socket-head screw | McMaster-Carr part **91290A115** — search directly at [mcmaster.com](https://www.mcmaster.com/products/socket-screws/) (part-specific URLs aren't search-indexed) |
| 10 | M2×5mm socket-head screw, black oxide | McMaster-Carr part **91290A012** — search directly at [mcmaster.com](https://www.mcmaster.com/products/socket-screws/) |

### Sourcing notes

None of the switches/buttons/LEDs/joystick carry a vendor SKU in the source files (unlike the
McMaster screws, which do) — the designer modeled placeholder shapes in Fusion 360 without
recording where they bought the real parts. The links in the table above are real, current
listings found via web search that match the drawing's specs and the finished-build photos — not
a specific endorsed product, just a starting point to compare on Amazon/McMaster/AliExpress
yourself.

**Confirmed against a WIP build photo (posted on the MakerWorld project page):** the two
R400B-M4 joysticks are chunky arcade-style sticks with rubber gaiter boots (matches typical
AliExpress listings for that part), there's exactly one long-throw linear slide potentiometer
(matches BOM qty 1), both illuminated flip-cover "missile switches" are visible (one reads red,
the other teal/blue under indoor lighting — likely just white balance on the "green" LED, not a
different part), the enclosed perforated-case power supply matches the RS-25-5's typical form
factor, and the custom PCB visibly carries a row of DIP-16 ICs consistent with the 8×74HC165N +
4×74HC595N confirmed from the EasyEDA project file.

**Confirmed against clearer, well-lit finished-build photos:** the round buttons (both the
10-button bank and the smaller 4-button groups) are a distinct, recognizable "anti-vandal" style
— chrome/stainless ring bezel, flat brushed-metal actuator, ring or dot LED underneath (lights
white/blue/red/green depending on position) — not generic waterproof stainless buttons. Swapped
in real anti-vandal listings for the 12mm/19mm/20mm items in the table accordingly. The
lever toggle switches each sit next to a separate small round pilot LED rather than being
illuminated themselves, confirming the existing 5mm-LED + RTF-5010-holder line items already
cover this rather than needing an illuminated toggle switch. The top-right panel (5 vertical LED
bars + small round LEDs + one toggle) is confirmable as the Fuel Display Panel — its STL geometry
(5× 10.3×27mm slots + 7× 8.4mm round holes) matches exactly. The illuminated red/green corner
buttons that looked separate from the missile switches across several photos turned out to be the
same button already matched to the Abort/Stage Panel's 12mm hole (confirmed directly by the
builder) — a case of misjudging distance/position across different camera angles, not a
missing/extra part. No open items remain from the photo review.

A few of the links deserve a specific caveat, beyond what fits in the table:

- **RTF-5010 LED holder** is a real Kingbright part number, confirmed 8.1mm-hole black nylon bezel — matches the measured hole almost exactly.
- **R400B-M4 joystick** is a real, specific part (a 10kΩ 4-axis potentiometer module, sometimes sold as JH-D400B-M4), primarily on AliExpress rather than Amazon. Also in [EasyEDA's component library](https://easyeda.com/components/JOYSTICK-R400B-M4_2746fd950f1e4884b7d537fe7571a120) if you want the footprint/symbol.
- **6mm push button (7mm actual cutout)** — anti-vandal illuminated switches are hard to find this small (8mm is typically the smallest on the market; see [DAIER's 8mm line](https://www.chinadaier.com/category/push-button-switch/anti-vandal-switch/8mm-metal-push-button-switch/) if you want illuminated and are willing to size the hole up slightly). The Sunrom link in the table is a plain, non-illuminated exact match instead.
- **19mm Red "Large" (20mm actual)** — no exact 20mm anti-vandal match exists; the WerFamily 22mm link may need the hole enlarged slightly, or use the closer-sized but non-anti-vandal-style Aexit 20mm link instead.

### Measured mounting-hole sizes (from STL geometry)

The panel STLs don't carry part labels, but they do carry real geometry — so rather than trust
the Parts List's nominal names, I cross-sectioned every panel at mid-thickness and measured the
actual hole/slot dimensions directly (via `trimesh`, cutting each STL's solid mesh at its
thickness midpoint and measuring the resulting polygons). This turned up one real correction and
several exact confirmations:

| Part | Nominal name | **Measured hole** | Where / notes |
|---|---|---|---|
| 6mm push button (×20) | "6mm" | **7.00mm**, not 6mm | All 20 on Action Group Panel. Buy for a 7mm cutout, not 6mm — a plain 6mm tactile switch will rattle loose in this hole. |
| 12mm switch (×10) | "12mm" | **12.00mm**, confirmed | 8 on Menu Panel (vertical bank) + 1 each on Abort/Stage Panel = 10, exact match to BOM qty. |
| 19mm LED push button — Green/White/Blue/Yellow (+ some Red) | "19mm" | **19.00mm**, confirmed | All 10 on SAS Plate in a clean 2×5 grid (the SAS mode-select bank). |
| 19mm LED push button — Red "Large" | "19mm" | **20.00mm**, larger | 1 each on Abort Panel and Stage Panel — genuinely a bigger button/hole than the other colors, not just a naming quirk. Don't buy 12 identical 19mm buttons; the 2 Abort/Stage ones need a ~20mm part. |
| LED holder RTF-5010 (×23) | 8.1mm spec | **~8.0–8.5mm**, confirmed | Matches Kingbright's stated 8.1mm hole closely. Found across Fuel Display (7), SAS Plate (2), Throttle Panel (10), Joystick Panel (4) = 23, exact match to BOM qty. |
| 4-color LED bar (×5) | — | **10.3mm × 27mm rectangular slot**, not round | All 5 on Fuel Display Panel, exact match to BOM qty — useful for picking a bar-graph component that actually fits a rectangular cutout rather than a round one. |
| Slide potentiometer (×1) | — | **~4mm × 72mm slot** | Centered on the Throttle Panel. A pot with ~60–70mm of actual travel (not total body length) will fit this slot well. |
| SPDT toggle switch (item 12, ×4) | — | 2 confirmed at 12.00mm | On the Joystick Panel. The other 2 weren't clearly identifiable in the geometry — don't assume they're the same size without checking. |

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

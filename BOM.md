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
white/blue/red/green depending on position) — not the generic waterproof stainless buttons
linked below. Swapped in real anti-vandal listings for the 12mm/19mm/20mm items accordingly. The
lever toggle switches each sit next to a separate small round pilot LED rather than being
illuminated themselves, confirming the existing 5mm-LED + RTF-5010-holder line items already
cover this rather than needing an illuminated toggle switch. The top-right panel (5 vertical LED
bars + small round LEDs + one toggle) is confirmable as the Fuel Display Panel — its STL geometry
(5× 10.3×27mm slots + 7× 8.4mm round holes) matches exactly.

**Two extra buttons not on the Parts List at all:** beyond the missile-switch-adjacent button
already matched to Abort/Stage Panel's 12mm hole, there's a second, separate illuminated button
at the far bottom-left and bottom-right corners of the console — confirmed via close-up photos to
be genuine buttons with lit LED rings (not screw-head reflections), color-matched to their side's
missile switch (**red** bottom-left, **green** bottom-right). These sit well below the missile
switches, separated by the full panel height, and don't match any hole in the flat panel scans
(Left/Right Side Panel, Bottom/Front/Rear Panel). Since every quantity in the Parts List's 46
items already reconciles exactly without them, these two are most likely something the builder
added beyond the stock design — not a mis-scan on my end. Best geometric lead: a multi-plane scan
of `Combo Brace v8.stl` and `Combo Brace 2 v7.stl` (the two 3D corner brackets carrying the
fan+switch+knob assembly) found a consistent ~10mm round hole in each, a standard anti-vandal
button size — plausible but not confirmed, since 3D bracket geometry doesn't slice as cleanly as
a flat panel.

- **Corner button, ×2 (confirmed real, panel unconfirmed)** — genuine illuminated pushbutton, red on the left, green on the right. Best current match: a ~10mm anti-vandal metal pushbutton with ring LED, e.g. [NDZZQBPGO 10mm anti-vandal momentary pushbutton, ring LED](https://www.amazon.com/Momentary-Latching-Illuminated-Anti-Vandal-Waterproof/dp/B0CY2D4HVM) in red and green. Since this isn't in the original Parts List, measure the actual hole on your build directly before ordering rather than trusting this size guess.

- **Arduino Mega** — genuine [Arduino Mega 2560 REV3](https://www.amazon.com/Arduino-ATmega2560-Compatible-Advanced-Projects/dp/B0046AMGW0) or any ATmega2560-compatible clone (ELEGOO, SainSmart, KEYESTUDIO all show up on Amazon).
- **MW RS-25-5** — this is a real Mean Well part number, sold at [DigiKey](https://www.digikey.com/en/products/detail/mean-well-usa-inc/RS-25-5/7706180), [Mouser](https://www.mouser.com/ProductDetail/MEAN-WELL/RS-25-5), and [Newark](https://www.newark.com/mean-well/rs-25-5/power-supply-ac-dc-5v-5a/dp/99AC4268). 5V/5A/25W AC-DC supply.
- **USB Type-B panel-mount connector** — generic part, e.g. [rectangular panel-mount USB-B connector](https://www.amazon.com/QIANRENON-Rectangular-Connector-Bulkhead-Mounting/dp/B0DG2MD5L4) (23×18.5mm cutout).
- **Power input switch** — since the RS-25-5 takes mains AC input, this is likely an IEC C14 inlet with integrated rocker switch (and often a fuse holder), e.g. [IEC 320 C14 inlet + rocker switch panel socket](https://www.amazon.com/Antrader-Rocker-Switch-Socket-Connector/dp/B07F2SWY56). Worth confirming panel cutout size against the STL before buying.
- **30mm fan** — standard 30×30×10mm 12V brushless fan, e.g. [GDSTIME 30mm 12V fan](https://www.amazon.com/GDSTIME-30mm-Small-Brushless-Cooling/dp/B00MYNX0ZI).
- **12mm switch** — the finished-build photos confirm this is an anti-vandal metal pushbutton with ring LED, e.g. [DMWD 12mm anti-vandal momentary pushbutton, blue ring LED](https://www.amazon.com/Super-Short-Momentary-Button-Switch/dp/B0GHN8CRMF), or the wider color range at [Evelta's 12mm anti-vandal series](https://evelta.com/12mm-metal-push-button-switch-anti-vandal-momentary-ring-led-red-4-pin/) (red/green/blue/yellow). Matches the Menu Panel's 12mm holes confirmed below.
- **Slide potentiometer** — 10kΩ linear-taper slide pot for the throttle, e.g. [Bourns 10K slide potentiometer, 100mm travel](https://www.amazon.com/BOURNS-Potentiometer-Travel-Single-Linear/dp/B079ZQ6T13) (pick travel length to match the Throttle Panel STL).
- **3-axis joystick, R400B-M4** — this is a real, specific part (a 10kΩ 4-axis potentiometer joystick module, sometimes sold as JH-D400B-M4), primarily found on **AliExpress** rather than Amazon, e.g. [R400B-M4 four-dimensional joystick potentiometer](https://www.aliexpress.com/item/1005006777915138.html). Also listed in [EasyEDA's component library](https://easyeda.com/components/JOYSTICK-R400B-M4_2746fd950f1e4884b7d537fe7571a120) if you want the footprint/symbol.
- **4-color LED bar** — closest match is a 10-segment, 4-color LED bar graph (red/yellow/green/blue), e.g. [AITRIP 10-segment 4-color LED bar graph](https://www.amazon.com/AITRIP-Segment-Display-2xSuper-3xYellow/dp/B0CB3JB3P8), which is close in footprint to the measured 10.3mm × 27mm rectangular cutout (below) but not an exact match — confirm segment count and body size against the panel before buying.
- **6mm push button** — geometry confirms a **7mm round cutout**, not a bare 6×6mm PCB tactile switch. The finished-build photos show these lit up (white/red), so they're illuminated too, not plain — but anti-vandal switches are hard to find this small (8mm is typically the smallest illuminated size on the market; see e.g. [DAIER's 8mm metal pushbutton line](https://www.chinadaier.com/category/push-button-switch/anti-vandal-switch/8mm-metal-push-button-switch/)). If you want an exact 7mm match, Sunrom sells a plain (non-illuminated) version: [7mm momentary push button, black](https://www.sunrom.com/p/black-push-button-switch-7mm-momentary) (also [red](https://www.sunrom.com/p/red-push-button-switch-7mm-momentary)/[green](https://www.sunrom.com/p/green-push-button-switch-7mm-momentary)); otherwise size the hole up slightly for an illuminated 8mm anti-vandal button instead.
- **19mm LED push buttons (Green/White/Blue/Yellow + regular Red, ×9–10)** — finished-build photos confirm the anti-vandal ring-LED style: [PPOZYLPC 19mm anti-vandal metal pushbutton, ring LED](https://www.amazon.com/PPOZYLPC-Anti-Vandal-Button-Stainless-Momentary/dp/B0DB864CDM) — buy the **momentary** variant, not latching, and confirm LED voltage (commonly 12V in this product family, though not stated on the drawing). Geometry check (below) confirms these genuinely need a 19mm hole.
- **19mm LED push button — Red "Large" (Abort/Stage, ×2)** — geometry shows these need a ~20mm hole, not 19mm. Closest real anti-vandal match is 22mm rather than 20mm exactly: [WerFamily 22mm anti-vandal pushbutton, red ring LED](https://www.amazon.com/WerFamily-Momentary-Button-Waterproof-Stainless/dp/B078J7JWH9) — confirm it'll fit a 20mm hole (may need slight enlarging) before ordering, or use the closer-sized but non-anti-vandal [Aexit 20mm red LED momentary pushbutton](https://www.amazon.com/Aexit-Momentary-Stainless-Pushbutton-Terminals/dp/B07KVYBBBG) instead. Buy these separately from the other 19mm colors rather than assuming one size fits all.
- **LED toggle switch, illuminated, covered, 12V (Red/Green)** — this is the classic "missile switch" style: toggle + hinged safety cover with LED tip, e.g. [12V illuminated red toggle switch with aircraft missile-style flip cover](https://www.amazon.com/Illuminated-Toggle-Control-Aircraft-Missile/dp/B0DHPH2L38), or [SparkFun's illuminated toggle + cover](https://www.sparkfun.com/toggle-switch-and-cover-illuminated-red.html) for a green-buyable-separately version.
- **5mm LEDs (red/blue/green/yellow/white)** — standard 5mm T-1¾ THT LEDs, any electronics supplier.
- **LED holder, RTF-5010** — real Kingbright part number, confirmed 5mm/8.1mm-hole black nylon bezel, sold at [TME](https://www.tme.com/us/en-us/details/rtf-5010/holders/kingbright-electronic/), [RS Components](https://uk.rs-online.com/web/p/led-holders/2622999), and [Rapid Electronics](https://www.rapidonline.com/kingbright-rtf5010-led-bezel-clip-prominent-5mm-55-0260).
- **SPDT toggle switch (item 12)** — most likely a standard MTS-102 style mini toggle, e.g. [MTS-102 mini SPDT toggle switch](https://www.amazon.com/10pcs-MTS-102-125VAC-Toggle-Switches/dp/B01H96PTRG). Geometry check below found 2 of the 4 at a 12mm hole (on the Joystick Panel) — the other 2 weren't clearly identifiable, so measure before buying rather than assuming 6mm.

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

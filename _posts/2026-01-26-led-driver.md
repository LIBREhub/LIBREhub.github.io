---
title: Low-cost LED Driver
description: A budget-friendly, four-channel LED driver for high-power optogenetics and microscopy, featuring analog intensity control and digital switching.
categories: resource
header-img: /images/resources/led-driver/image30.png
---

*Developed by Florencia Novillo, Andres Mendoza, and Vicente Parot. Part of LIBRE\_hub.*

## **Low-cost LED Driver**

This circuit is a budget-friendly alternative to commercial LED/laser diode drivers (e.g., Thorlabs DC4100-HUB). It allows control of high-power LEDs used in optogenetics and microscopy. It is a four-channel LED Driver built as a wrapper to a single analog-adjustable, commercial LED driver that operates as a constant current source. 

The driver box has one analog input for intensity control of the driver, and four digital inputs to switch 4 LEDs independently. There are also manual controls to bypass any of the 5 inputs, a potentiometer to manually adjust the intensity, and an optional analog ammeter to monitor output current.

#### **Components and Tools**

**Equipment**

| Qty | Component | Specifications | Supplier |
| :--- | :--- | :--- | :--- |
| 1 | 3D printer | e.g. Ender 3 | Creality |

**Tools**

| Qty | Component | Specifications | Supplier |
| :--- | :--- | :--- | :--- |
| 1 | Soldering iron | 60W Adjustable temperature | [AliExpress](https://www.aliexpress.com/item/1005007970187200.html) |
| 1 | Soldering wire | 0.8 mm, flux core | [AliExpress](https://www.aliexpress.com/item/1005008695639704.html) |
| 1 | Hot air gun | | [AliExpress](https://www.aliexpress.com/item/1005007010056491.html) |
| 1 | Allen key | M2 | [GrabCAD](https://grabcad.com/library/allen-key-set-4/details?folder_id=3295376) |
| 1 | Allen key | M3 | [GrabCAD](https://grabcad.com/library/allen-key-set-4/details?folder_id=3295376) |
| 1 | Allen key | M6 | [GrabCAD](https://grabcad.com/library/6mm-allen-wrench-1) |
| 1 | Screwdriver | 0.6 mm flat blade | [AliExpress](https://www.aliexpress.com/item/1005008304338583.html) |
| 1 | Wire cutter | Diagonal pliers, any size | [AliExpress](https://www.aliexpress.com/item/4000988113226.html) |
| 1 | Multimeter | | Any |
| 1 | Oscilloscope | | Any |

**Electronics**

| Qty | Component | Specifications | Supplier |
| :--- | :--- | :--- | :--- |
| 1 | Power Supply Module | 5V/3.3V for Breadboard | [AliExpress](https://www.aliexpress.com/item/1005001621899532.html) |
| 1 | Charging Module | TP4056 USB-C | [AliExpress](https://www.aliexpress.com/item/32818058518.html) |
| 1 | MOSFET | IRLZ44N | [AliExpress](https://www.aliexpress.com/item/1005008120572312.html) |
| 4 | Transistor | 2N2222 | [AliExpress](https://www.aliexpress.com/item/1005007720496827.html) |
| 5 | Resistor | 10k Ohm | [AliExpress](https://www.aliexpress.com/item/1005005698974060.html) |
| 5 | Resistor | 220 Ohm | [AliExpress](https://www.aliexpress.com/item/1005005698974060.html) |
| 5 | LED | 5mm Blue | [AliExpress](https://www.aliexpress.com/item/1005008495577170.html) |
| 1 | Ammeter | Analog 85C1 (0-1A) | [AliExpress](https://www.aliexpress.com/item/4000067677334.html) |
| 1 | Potentiometer | 10k Ohm | [AliExpress](https://www.aliexpress.com/item/32810872544.html) |
| 1 | LED Driver | BuckBlock A009-D-V-1000 | [LEDSupply](https://www.ledsupply.com/led-drivers/buckblock-dc-led-driver) |
| 1 | Jumper Cables | For 12V LED Strip | [LEDSupply](https://www.ledsupply.com/accessories/jumper-cables-12v-led-strip-light) |

**Hardware & Fasteners**

| Qty | Component | Specifications | Supplier |
| :--- | :--- | :--- | :--- |
| 20 | Heat Inserts | M3 x 5mm x 4mm | [AliExpress](https://www.aliexpress.com/item/32810872544.html) |
| 2 | Screws | M2 x 6mm | [AliExpress](https://es.aliexpress.com/item/32810872544.html?spm=a2g0o.productlist.main.1.1599DD4xDD4xNq&algo_pvid=982fe1b2-535d-4144-b9f2-4d24c5794567&pdp_ext_f=%7B%22order%22%3A%2213060%22%2C%22spu_best_type%22%3A%22service%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A32810872544%7C_p_origin_prod%3A) |
| 4 | Screws | M3 x 10mm | [AliExpress](https://es.aliexpress.com/item/32810872544.html?spm=a2g0o.productlist.main.1.1599DD4xDD4xNq&algo_pvid=982fe1b2-535d-4144-b9f2-4d24c5794567&pdp_ext_f=%7B%22order%22%3A%2213060%22%2C%22spu_best_type%22%3A%22service%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A32810872544%7C_p_origin_prod%3A) |
| 1 | Filament | PLA+ | Esun |

---

#### **1. 3D Printing**

The enclosure for the LED Driver is designed to be printed in PLA. Ensure your printer bed is leveled and clean to prevent warping.

**Figure 1:** Once the printing process is complete, inspect the parts. Clean any stringing or imperfections from the edges and holes to ensure a proper fit for the electronics and fasteners.
<img class="pfloat-center" src="/images/resources/led-driver/image1.jpeg" width="35%" style="display: block; margin: 0 auto;" loading="lazy" data-action=zoom>

---

#### **2. Electronics (Pre-soldered PCB)**

If you are using the custom PCB designed for this project (manufactured via JLC PCB), follow these detailed assembly steps to prepare the modules and components.

**Power Supply Module**
The power supply module requires modification to fit within the enclosure's height constraints.
**Figure 2:** Locate the pins on the bottom of the module and cut them flush. This is critical to prevent short circuits and ensure the module sits flat.
<img class="pfloat-center" src="/images/resources/led-driver/image2.png" width="50%" style="display: block; margin: 0 auto;" loading="lazy" data-action=zoom>

**Figure 3:** Solder the header pins to the *top* side of the module as shown. This inversion allows the module to mount correctly onto the main PCB.
<img class="pfloat-left" src="/images/resources/led-driver/image3.png" width="40%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/led-driver/image4.jpeg" width="40%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>

**Charging Module (TP4056)**
**Figure 4:** Prepare the TP4056 charging module for mounting. Insert an M3 screw through the mounting hole and use a spacer (either 3D printed or nylon) to maintain the correct height.
<img class="pfloat-left" src="/images/resources/led-driver/image5.png" width="45%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/led-driver/image6.png" width="45%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>

**Figure 5:** Solder the module directly to the main PCB. Ensure the USB-C port is aligned with the edge of the board for accessibility.
<img class="pfloat-left" src="/images/resources/led-driver/image7.png" width="45%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/led-driver/image8.png" width="45%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>

**Ammeter Preparation**
**Figure 6:** Inspect the analog ammeter (85C1). Identify the positive and negative terminals on the rear housing.
<img class="pfloat-left" src="/images/resources/led-driver/image9.jpeg" width="45%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/led-driver/image10.png" width="45%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>

**Figure 7:** Cut two lengths of wire. Strip approximately 1 cm of insulation from the ends. Twist the copper strands tightly and tin them with solder to prevent fraying.
<img class="pfloat-left" src="/images/resources/led-driver/image11.png" width="45%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/led-driver/image12.png" width="45%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>

**Figure 8:** Crimp ring terminals onto one end of each wire. Attach these firmly to the ammeter posts using the included nuts.
<img class="pfloat-left" src="/images/resources/led-driver/image13.png" width="45%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/led-driver/image14.png" width="45%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>

**Potentiometer**
**Figure 9:** Solder three wires to the potentiometer terminals. Use heat shrink tubing over the solder joints to prevent shorts. Twist the wires together to keep the assembly tidy.
<img class="pfloat-center" src="/images/resources/led-driver/image15.png" width="60%" style="display: block; margin: 0 auto;" loading="lazy" data-action=zoom>

**LED Driver (BuckBlock)**
**Figure 10:** The BuckBlock A009-D-V-1000 is the core current source. Familiarize yourself with the wire color coding before soldering.
<img class="pfloat-center" src="/images/resources/led-driver/image16.jpeg" width="60%" style="display: block; margin: 0 auto;" loading="lazy" data-action=zoom>

**Figure 11:** Wiring the BuckBlock to the PCB terminal block.
1.  **Red & Black:** Connect to the power input terminals (Vin+ / Vin-).
2.  **Yellow:** Connect to the dimming control/potentiometer input.
3.  **White/Purple:** Connect to the LED output terminals.
<img class="pfloat-left" src="/images/resources/led-driver/image17.png" width="30%" loading="lazy" data-action=zoom>
<img class="pfloat-left" src="/images/resources/led-driver/image18.png" width="30%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/led-driver/image19.png" width="30%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>

---

#### **3. Assembly**

**Case Preparation**
**Figure 12:** Using a soldering iron set to a low temperature (~200°C), press the M3 heat-set inserts into the plastic bosses of the 3D printed case. Ensure they sit flush with the surface.
<img class="pfloat-center" src="/images/resources/led-driver/image20.png" width="60%" style="display: block; margin: 0 auto;" loading="lazy" data-action=zoom>

**Mounting Components**
**Figure 13:** Insert the ammeter into the front panel cutout. Secure it using the mounting brackets or nuts provided with the meter.
<img class="pfloat-left" src="/images/resources/led-driver/image21.png" width="45%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/led-driver/image22.png" width="45%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>

**Wiring the Case**
**Figure 14:** Connect the free ends of the ammeter wires to the corresponding terminals on the main PCB. Verify the polarity to ensuring the needle deflects correctly.
<img class="pfloat-left" src="/images/resources/led-driver/image23.png" width="45%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/led-driver/image24.png" width="45%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>

**Figure 15:** Connect the potentiometer wires to the control headers on the PCB.
<img class="pfloat-left" src="/images/resources/led-driver/image25.png" width="45%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/led-driver/image26.png" width="45%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>

**Figure 16:** Mount the potentiometer to the front panel hole. If the potentiometer has an anti-rotation tab, ensure it is seated in the corresponding slot or remove it if not needed.
<img class="pfloat-left" src="/images/resources/led-driver/image27.png" width="45%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/led-driver/image28.png" width="45%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>

**Final Configuration**
**Figure 17:** Before closing the box, configure the power supply module jumper to output **12V** (indicated by the blue LED). This voltage is required for the driver operation.
<img class="pfloat-center" src="/images/resources/led-driver/image29.png" width="60%" style="display: block; margin: 0 auto;" loading="lazy" data-action=zoom>

**Figure 18:** Place the PCB into the case and secure the lid with M3 screws. The Low-cost LED Driver is now ready for operation.
<img class="pfloat-center" src="/images/resources/led-driver/image30.png" width="80%" style="display: block; margin: 0 auto;" loading="lazy" data-action=zoom>

---

#### **4. LED Driver Characterization**

The device performance was characterized to ensure suitability for high-speed optogenetics. The optical modulation is limited by the driver’s internal current regulation dynamics and the operating point (input voltage, LED Vf, wiring inductance, etc.).

**Rise and Fall Times**
The system exhibits a large transient/overshoot followed by a settling period during the ON portion of the pulse. This behavior makes automatic "rise/fall time" readings dependent on the specific waveform shape.

| Frequency | Rise time | Fall time |
| :--- | :--- | :--- |
| ~0.90–1.00 kHz | ~22–34 µs | ~5–8 µs |
| ~3.0 kHz | ~27.6 µs | ~5.7 µs |
| ~4.0 kHz | ~31.5 µs | ~5.7 µs |
| ~6.0–7.0 kHz | ~30–31.5 µs | ~5.2–6.1 µs |
| ~100–300 Hz | ~26–28 µs | ~1–4 ms |

**Pulse Dynamics & Frequency Response**
Below are representative oscilloscope captures showing pulse behavior.
*Left: A 75µs pulse generating ~50µs FWHM optical output. Right: Fast transients visible at 3 kHz driving frequency.*
<img class="pfloat-left" src="/images/resources/led-driver/image33.png" width="45%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/led-driver/image35.png" width="45%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>

**Steady State Behavior**
At lower frequencies (e.g., 300 Hz), the steady-state current becomes clearly visible after the initial transient.
<img class="pfloat-center" src="/images/resources/led-driver/image38.png" width="60%" style="display: block; margin: 0 auto;" loading="lazy" data-action=zoom>

---

#### **References**

* [Gerber PCB](/images/resources/led-driver/2026-01-27%20Gerber-LED-dirver%20PCB.zip)
* [EasyEDA csv BOM](/images/resources/led-driver/2026-01-27%20BOM_easyeda_LED_driver.csv)


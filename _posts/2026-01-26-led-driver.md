---
title: Low-cost Four-Channel LED Driver
description: A budget-friendly wrapper for high-power LED control in optogenetics and microscopy.
categories: resource
header-img: /images/resources/led-driver/image18.png
---

*Developed by Florencia Novillo, Andres Mendoza, and Vicente Parot. Part of LIBRE\_hub.*

## **Budget-Friendly LED Control for Bioimaging**

This circuit is a budget-friendly alternative to commercial LED/laser diode drivers (e.g., Thorlabs DC4100-HUB). It allows control of high-power LEDs used in optogenetics and microscopy. It is a four-channel LED Driver built as a wrapper to a single analog-adjustable, commercial LED driver that operates as a constant current source.

The driver box features:

* One **analogue input** for intensity control.  
* Four **digital inputs** to switch 4 LEDs independently.  
* **Manual controls** to bypass any of the 5 inputs.  
* A **potentiometer** for manual intensity adjustment.  
* An optional **analog ammeter** to monitor output current.

#### **Components and Tools**

**Equipment and Tools**

| Qty | Component | Specifications | Supplier | Price (USD) |
| :--- | :--- | :--- | :--- | :--- |
| 1 | 3D printer | e.g. Ender 3 | Creality | 199.0 |
| 1 | Soldering iron | 60W Adjustable temperature | [AliExpress](https://www.google.com/search?q=https://www.aliexpress.com/item/1005005934571060.html) | 3.89 |
| 1 | Soldering wire | 0.8 mm, flux core | [AliExpress](https://www.google.com/search?q=https://www.aliexpress.com/item/1005006000213454.html) | 1.64 |
| 1 | Hot air gun | | [AliExpress](https://www.google.com/search?q=https://www.aliexpress.com/item/1005005953046774.html) | 7.38 |
| 1 | Allen key | M3 | [AliExpress](https://www.google.com/search?q=https://www.aliexpress.com/item/1005005953046774.html) | 0.69 |
| 1 | Wire cutter | Diagonal pliers | [AliExpress](https://www.google.com/search?q=https://www.aliexpress.com/item/1005005470366668.html) | 0.99 |
| 1 | Wire stripper | Stripper and crimper | [AliExpress](https://www.google.com/search?q=https://www.aliexpress.com/item/1005005470366668.html) | 3.91 |

**Electronics (BOM \- Pre-soldered PCB Option)**

| Qty | Component | Specifications | Supplier | Price (USD) |
| :--- | :--- | :--- | :--- | :--- |
| 1 | PCB | [Soldered, Gerber/BOM/SC available](https://jlcpcb.com/) | JLC PCB | 22.00 |
| 1 | Buckblock | [A009-D-V-1000; 1A](https://www.google.com/search?q=https://www.ledsupply.com/led-drivers/buckblock-constant-current-led-driver) | LEDSupply | 21.77 |
| 1 | Power Module | [100W USB-C PD Trigger](https://www.google.com/search?q=https://www.aliexpress.com/item/1005005961474944.html) | AliExpress | 1.24 |
| 4 | MOSFET | [IRLZ44N](https://www.google.com/search?q=https://www.aliexpress.com/item/32828691515.html) | AliExpress | 0.99 |
| 8 | BJT | [2N2222](https://www.google.com/search?q=https://www.aliexpress.com/item/32850989392.html) | AliExpress | 0.99 |
| 5 | Female BNC | [Elbow, through-hole](https://www.google.com/search?q=https://www.aliexpress.com/item/1005004128505581.html) | AliExpress | 4.65 |
| 1 | Potentiometer | [Rotary 22 kΩ](https://www.google.com/search?q=https://www.aliexpress.com/item/32847055745.html) | AliExpress | 1.09 |
| 1 | Ammeter | [0-1 A Analog](https://www.google.com/search?q=https://www.aliexpress.com/item/32851167817.html) | AliExpress | 3.02 |
| 4 | Barrel jack | [2.1 mm DC](https://www.google.com/search?q=https://www.aliexpress.com/item/32958448661.html) | AliExpress | 1.03 |

**3D Printed Case Parts**

| Component | Specifications | Supplier | Price (USD) |
| :--- | :--- | :--- | :--- |
| Case | Top and bottom. Stl file | \[Download Placeholder\] | 0 |
| PLA filament | 1.75 mm | [Esun](https://www.esun3d.com/) | 50.99 |
| Heat inserts | M3(OD4.2mm), 6mm | [AliExpress](https://www.google.com/search?q=https://www.aliexpress.com/item/1005005961474944.html) | 0.99 |

#### **1\. 3D Printing and Preparation**

**Step 1: Printer Settings**

| Setting | Option |
| :--- | :--- |
| Material | PLA |
| Temperature | Standard for PLA |
| Layer Height | 0.2mm (0.1mm for parts with threads) |

**Step 2: Clean-up and Safety**

Carefully remove the print border from all pieces. To avoid injury, remove most of the edge without a knife first. Clean the remaining edge with a utility knife using a "peeling" action, supporting the part with the thumb of your dominant hand while moving the blade away from your body.

<img class="pfloat-center" src="/images/resources/led-driver/image1.jpeg" width="60%" style="display: block; margin: 0 auto;" loading="lazy" data-action=zoom>

#### **2\. Electronics Assembly**

**USB-C Power Supply Module:**

1. Attach nylon spacers to the charging module (Figure 4).  
2. Solder 1x2 header pins to the PCB, removing the middle pin if using a 3-pin strip.  
3. Align the module's (+) and (-) terminals with the Vin+ and GND pins on the PCB.  
4. Secure with M2 screws and washers so the module sits parallel to the main board.

<img class="pfloat-left" src="/images/resources/led-driver/image4.jpeg" width="33%" loading="lazy" data-action=zoom>
<img class="pfloat-left" src="/images/resources/led-driver/image5.png" width="33%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/led-driver/image17.png" width="33%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>


**LED Buckblock Installation:**

Strip, twist, and tin the six wires of the Buckblock. Connect them to the terminal blocks (BB\_LED, BB\_PS, BB\_DIM) in the exact order they exit the component: LED-, LED+, Vin+, Vout-, DIM, and DIM GND.

<img class="pfloat-center" src="/images/resources/led-driver/image11.png" width="80%" style="display: block; margin: 0 auto;" loading="lazy" data-action=zoom>

**Ammeter and Potentiometer:**

* **Ammeter:** Connect the negative (-) wire to Pin 1 and the positive (+) wire to Pin 2 of the AMP terminal block.  
* **Potentiometer:** Solder wires to pins 2 and 3\. Connect them to pins 2 and 3 of the POT terminal block on the PCB.

<img class="pfloat-left" src="/images/resources/led-driver/image14.png" width="45%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/led-driver/image15.png" width="45%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>

#### **3\. Enclosure and Final Setup**

**Hardware Prep:**

Install eight M3 heat-set inserts into the holes on the top and bottom case. This ensures the case can be opened repeatedly for maintenance.

<img class="pfloat-center" src="/images/resources/led-driver/image12.png" width="45%" loading="lazy" data-action=zoom>

**Closing the Case:**

1. **Voltage Selection:** Connect a USB-C charger. Press the module button until the **12V LED** is lit (Figure 17).  
2. **Mounting:** Fit the PCB into the bottom case. Place the ammeter and potentiometer into their case cutouts.  
3. **Sealing:** Fit the top case, align the switches, and secure with the four corner M3 screws.

<img class="pfloat-center" src="/images/resources/led-driver/image18.png" width="70%" style="display: block; margin: 0 auto;" loading="lazy" data-action=zoom>

#### **4\. Performance Characterization**

Extensive testing using a high-speed power meter (Thorlabs PM400+S121C, \<1 µs response) confirms the driver's suitability for optogenetic pulsing and imaging.

**Key Performance Findings:**

* **Power:** Standard 5V phone chargers provide only \~20% intensity. A USB-C PD source (30W+) is required for full output with 3W/5W LEDs.  
* **Dynamic Transients:** We observe a fast-rising transient (\~40 µs) followed by a decay/settling period of 1-2 ms. Pulses must be at least **50 µs** long to be relayed to the output.  
* **Modulation Speed:** The system replicates signals up to **30 kHz**, though the waveform shape degrades significantly at these extremes. The recommended stable operating limit is in the **low kHz range**.

| Frequency | Rise Time | Fall Time |
| :---- | :---- | :---- |
| \~1.0 kHz | \~22–34 µs | \~5–8 µs |
| \~4.0 kHz | \~31.5 µs | \~5.7 µs |
| \~100 Hz | \~26–28 µs | \~1–4 ms (steady state) |

<img class="pfloat-left" src="/images/resources/led-driver/image33.png" width="45%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/led-driver/image34.png" width="45%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>
At lower frequencies, the transient overshoot is more pronounced before settling to the steady-state current.
<img class="pfloat-left" src="/images/resources/led-driver/image38.png" width="45%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/led-driver/image43.png" width="45%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>


#### **Design Files and Resources**

* [Onshape Project \- Assembly](https://cad.onshape.com/documents/096c25a9298dd8889e4dec74/w/c5e233639d356c6856bc744c/e/240705b285462483907fc860)  
* [Online Circuit Simulation](https://www.google.com/search?q=https://tinyurl.com/led-driver-sim-placeholder)  
* [STL Files Zip (Enclosure)](https://www.google.com/search?q=https://github.com/vparot/led-driver-case)  
* [Gerber & BOM (PCB)](https://www.google.com/search?q=https://github.com/vparot/led-driver-pcb)

*This guide provides a hardware overview. Users should calibrate resulting optical dose against mean optical power for dynamic pulse experiments.*
---
title: High Coherence Low-Cost Diode Laser
description: A DIY control system and interferometer to stabilize a laser diode for high-precision microscopy and optogenetics.
categories: resource
header-img: /images/resources/high-coherence-laser/image9.png
---

*Developed by Nancy Gomez, Matias Solis, and Vicente Parot. Part of LIBRE\_hub.*

## **High Coherence Low-Cost Diode Laser**

This project is our own attempt at testing, refining, and adapting an online report of a DIY laser interferometer for use in interferometric microscopy. The goal is to use low-cost means to control a laser diode to generate a stable single-mode output.

The reference project is similar; however, its design aims to be used in a length measurement arm, whereas we would like to use a free-space output beam to illuminate the excitation path of a fluorescence microscopy system. The videos describing the source project are available here:
* [Laser Interferometer - Part 1: The Optical Design](https://www.youtube.com/watch?v=v8gaEqHa1r0)
* [Laser Interferometer - Part 2: Building the beam splitter](https://www.youtube.com/watch?v=AZ9-UrlGOcE)
* [Laser Interferometer - Part 3: Mechanical Design](https://www.youtube.com/watch?v=0vnV1S7gBCE)

#### **Project Summary**

The project consists of the design and construction of an electronic and optical control system destined to stabilize the wavelength emitted by a laser diode, with the aim of obtaining a light source of high temporal coherence at a low cost. This initiative seeks to develop an accessible alternative to high-precision commercial lasers, whose price is often prohibitive in the Latin American market.

From an electronic point of view, a circuit was implemented capable of manipulating both the temperature and the current of the laser diode through two control modes or phases:
1.  **Pre-heating:** The controller heats the laser mount until it reaches the desired operating temperature.
2.  **Current Stabilization:** Once this condition is stabilized, the system passes to the second mode, where regulation focuses exclusively on minimizing the accumulated error associated with the laser current, improving its temporal stability.

The electronic system is composed of three PCB cards (driver, actuator, and sensor) plus a microcontroller. To complete the control loop in the second mode, a DIY interferometer (based on two retroreflectors, a mirror, a beam splitter, and a detector) is used to monitor the variation in the emitted wavelength. Approximately 10% of the laser light is diverted to evaluate its coherence, while the remaining 90% is available for applications such as the microscope to be developed subsequently.

High-coherence lasers play a fundamental role in various biomedical engineering applications that require extreme precision, such as interferometry, holography, spectroscopy, and advanced microscopy.

---

### **Materials and Components**

The electronic system responsible for laser control is composed of four subsystems: drivers, actuator, sensor, and microcontroller.

**Drivers**
| Component | Quantity |
| :--- | :--- |
| Capacitor 10uF | 3 |
| Capacitor 1uF | 1 |
| Capacitor 100nF | 2 |
| Capacitor 10nF | 1 |
| Ferrite Bead FB20009-3B-RC | 2 |
| MOSFET IRLZ44N | 1 |
| Transistor BC337 | 1 |
| Resistor 330Ω | 2 |
| Resistor 10kΩ | 3 |
| Resistor 10Ω | 1 |
| Resistor 30kΩ | 1 |
| Resistor 100kΩ | 1 |
| Resistor 15kΩ | 1 |
| Potentiometer Trimmer 10kΩ | 1 |
| Power Activation Module 100W 5A USB-C PD | 1 |
| Voltage Regulator MCP1700-3002E/T0 | 1 |
| Op-Amp OPA344 | 1 |
| USB-C Adapter and Cable | 1 |
| Connector XH2.54 2-pin | 4 |
| Connector XH2.54 3-pin | 1 |
| Pinheader 1-pin (For testing resistor) | 1 |

**Actuator**
| Component | Quantity |
| :--- | :--- |
| Capacitor 100nF | 2 |
| Resistor 4.7kΩ | 2 |
| Resistor 30Ω | 2 |
| Temperature Sensor DS18B20 | 2 |
| Connector XH2.54 2-pin | 2 |
| Connector XH2.54 3-pin | 1 |
| Laser Diode HL63022DG (or similar common anode) | 1 |

**Sensor**
| Component | Quantity |
| :--- | :--- |
| Capacitor 10pF | 2 |
| Resistor 39kΩ | 2 |
| Resistor 100Ω | 1 |
| Resistor 5.1kΩ | 1 |
| Op-Amp TL072 | 1 |
| Photodiode SFH229 | 2 |
| Connector XH2.54 2-pin | 4 |

**Microcontroller**
| Component | Quantity |
| :--- | :--- |
| Development Board with MCU STM32F103C8T6 (BluePill) | 1 |
| ST-Link V2 | 1 |
| Connector XH2.54 2-pin | 2 |
| Connector XH2.54 3-pin | 2 |

**Optical Components (Interferometer)**
| Item | Pieces | Price (CLP) | Link |
| :--- | :--- | :--- | :--- |
| Tempered glass (Base) 45x150x4mm | 1 | $12,100 | [AliExpress](https://a.aliexpress.com/_mNfmMhP) |
| JGS2 (Beam Splitter) 15x30x6mm | 1 | $14,200 | [AliExpress](https://es.aliexpress.com/item/1005008287828744.html) |
| Aluminum alloy to mount CCR and Laser (12mm) | 4 | $900 | [AliExpress](https://es.aliexpress.com/item/1005007882013034.html) |
| Corner Cube Reflectors | 4 | $5,200 | [AliExpress](https://es.aliexpress.com/item/1005009665718638.html) |
| Laser Diode Single Mode (Oclaro HL63022DG 638nm 240mW) | 1 | $16,200 | [AliExpress](https://es.aliexpress.com/item/1005008368594737.html) |
| Laser Diode Collimating Lens with Case | 1 | $900 | [AliExpress](https://es.aliexpress.com/item/1005004747758829.html) |
| M9 Outer Diameter Laser Collimating Lens (F10) | 1 | $2,688 | [AliExpress](https://es.aliexpress.com/item/1005005984643958.html) |
| Powell Lens Holder + Laser Tube Fixed Seat | 1 | $11,400 | [AliExpress](https://es.aliexpress.com/item/1005005514166858.html) |

---

### **Instructions for Electronic System Use**

In general, the system is "plug-and-play"; connecting the power is sufficient to start operation. However, several instructions regarding safety and proper usage must be followed.

**1. ESD Protection**
Before use, it is recommended to work in a safe environment free of static electricity to avoid damage to the laser diode. The basic set for an anti-static space includes an anti-static mat, a wrist strap, and a correct ground connection. Ensure the mat is fixed at the corners to prevent displacement.
<img class="pfloat-center" src="/images/resources/high-coherence-laser/image1.jpg" width="80%" style="display: block; margin: 0 auto;" loading="lazy" data-action=zoom>

**2. Laser Mounting**
This instruction is fundamental before soldering and final assembly. Ensure the laser diode is correctly installed in its mount—it should not be loose or tilted. The diode must be crimped to the mount for a firm fit. **We emphatically recommend completing the mount assembly before soldering the device to the actuator circuit.**

**3. MCU Voltage Tolerance**
Always consider the voltage tolerance of the microcontroller pins. The model used (STM32F103) has some GPIO ports that are 5V tolerant when configured as inputs; otherwise, they only tolerate 3.3V. This is especially relevant for communication protocols that require configuring GPIOs as outputs.

**4. Circuit Connection**
The **Driver** circuit fulfills two main functions:
1.  Converts control signals from the MCU into signals suitable for the actuators.
2.  Energizes the rest of the system circuits (distributing power and ground lines).

The driver has three outputs connected directly to the power line (highlighted in the figure). Note that jumpers were used here for prototyping, but JST connectors are recommended for the final version.
<img class="pfloat-center" src="/images/resources/high-coherence-laser/image2.jpg" width="60%" style="display: block; margin: 0 auto;" loading="lazy" data-action=zoom>

The rest of the connections between boards can be performed as follows:
* **Blue Wire:** Current Control Signal
* **Orange Wire:** Temperature Control Signal
<img class="pfloat-center" src="/images/resources/high-coherence-laser/image3.png" width="80%" style="display: block; margin: 0 auto;" loading="lazy" data-action=zoom>

**5. Current Tuning**
The driver system incorporates a potentiometer configured as a variable resistor, which sets a DC level for the current control signal. It is recommended to start the adjustment with the potentiometer at its minimum value and, using the **testing resistor**, regulate the current until the desired level is reached.
<img class="pfloat-center" src="/images/resources/high-coherence-laser/image4.png" width="60%" style="display: block; margin: 0 auto;" loading="lazy" data-action=zoom>

---

### **Microcontroller Programming**

We use an STM32 microcontroller (BluePill), characterized by its power and versatility. To modify and upload the code, two applications are used: **STM32CubeMX** and **STM32CubeIDE**.

<img class="pfloat-center" src="/images/resources/high-coherence-laser/image5.png" width="40%" style="display: block; margin: 0 auto;" loading="lazy" data-action=zoom>

* **STM32CubeMX:** Allows hardware configuration (GPIO, timers, ADC, clock frequency).
* **STM32CubeIDE:** Integrated development environment for editing, compiling, and programming the code.

**Important:** In newer versions of these programs, you must activate an additional option in STM32CubeMX. Under `Project Manager > Toolchain / IDE`, select **STM32CubeIDE** so the generated code is correctly imported.
<img class="pfloat-center" src="/images/resources/high-coherence-laser/image6.png" width="80%" style="display: block; margin: 0 auto;" loading="lazy" data-action=zoom>

**Operating Modes**
The BluePill development board has a pin that determines if the system is in **Programming Mode** or **Operating Mode**. The figure below indicates the pin and the position for each mode. Always reset the system using the button next to the pins after changing the operation mode.
<img class="pfloat-center" src="/images/resources/high-coherence-laser/image7.jpg" width="60%" style="display: block; margin: 0 auto;" loading="lazy" data-action=zoom>

---

### **Optical Assembly (Interferometer)**

**Assembly Steps**
1.  Paste a sheet of graph paper underneath the tempered glass base to facilitate positioning components with correct angles and distances.
2.  Sand 2 of the aluminum pieces so the 12mm circle is large enough to fit the Corner Cube Reflectors (CCR)—approximately 12.7mm horizontal diameter.
3.  Sand 1 aluminum piece to fit the laser diode mount—approximately 13mm horizontal diameter.
4.  Insert the laser diode into its mount along with the collimating lens.
5.  Mount the laser and CCRs into the aluminum pieces.
6.  **Verification:** Verify that the laser beam does not form an angle with respect to the horizontal. Use an optical card to check that the beam height is the same near the laser and far from it. If an angle forms, replace the aluminum pieces with a tilt-adjustable base.

**Design 1: Simplified Setup**
Assemble the simplified version to determine if fringes can be formed. Place components on the tempered glass base using only double-sided tape to test positions.

* **L:** Laser
* **R:** Retroreflectors (CCR)
* **BS:** Beam Splitter
* **Green/Moss/Dark Green:** Laser paths.

<img class="pfloat-center" src="/images/resources/high-coherence-laser/image8.png" width="80%" style="display: block; margin: 0 auto;" loading="lazy" data-action=zoom>

The mint green path represents the first split: ~90% free for the microscope, ~5% to detector, ~5% to CCR1. The moss green path is the reflection from CCR1. The dark green path is the final reflection from CCR2 combining at the detector.

**Design 2: Final Assembly**
Once fringes are achieved, modify the setup to include the mirror.
1.  Cut the mirror to 20 x 15 x 3 mm.
2.  Move the second CCR to include the mirror as shown in the scheme below.
3.  Continue using double-sided tape for positioning.

<img class="pfloat-center" src="/images/resources/high-coherence-laser/image9.png" width="80%" style="display: block; margin: 0 auto;" loading="lazy" data-action=zoom>

* **Light Blue Rectangle:** Newly included mirror.

When fringes are achieved with the largest optical path difference possible (considering the base dimensions), mark the positions on the base. Remove the double-sided tape, clean the components, and glue them permanently using epoxy.
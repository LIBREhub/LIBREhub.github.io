---
title: 3D Printed Perfusion Chamber for Live Tissue Imaging
description: A comprehensive, low-cost modular system for constant ACSF flow and stable imaging of brain slices.
categories: resource
header-img: /images/resources/perfusion-chamber/image42.jpeg
---

*Developed by Antonia Norambuena Valencia and Vicente Parot. Part of LIBRE\_hub.*

## **3D Printed Perfusion Chamber for Neurophysiology**

A perfusion chamber is an essential tool for maintaining a constant flow of Artificial Cerebrospinal Fluid (ACSF) through a tissue sample. This is fundamental for all-optical neurophysiology imaging in brain slices, where the tissue must remain fixed and viable for long periods.

This guide provides a detailed walkthrough for building a complete perfusion system using a custom chamber manufactured via UV-resin 3D printing, offering a stable and low-cost alternative to commercial setups.

*Note: For the preceding tissue preparation step, see our guide on [Floating Brain Slice Recovery Containers](/2026/01/26/brain-slice-containers.html).*

#### **Components and Tools**

| Qty | Component | Specifications | Provider |
| :---- | :---- | :---- | :---- |
| 1 | UV-curable Resin | Photosensitive, Transparent, 500g | TodoToner.cl |
| 1 | Resin 3D Printer | DLP System, 0.03-0.05 layer height | Creality LD-002H |
| 10m | Tygon PVC Tubing | I.D. 1/16 in. × O.D. 1/8 in. | [McMaster-Carr](https://www.mcmaster.com/5155T12/) |
| 1 | Disposable Syringe | 100 mL | [AliExpress](https://www.aliexpress.com/item/1005004193173946.html) |
| 1 | Syringe tip | 1.5 in long, Blunt end, 18G | [AliExpress](https://www.aliexpress.com/item/1005009553731122.html) |
| 2 | Air Diffusers | Sintered air stone | [AliExpress](https://www.aliexpress.com/item/33003579178.html) |
| 10 | Luer Connectors | Male/Female F29 for 1/8 in. tubing | [AliExpress](https://www.aliexpress.com/item/1005008889289003.html) |
| 1 | Clear Glass Base | 108 x 50 mm (1.5mm thick) | [AliExpress](https://www.aliexpress.com/item/1005007115892256.html) |
| 1 | Coverslip | 24x32 mm (0.13-0.17 thick) | [AliExpress](https://www.aliexpress.com/item/1005004777825814.html) |
| 1 | Epoxy Glue | Two-part transparent | [Amazon](https://www.amazon.com/Gorilla-Epoxy-Minute-ounce-Syringe/dp/B01MFDGJ7D) |
| 1 | Acetic Silicone | Fungicide-free (for glass sealing) | Local Supply |
| 2 | Cylindrical Magnets | 4mm diameter x 6mm length | [AliExpress](https://www.aliexpress.com/item/1005009690626842.html) |
| 1 | Flow Regulator | Manual drip control | [AliExpress](https://www.aliexpress.com/item/1005008530722471.html) |
| 1 | Peristaltic Pump | For waste suction | [AliExpress](https://www.aliexpress.com/item/1005005453098168.html) |
| 1 | Waste Container | 1L, Clear | [AliExpress](https://www.aliexpress.com/item/1005006155924881.html) |
| 2 | Syringe Holders | 3D printed, PLA | [Onshape](https://cad.onshape.com/documents/096c25a9298dd8889e4dec74/w/c5e233639d356c6856bc744c/e/240705b285462483907fc860) |

#### **1\. Design and Printing Instructions**

The chamber was designed in [Onshape](https://www.onshape.com/) to ensure unidirectional flow. The geometry includes specific landing areas for samples and optimized entry/exit ports. A "spiral" interface was integrated to match standard plastic flow regulation pieces, ensuring a secure, leak-free tubing connection.

<img class="pfloat-left" src="/images/resources/perfusion-chamber/image31.jpeg" width="45%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/perfusion-chamber/image32.jpeg" width="45%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>
<img class="pfloat-left" src="/images/resources/perfusion-chamber/image33.jpeg" width="45%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/perfusion-chamber/image36.jpeg" width="45%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>

**Printing Protocol:**

1. **Preparation:** Load the .stl or .ctb files into the printer (e.g., Creality LD-002R).  
2. **Resin Selection:** Use transparent resin for optical clarity.  
3. **Start Print:** Monitor the first layers to ensure adhesion.

<img class="pfloat-left" src="/images/resources/perfusion-chamber/image1.jpeg" width="33%" loading="lazy" data-action=zoom>
<img class="pfloat-left" src="/images/resources/perfusion-chamber/image2.png" width="33%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/perfusion-chamber/image3.jpeg" width="33%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>


**Washing and Curing:**

* **Washing:** Remove parts and wash in Isopropyl Alcohol (IPA) to remove residue.  
* **Curing:** Use a UV chamber (e.g., Creality UW-03) to fully polymerize the parts.

<img class="pfloat-left" src="/images/resources/perfusion-chamber/image4.jpeg" width="24%" loading="lazy" data-action=zoom>
<img class="pfloat-left" src="/images/resources/perfusion-chamber/image5.jpeg" width="24%" loading="lazy" data-action=zoom>
<img class="pfloat-left" src="/images/resources/perfusion-chamber/image6.jpeg" width="24%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/perfusion-chamber/image7.jpeg" width="24%" loading="lazy" data-action=zoom>

#### **2\. Post-Processing and Assembly**

**Refinement:**

<img class="pfloat-left" src="/images/resources/perfusion-chamber/image8.jpeg" width="33%" loading="lazy" data-action=zoom>
<img class="pfloat-left" src="/images/resources/perfusion-chamber/image9.jpeg" width="33%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/perfusion-chamber/image10.jpeg" width="33%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>


**Chamber and Base Assembly:**

Apply silicone sealant to the bottom of the chamber and press it onto the 107x50mm glass base. Install the 4mm magnet into the recess.

<img class="pfloat-left" src="/images/resources/perfusion-chamber/image11.jpeg" width="33%" loading="lazy" data-action=zoom>
<img class="pfloat-left" src="/images/resources/perfusion-chamber/image12.jpeg" width="33%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/perfusion-chamber/image13.jpeg" width="33%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>


**The Lid and Final Sealing:**

Secure the coverslip to the porous base of the lid frame using epoxy. Seal the entire chamber to the glass base using acetic silicone to ensure no leaks.

<img class="pfloat-left" src="/images/resources/perfusion-chamber/image14.jpeg" width="33%" loading="lazy" data-action=zoom>
<img class="pfloat-left" src="/images/resources/perfusion-chamber/image15.jpeg" width="33%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/perfusion-chamber/image45.jpeg" width="33%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>


#### **3\. Setup Integration**

**ACSF Reservoirs:**

Mount 100mL syringes in holders. Connect them to the chamber entry via Luer adapters and Tygon tubing, including an inline flow regulator.

<img class="pfloat-left" src="/images/resources/perfusion-chamber/image20.jpeg" width="24%" loading="lazy" data-action=zoom>
<img class="pfloat-left" src="/images/resources/perfusion-chamber/image21.jpeg" width="24%" loading="lazy" data-action=zoom>
<img class="pfloat-left" src="/images/resources/perfusion-chamber/image22.jpeg" width="24%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/perfusion-chamber/image24.jpeg" width="24%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>


**Suction and Waste:**

The magnetic suction tip allows for millimetric adjustment of the fluid level. Connect this to the peristaltic pump and waste container.

<img class="pfloat-left" src="/images/resources/perfusion-chamber/image18.jpeg" width="33%" loading="lazy" data-action=zoom>
<img class="pfloat-left" src="/images/resources/perfusion-chamber/image19.jpeg" width="33%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/perfusion-chamber/image23.jpeg" width="33%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>


**Gasification (Carbogen):**

Install the gas network from the Carbogen cylinder. Use a bifurcation to oxygenate both the reservoir and the ex-vivo slices.

<img class="pfloat-left" src="/images/resources/perfusion-chamber/image26.jpeg" width="33%" loading="lazy" data-action=zoom>
<img class="pfloat-left" src="/images/resources/perfusion-chamber/image27.jpeg" width="33%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/perfusion-chamber/image28.jpeg" width="33%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>


**Final System Check:**

Before experiments, test the flow and verify that the "spiral" connectors are secure.

<img class="pfloat-left" src="/images/resources/perfusion-chamber/image38.jpeg" width="24%" loading="lazy" data-action=zoom>
<img class="pfloat-left" src="/images/resources/perfusion-chamber/image39.jpeg" width="24%" loading="lazy" data-action=zoom>
<img class="pfloat-left" src="/images/resources/perfusion-chamber/image40.jpeg" width="24%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/perfusion-chamber/image41.jpeg" width="24%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>
<img class="pfloat-left" src="/images/resources/perfusion-chamber/image42.jpeg" width="45%" loading="lazy" data-action=zoom>
<img class="pfloat-right" src="/images/resources/perfusion-chamber/image46.jpeg" width="45%" loading="lazy" data-action=zoom>
<div style="clear:both;"></div>


#### **Design Files**

Access the CAD files and repositories below:

* [Onshape Project \- Perfusion Chamber](https://www.onshape.com/)  
* [STL Repositories \- LabParot](https://www.google.com/search?q=https://github.com/vparot/)
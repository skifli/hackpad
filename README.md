# hackpad

- [hackpad](#hackpad)
  - [Project Structure](#project-structure)
  - [Journal](#journal)
  - [PCB](#pcb)
    - [Schematic](#schematic)
    - [PCB Design](#pcb-design)
    - [PCB Render](#pcb-render)
  - [CAD](#cad)
  - [BOM](#bom)
  - [Software](#software)

| Cover                            | Exploded View                                    |
| -------------------------------- | ------------------------------------------------ |
| ![cover photo](assets/cover.png) | ![exploded view photo](assets/exploded-view.jpg) |

A fully wireless macropad with 14 Choc v1 Ambient Nocturnal switches, 2 rotary encoders (with a push-button each), and a small screen! The case is in two sections - a top and bottom, and joins together via 8 magnets, half in each side of the case (you can see the magnet holes in the various views).

I made this project because when programming / doing CAD design there are so many different shortcuts I use to make sketches, change orbit types, etc, and these require a lot of clicks. These all could be streamlined a lot more with the use of a macropad - which is why I made this one. I decided to also add a screen so I could easily see which profile I'm on and switch (likely by rotating a rotary encoder while it is held down), and the two rotary encoders to easily control multiple audio streams (mainly YouTube vs. Spotify).

## Project Structure

> [!TIP]\
> Only includes files / folders relevant to admin that would benefit from explanation.

```
└── 📁hackpad
    └── 📁design
        └── 📁cad
            ├── case_bottom.step
            ├── case_top.step
        └── 📁pcb
            ├── ... # Contains the KiCad directory for the PCB
        └── 📁plate
            ├── ... # Contains the KiCad directory for the plate, which is made from an exported DXF from the Fusion 360 Sketch (plate.dxf)
    ├── JOURNAL.md # The journal of the design process
    └── README.md # This file
```

> [!WARNING]\
> The KiCad plate PCB gives [malformed outline warnings](JOURNAL.md#20072025) and doesn't show correctly in 3D view - no idea why, but when exported with the Fabrication Toolkit and imported into JLCPCB it's totally fine 🗿 (if it works, it works™). 

## Journal

The [journal](JOURNAL.md) contains each day's work, logged, with the aid of images. Total time is at the top and each day has its time logged. There is also a Table of Contents for easy navigation :).

> [!NOTE]\
> Total time spent: **54h**

## PCB

### Schematic

![kicad schematic](assets/schematic.svg)

### PCB Design

![kicad pcb design](assets/pcb-design.svg)

### PCB Render

![kicad pcb render](assets/pcb-render.png)

## CAD

| Case Top Side View (from the bottom)                 | Case Bottom Side View (from the top)                       |
| ---------------------------------------------------- | ---------------------------------------------------------- |
| ![case top side only](assets/case-top-side-only.png) | ![case bottom side only](assets/case-bottom-side-only.png) |

| Case Plate                                     | Case USB Port                              |
| ---------------------------------------------- | ------------------------------------------ |
| ![case plate only](assets/case-plate-only.png) | ![case usb port](assets/case-usb-port.png) |

## BOM

> [!TIP]\
> The BOM is split into the different companies from which the components would be bought, with an empty line delimiting them. As well as this, at the end of each section, the total price for that provider, along with the shipping, is provided in the **Price** column. There is also the total price in the aforementioned column on the last row.

> [!NOTE]\
> I found the promo code **KBDNEWS** for Mechboards (a UK-based merchant) 5% off so I included that in the BOM as well to explain the decrease in total price.

<details open>
<summary>BOM in table format</summary>

| Component                                   | Description                     | Notes                                                                              | Quantity | Provider          | Price       | Shipping                 |
| ------------------------------------------- | ------------------------------- | ---------------------------------------------------------------------------------- | -------- | ----------------- | ----------- | ------------------------ |
| Kailh Choc Hotswap Sockets                  | V1 (Pack of 10)                 |                                                                                    | 2        | Mechboards        | £6.00       | £5.28                    |
| JST PH 2-Pin Cable - Male Header            |                                 | I am going to wire the battery to the Slide Switch and then to the nice!nano v2    | 1        | Mechboards        | £2.00       |                          |
| nice!nano v2                                |                                 |                                                                                    | 1        | Mechboards        | £27.50      |                          |
| nice!view                                   |                                 |                                                                                    | 1        | Mechboards        | £16.00      |                          |
| DDC Choc (v1) PBT Blank Keycaps - White     | White Keycaps / 1u (Pack of 10) |                                                                                    | 1        | Mechboards        | £4.50       |                          |
| DDC Choc (v1) PBT Blank Keycaps - Black     | Black Keycaps / 1u (Pack of 10) |                                                                                    | 1        | Mechboards        | £4.50       |                          |
| lowprokb Choc (V1) Ambients Nocturnal       | (Pack of 10)                    |                                                                                    | 2        | Mechboards        | £19.00      |                          |
| KBDNEWS Promo Code                          |                                 |                                                                                    |          | Mechboards        | -5%         |                          |
| **Total (Mechboards)**                      |                                 |                                                                                    |          |                   | **£80.81**  | **Included on the left** |
| JST PH 2-Pin Cable - Female Connector 150mm |                                 | I am going to wire the battery to the Slide Switch and then to the nice!nano v2    | 1        | The Pi Hut        | £0.80       | £7.80                    |
| Heat Shrink Pack                            |                                 | Same as above, just to cover the joints for safety                                 | 1        | The Pi Hut        | £4.30       |                          |
| 150mAh 3.7V LiPo Battery                    |                                 |                                                                                    | 1        | The Pi Hut        | £4.50       |                          |
| Breadboard-friendly SPDT Slide Switch       |                                 |                                                                                    | 1        | The Pi Hut        | £0.80       |                          |
| 1N4148 SMT SOD-123 Diodes                   | (Pack of 100)                   |                                                                                    | 1        | The Pi Hut        | £4.80       |                          |
| Rotary Encoder + Extras                     | (Pack of 2)                     | It says extras but there's no mention of anything else on the product page LOL ;-; | 2        | The Pi Hut        | £8.60       |                          |
| Rubber Bumper Feet                          | (Pack of 4)                     | 4 for the case bottom and 4 for the PCB bottom for a set height                    | 2        | The Pi Hut        | £1.80       |                          |
| **Total (The Pi Hut)**                      |                                 |                                                                                    |          |                   | **£33.40**  | **Included on the left** |
| Comus M1219-3 Neodynium Disc Magnet         |                                 | To join the two case halves                                                        | 8        | Rapid Electronics | £3.48       | £3.30                    |
| **Total (Rapid Electronics)**               |                                 |                                                                                    |          |                   | **£6.58**   | **Included on the left** |
| Custom PCB                                  | PCB (JLCPCB) (x1)               |                                                                                    | 1        | JLCPCB            | £1.49       | £19.47                   |
| Custom Plate                                | PCB (JLCPCB) (x1)               | Only one special offer is valid in shopping cart :(.                               | 1        | JLCPCB            | £2.97       |                          |
| **Total (JLCPCB)**                          |                                 |                                                                                    |          |                   | **£23.93**  | **Included on the left** |
| **TOTAL**                                   |                                 |                                                                                    |          |                   | **£144.72** |                          |


</details>

The BOM can be found in [`/bom.csv`](bom.csv). Since this is my first ever hardware project, I decided to go for some products that were easier to find footprints / symbols in KiCad for. With hindsight, spending the amount of money I now have to on a nice! nano v2 or nice!view (which I landed on because I chose the nice! nano v2) isn't really necessary. So, in future projects I'll choose other, cheaper components - but for this one I've already designed the PCB etc, and was very new to this whole world of design, and so decided to go with components that I was more confident with.

The Seeed Studio XIAO RP2040 didn't have enough GPIO anyway since I needed a 4x4 key matrix (so 8 pins), 4 other GPIO for the 2 rotary encoders, and the screen pins. Now, unfortunately this does mean the price is way over $150. This is in part because I also forgot Hackclub operates in USD and so was sure I would be in price range until 2 days ago, at which point I had a heart attack 😭. I'll try to cover the rest myself... not really sure how that'll go because I need to buy solder and other stuff since this is my first hardware project (which is already a lot of money), but we'll see... I'm not sure if Hackclub has a thing with JLCPCB for cheaper PCBs but if so that would reduce the total cost, although it might still be just over $150.

## Software

Will be added once the physical components are received and assembled, as I don't want to start writing code and then find out it doesn't work because I accidentally used libraries for different components, or something similar to that.

---
<sub>Thanks to [Hackclub](https://hackclub.com) for such an amazing opportunity - this project was made by [@skifli](https://github.com/skifli) with 🩷, under the [MIT License](LICENSE).</sub>
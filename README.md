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


> [!IMPORTANT]\
> Since submission, the BOM price has decreased to $119.89 from above $150 (check [#bom](#bom) for more information).

A fully wireless macropad with 14 Choc v1 Ambient Nocturnal switches, 2 rotary encoders (with a push-button each), and a small screen! The case is in two sections - a top and bottom, and joins together via 8 magnets, half in each side of the case (you can see the magnet holes in the various views).

I made this project because when programming / doing CAD design there are so many different shortcuts I use to make sketches, change orbit types, etc, and these require a lot of clicks. These all could be streamlined a lot more with the use of a macropad - which is why I made this one. I decided to also add a screen so I could easily see which profile I'm on and switch (likely by rotating a rotary encoder while it is held down), and the two rotary encoders to easily control multiple audio streams (mainly YouTube vs. Spotify).

## Project Structure

> [!IMPORTANT]\
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
> Total time spent: **60h**

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

<details closed>
<summary>BOM in table format</summary>

| Component                               | Description                     | Notes                                            | Qty | Price      | Shipping   | Provider   | Link                                                                                                               |
| --------------------------------------- | ------------------------------- | ------------------------------------------------ | --- | ---------- | ---------- | ---------- | ------------------------------------------------------------------------------------------------------------------ |
| Kailh Choc Hotswap Sockets              | V1 (Pack of 10)                 |                                                  | 2   | £6.00      | £1.81      | Mechboards | [Link](https://mechboards.co.uk/products/kailh-choc-hotswap-sockets?variant=40427263754445)                        |
| DDC Choc (v1) PBT Blank Keycaps - White | White Keycaps / 1u (Pack of 10) |                                                  | 1   | £4.50      | –          | Mechboards | [Link](https://mechboards.co.uk/products/ddc-choc-pbt-blank-keycaps?variant=47587896426701)                        |
| DDC Choc (v1) PBT Blank Keycaps - Black | Black Keycaps / 1u (Pack of 10) |                                                  | 1   | £4.50      | –          | Mechboards | [Link](https://mechboards.co.uk/products/ddc-choc-pbt-blank-keycaps?variant=47405364576461)                        |
| lowprokb Choc (V1) Ambients Nocturnal   | (Pack of 10)                    |                                                  | 2   | £19.00     | –          | Mechboards | [Link](https://mechboards.co.uk/products/lowprokb-ambients-silent-linear-nocturnal-choc-v1?variant=47588169908429) |
| KBDNEWS Promo Code                      |                                 |                                                  | –   | –£0.94     | –          | –          | –                                                                                                                  |
| **Total (Mechboards)**                  |                                 |                                                  |     | **£34.11** | *Included* |            |                                                                                                                    |
| nice!nano v2                            |                                 | Compatible board                                 | 1   | £2.99      | £2.99      | AliExpress | [Link](https://www.aliexpress.com/item/1005006035267231.html)                                                      |
| nice!view                               |                                 | Compatible screen (without headers)              | 1   | £12.69     | –          | AliExpress | [Link](https://www.aliexpress.com/item/1005008115497843.html)                                                      |
| Header Pins                             | 1x5 Pins (50 PCS)               | Headers for the above screen                     | 1   | £1.15      | –          | AliExpress | [Link](https://www.aliexpress.com/item/4000988113226.html)                                                         |
| Tiny Disc Magnet                        | 4x3mm (100 PCS)                 | To join the top and bottom of the case           | 1   | £4.86      | £2.96      | AliExpress | [Link](https://www.aliexpress.com/item/1005009177139622.html)                                                      |
| SMT SOD-123 Diodes                      | 100 PCS                         | For the switches                                 | 1   | £1.11      | –          | AliExpress | [Link](https://www.aliexpress.com/item/4000685043735.html)                                                         |
| Heat Shrink Tubes                       |                                 | For wiring between switch, battery, nice!nano v2 | 1   | £1.35      | –          | AliExpress | [Link](https://www.aliexpress.com/item/1005008146302901.html)                                                      |
| JST PH Plug Connector with Wire (M)     | MALE 2P 100mm (5 PCS)           | For battery wiring                               | 1   | £0.34      | £1.94      | AliExpress | [Link](https://www.aliexpress.com/item/1005008864177105.html)                                                      |
| JST PH Plug Connector with Wire (F)     | FEMALE 2P 100mm (5 PCS)         | For battery wiring                               | 1   | £0.49      | £1.94      | AliExpress | [Link](https://www.aliexpress.com/item/1005008864177105.html)                                                      |
| Bumper Feet                             | 5mm x 2mm (100 PCS)             | For bottom of the case and PCB                   | 1   | £1.59      | –          | AliExpress | [Link](https://www.aliexpress.com/item/1005004068119765.html)                                                      |
| Toggle Switch                           | K031b004-G3                     | To power on/off the system                       | 1   | £1.94      | –          | AliExpress | [Link](https://www.aliexpress.com/item/1005009306874094.html)                                                      |
| 3.7V 150mAh                             | 1 battery                       | To power the system                              | 1   | £4.74      | N/A        | AliExpress | [Link](https://www.aliexpress.com/item/1005004084377638.html)                                                      |
| Rotary Encoder w/ Push Button           | 5 PCS                           |                                                  | 1   | £1.08      | –          | AliExpress | [Link](https://www.aliexpress.com/item/1005005983134515.html)                                                      |
| **Total (AliExpress)**                  |                                 |                                                  |     | **£42.35** | *Included* |            |                                                                                                                    |
| Plate & PCB                             |                                 |                                                  |     | £5.94      | £6.11      | JLCPCB     | N/A                                                                                                                |
| **Total (JLCPCB)**                      |                                 |                                                  |     | **£12.05** | *Included* |            |                                                                                                                    |
| **TOTAL**                               |                                 |                                                  |     | **£88.51** | *Included* |            |                                                                                                                    |  |

</details>

> [!IMPORTANT]\
> Please disregard a lot of what is in the below text. After someone in the Slack (@Toby), introduced me to the world of AliExpress, I completely redid the BOM. It is now $119.89 (yes that is USD lol), so way under the limit. Thanks a lot dude :).

The BOM can be found in [`/bom.csv`](bom.csv). Since this is my first ever hardware project, I decided to go for some products that were easier to find footprints / symbols in KiCad for. With hindsight, spending the amount of money I now have to on a nice! nano v2 or nice!view (which I landed on because I chose the nice! nano v2) isn't really necessary. So, in future projects I'll choose other, cheaper components - but for this one I've already designed the PCB etc, and was very new to this whole world of design, and so decided to go with components that I was more confident with.

The Seeed Studio XIAO RP2040 didn't have enough GPIO anyway since I needed a 4x4 key matrix (so 8 pins), 4 other GPIO for the 2 rotary encoders, and the screen pins. Now, unfortunately this does mean the price is way over $150. This is in part because I also forgot Hackclub operates in USD and so was sure I would be in price range until 2 days ago, at which point I had a heart attack 😭. I'll try to cover the rest myself... not really sure how that'll go because I need to buy solder and other stuff since this is my first hardware project (which is already a lot of money), but we'll see... I'm not sure if Hackclub has a thing with JLCPCB for cheaper PCBs but if so that would reduce the total cost, although it might still be just over $150.

## Software

Will be _mostly_ added once the physical components are received and assembled, as I don't want to start writing code and then find out it doesn't work because I accidentally used libraries for different components, or something similar to that.

I have added some stuff in the [`/software`](software) directory though.

---
<sub>Thanks to [Hackclub](https://hackclub.com) for such an amazing opportunity - this project was made by [@skifli](https://github.com/skifli) with 🩷, under the [MIT License](LICENSE).</sub>
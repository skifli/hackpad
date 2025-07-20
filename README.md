# hackpad

- [hackpad](#hackpad)
  - [Project Structure](#project-structure)
  - [PCB](#pcb)
    - [Schematic](#schematic)
    - [PCB Design](#pcb-design)
    - [PCB Render](#pcb-render)
  - [CAD](#cad)

| Cover                            | Exploded View                                    |
| -------------------------------- | ------------------------------------------------ |
| ![cover photo](assets/cover.png) | ![exploded view photo](assets/exploded-view.jpg) |

A macropad with 14 Choc v1 Ambient Nocturnal switches, 2 rotary encoders, and a small screen! The case is in two sections - a top and bottom, and joins together via 8 magnets, half in each side of the case (you can see the magnet holes in the various views).

I made this project because when programming / doing CAD design there are so many different shortcuts I use to make sketches, change orbit types, etc, and these require a lot of clicks. These all could be streamlined a lot more with the use of a macropad - which is why I made this one. I decided to also add a screen so I could easily see which profile I'm on and switch, and the two rotary encoders to easily control multiple audio streams (mainly YouTube vs. Spotify).

## Project Structure

> [!TIP]\
> Only includes files / folders relevant to admin that would benefit from explanation.

```
└── 📁hackpad
    └── 📁design
        └── 📁cad
            ├── case_bottom.step
            ├── case_top.step
            ├── plate.step
        └── 📁pcb
            ├── ... # Contains the KiCad directory for the project
    ├── JOURNAL.md # The journal of the design process
    └── README.md # This file
```

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
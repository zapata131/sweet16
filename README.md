# Sweet 16 Macro Keyboard

- [Keyboard Customization](#keyboard-customization)
  - [Flashing the Keyboard](#flashing-the-keyboard)
- [General Layout](#general-layout)
- [Layers](#layers)
  - [Layer 0](#layer-0)
  - [Layer 1](#layer-1)
- [Keyboard Macros](#keyboard-macros)

The Sweet 16 Macro Keyboard bu 1UP Keyboards uses QMK (Quantum Mechanical Keyboard) Firmware. These allows to have different layers and interesting usability for this 4x4 keyboard.

This document details the customization of the QMK Firmware for my own usability. Since I use my computer for different things, I want to purpose different layers for different tasks I commonly use.

The following Sections detail the layout convention I'm using for this document and an explanation of the different layers.

## Keyboard Customization

I'm using the Keyboard Firmware Builder
at <kbfirmware.com> to modify and customize the firmware. This Firmware builder allows you to customize your keyboard using a graphic UI in your browser.

Each time you compile your project, the page generates a HEX file called `zapata16.hex` that you can flash on your keyboard using the QMK Toolbox.

I'm also saving a JSON configuration file named `zapata16.json` that you can upload to the Keyboard Firmware Builder and has the layout, macros, and current configuration of the firmware.

### Flashing the Keyboard

Flashing the keyboard allows you to upload new firmware. Before flashing the Sweet 16 Keyboard you need:

- [QMK Toolbox](https://qmk.fm/toolbox/)
- The proper HEX files

To upload the firmware:

1. Open the QMK Toolbox.
2. In the **Local file** field, type or select the path to the HEX file you want to flash.
3. On the **MCU (AVR only)**, select the **atmega32u4** option.
4. Connect the keyboard to the computer.
5. Press twice the reset button to load DFU mode.
6. If autoflash is enabled you should see the toolbox installing the firmware being as soon as the keyboard is recognized.
7. If autoflash is not enabled click “Flash” once the keyboard enters in DFU mode have finished installing.

After following this steps, the toolbox shows a confirmation message and you can start using your keyboard with the new firmware.

## General Layout

The Sweet 16 Keyboard has 16 keys arranged in a 4x4 grid. For the purposes of these document, we are defining the name of the keys by number regardless of the layer.

For the purpose of these documentation, we name the keys in the first row of the keyboard as `key01`, `key02`, `key03`, and `key04` from left to right. The following row has `key05`, `key06` and so on for the following rows and keys.

## Layers

The QMK firmware allows to have multiple keybord layers that change layout and usability. For usability, we are using the `key13` (the red key) to change layers.

Right now I'm using two layers:

- **Layer 0**: General work and OS-level shortcuts.
- **Layer 1**: Video editing (DaVinci Resolve) Shortcuts

QMK allows yuou to create keyboard macros, so most of the usability of the keyboard exploits this feature.

The following section detail the layout and usability of each layer.

### Layer 0

Layer 0 is my base layer. It has shortcut macros used for navigation in Chrome and other OS-level shortcuts.

The following table shows the current usage of each key.


| Layer 0 | - | - | - |
|-|-|-|-|
| Zoom Audio Toggle | Zoom Video Toggle | NA | NA |
| Undo (Macro 8) | Redo (Macro 9) | NA | NA |
| Back in Chrome (Macro 4) | Forward in Chrome (Macro 5) | Previous tab in Chrome (Macro 6) | NExt tab in Chrome (Macro 7) |
| Changes to Layer 1 | New Tab in Chrome (Macro 1) | Open last closed tab in Chrome (Macro 2) | Closes current tab in Chorme (Macro 3) |

For a detailed explanaition of each macro, see the [Keyboard Macros](#keyboard-macros) section.

### Layer 1

Layer 1 is my video editing layer. It has shortcut macros used in Da Vinci Resolve. It is a work in progress.

The following table shows the current usage of each key.


| Layer 1 | - | - | - |
|-|-|-|-|
| NA | NA | NA | NA |
| NA | NA | NA | NA |
| Ripple Delete from Start | Ripple Delete to End | Zoom In | Zoom Out |
| Changes to Layer 0 |  Link/Unlink Clips (Macro 14) | Split Clips (Macro 15) | B-Roll (Macro 0) |

For a detailed explanaition of each macro, see the [Keyboard Macros](#keyboard-macros) section.


## Keyboard Macros

The following is a list of all the macros in this configuration and their usage.

- **Macro 0**: In DaVinci Resolve, unlinks audio and video and adds the retime controls. Special for B-Roll.
- **Macro 1**: In Chrome, opens a new tab (⌘+T).
- **Macro 2**: In Chrome, opens last closed tab (⌘+Shift+T).
- **Macro 3**: In Chrome, closes the current tab (⌘+W).
- **Macro 4**: In Chrome, last page (⌘+[ ).
- **Macro 5**: In Chrome, next page (⌘+] ).
- **Macro 6**: In Chrome, previous tab. (⌘+PgUp)
- **Macro 7**: In Chrome, next tab (⌘+PgDN).
- **Macro 8**: Undo (⌘+Z).
- **Macro 9**: Redo (⌘+Shift+Z).
- **Macro 10**: NA.
- **Macro 11**: NA.
- **Macro 12**: In Zoom, Audio toggle (⌘+A).
- **Macro 13**: In Zoom, Video toggle (⌘+V).
- **Macro 14**: In DaVinci Resolve, toggles clip linking (⌥+⌘+L).
- **Macro 15**: In DaVinci Resolve, splits clips (⌘+\\).
- **Macro 16**: In DaVinci Resolve, ripple delete from start (Shift+⌘+[).
- **Macro 17**: In DaVinci Resolve, ripple delete to end (Shift+⌘+]).
- **Macro 18**: In DaVinci Resolve, zoom out (⌘ + -).
- **Macro 19**: In DaVinci Resolve, zoom in (⌘ + +).

Note: The following characters represent some of the special keys.
- ⌘ is also known as Command or Cmd
- ⌥ is also known as Option or Alt
- ⌃ is also known as Ctrl
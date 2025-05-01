# Sweet 16 Macro Keyboard

- [Keyboard Customization](#keyboard-customization)
  - [Flashing the Keyboard](#flashing-the-keyboard)
- [General Layout](#general-layout)
- [Layers](#layers)
  - [Layer 0 – macOS + Chrome](#layer-0--macos--chrome)
  - [Layer 1 – DaVinci Resolve](#layer-1--davinci-resolve)
  - [Layer 2 – Affinity Designer](#layer-2--affinity-designer)
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

Right now I'm using three layers:

- **Layer 0**: macOS + Chrome shortcuts  
- **Layer 1**: DaVinci Resolve editing tools  
- **Layer 2**: Affinity Designer layout and editing controls

QMK allows yuou to create keyboard macros, so most of the usability of the keyboard exploits this feature.

The following section detail the layout and usability of each layer.

### Layer 0 – macOS + Chrome {#layer-0}

| Key    | Shortcut              | Explanation                                |
|--------|-----------------------|--------------------------------------------|
| Key00  | ⌘ + C                 | Copy                                        |
| Key01  | ⌘ + V                 | Paste                                       |
| Key02  | ⌘ + Z                 | Undo                                        |
| Key03  | Layer toggle          | Switch to next layer                        |
| Key04  | ⌘ + ⇧ + 4             | Screenshot (selected area)                 |
| Key05  | ⌘ + Tab               | App switcher                               |
| Key06  | ⌘ + W                 | Close window/tab                            |
| Key07  | ⌘ + Space             | Spotlight search                           |
| Key08  | ⌘ + T                 | New tab (Chrome)                           |
| Key09  | ⌘ + ⇧ + T             | Reopen last closed tab                     |
| Key10  | ⌘ + ⇧ + N             | New incognito window                       |
| Key11  | ⌘ + R                 | Reload page                                |
| Key12  | ⌘ + Option + ←        | Previous tab                               |
| Key13  | ⌘ + Option + →        | Next tab                                   |
| Key14  | Control + ⇧ + Tab     | Universal previous tab                     |
| Key15  | ⌘ + W                 | Close tab (near tab navigation keys)       |

### Layer 1 – DaVinci Resolve {#layer-1}

| Key    | Shortcut              | Explanation                                |
|--------|-----------------------|--------------------------------------------|
| Key00  | J                     | Play reverse                               |
| Key01  | K                     | Stop playback                              |
| Key02  | L                     | Play forward                               |
| Key03  | Layer toggle          | Switch to next layer                       |
| Key04  | [                     | Previous keyframe                          |
| Key05  | ]                     | Next keyframe                              |
| Key06  | Option + Delete       | Ripple delete forward                      |
| Key07  | Shift + Delete        | Ripple delete backward                     |
| Key08  | A                     | Selection mode                             |
| Key09  | T                     | Trim mode                                  |
| Key10  | B                     | Blade tool                                 |
| Key11  | ⌘ + B                 | Cut at playhead                            |
| Key12  | ↑                     | Previous edit                              |
| Key13  | ↓                     | Next edit                                  |
| Key14  | ←                     | Step back one frame                        |
| Key15  | →                     | Step forward one frame                     |

### Layer 2 – Affinity Designer {#layer-2}

| Key    | Shortcut              | Explanation                                |
|--------|-----------------------|--------------------------------------------|
| Key00  | V                     | Move tool                                  |
| Key01  | A                     | Node tool                                  |
| Key02  | P                     | Pen tool                                   |
| Key03  | Layer toggle          | Switch to next layer                       |
| Key04  | ⌘ + G                 | Group selection                            |
| Key05  | ⌘ + ⇧ + G             | Ungroup                                    |
| Key06  | ⌘ + Z                 | Undo                                       |
| Key07  | ⌘ + ⇧ + Z             | Redo                                       |
| Key08  | ⌘ + C                 | Copy                                       |
| Key09  | ⌘ + V                 | Paste                                      |
| Key10  | ⌘ + D                 | Deselect                                   |
| Key11  | T                     | Text tool                                  |
| Key12  | ⌘ + ⇧ + ]             | Bring to front                             |
| Key13  | ⌘ + ]                 | Bring forward                              |
| Key14  | ⌘ + [                 | Send backward                              |
| Key15  | ⌘ + ⇧ + [             | Send to back                               |

---

Note: The following characters represent some of the special keys.
- ⌘ is also known as Command or Cmd
- ⌥ is also known as Option or Alt
- ⌃ is also known as Ctrl

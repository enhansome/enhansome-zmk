<h3 align="center"><img src="images/logo2.png" alt="logo2"></h3>

# Awesome ZMK with stars

A curated list of awesome ZMK firmware resources, links, zmk-config's, zmk-drivers, tools, hardware, and community projects.

## Contents

<a name="top"></a>

* [What is ZMK](#what-is-zmk)
  * [What is a board](#what-is-a-board)
  * [What is a shield](#what-is-a-shield)
  * [What are Modules](#what-are-modules)
* [Official Resources](#official-resources)
  * [Additional Resources](#additional-resources)
* [Quick start](#quick-start)
* [Community zmk-config user configurations](#community-zmk-config-user-configurations)
  * [Split Wired](#split-wired)
* [Community Documentation](#community-documentation)
  * [Useful Awesome List](#useful-awesome-list)
  * [Vendor Documentation](#vendor-documentation)
* [Community firmware Modules and Behaviors](#community-firmware-modules-and-behaviors)
  * [Custom Behaviors](#custom-behaviors)
  * [Drivers](#drivers)
    * [Drivers Trackpad](#drivers-trackpad)
    * [Drivers Trackball](#drivers-trackball)
    * [Drivers Trackpoint](#drivers-trackpoint)
    * [Drivers Analog Joystick](#drivers-analog-joystick)
    * [Drivers Haptic](#drivers-haptic)
    * [Drivers Display](#drivers-display)
    * [Drivers LEDS Backlight Underglow](#drivers-leds-backlight-underglow)
    * [Drivers Others](#drivers-others)
  * [Display Modules](#display-modules)
    * [Dongles Modules](#dongles-modules)
      * [Dongles Design](#dongles-design)
      * [Dongle Prospector Vendor](#dongle-prospector-vendor)
    * [Display Modules Hardware](#display-modules-hardware)
* [Tools and Software](#tools-and-software)
  * [Keymap Editors GUI](#keymap-editors-gui)
  * [Power Estimation](#power-estimation)
  * [Display Utilities](#display-utilities)
  * [RAW HID Host](#raw-hid-host)
  * [CLI and Utilities](#cli-and-utilities)
* [Hardware Addons must-have](#hardware-addons-must-have)
* [Community Pointing Projects as Computer Mouse](#community-pointing-projects-as-computer-mouse)
* [Guides and Tutorials](#guides-and-tutorials)
  * [Bootloader and Reset](#bootloader-and-reset)
  * [Solder and Desolder Tools](#solder-and-desolder-tools)
  * [How to Solder](#how-to-solder)
  * [How to Desolder](#how-to-desolder)
  * [Solder and Desolder Videos](#solder-and-desolder-videos)
  * [Supported Hardware](#supported-hardware)
  * [Hardware Tutorials](#hardware-tutorials)
  * [Software Tutorials](#software-tutorials)
  * [Learn Touch Typing](#learn-touch-typing)
* [Keyboard Shops](#keyboard-shops)
* [Keyboard News](#keyboard-news)
  * [Keyboard News Videos](#keyboard-news-videos)
* [Projects using ZMK closed-source or not upstreamed](#projects-using-zmk-closed-source-or-not-upstreamed)
* [Related projects](#related-projects)
* [License](#license)

***

## What is ZMK

> Pete Johanson [^6] is the creator and lead maintainer of the ZMK Firmware project

Zephyr™ Mechanical Keyboard (ZMK) Firmware

[![Discord](https://img.shields.io/discord/719497620560543766)](https://zmk.dev/community/discord/invite)
[![Build](https://github.com/zmkfirmware/zmk/workflows/Build/badge.svg)](https://github.com/zmkfirmware/zmk/actions) ⭐ 4,219 | 🐛 420 | 🌐 C | 📅 2026-08-17
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-v2.0%20adopted-ff69b4.svg)](CODE_OF_CONDUCT.md)
![GitHub last commit](https://img.shields.io/github/last-commit/zmkfirmware/zmk) ![GitHub Repo stars](https://img.shields.io/github/stars/zmkfirmware/zmk)

[ZMK Firmware](https://zmk.dev/) [^1][^2] is an open source (MIT) keyboard firmware built on the [Zephyr™ Project](https://www.zephyrproject.org/) Real Time Operating System (RTOS) [^3][^4]. ZMK's goal is to provide a modern, wireless, and powerful firmware free of licensing issues.

### What is a board

In ZMK, a board defines the PCB that includes the microcontroller unit (MCU). For keyboards, this is one of two options:

Complete keyboard PCBs that include the MCU (e.g. the Planck or Preonic).
Small MCU boards (e.g. the nice!nano or Seeed Studio Xiao RP2040) that expose pins and are designed to be combined with larger keyboard PCBs, or hand-wired to switches to create the final keyboard [^12].

### What is a shield

In ZMK, a shield is a PCB or hardwired set of components that when combined with an MCU-only board, like the SparkFun Pro Micro RP2040 or nice!nano, results in a complete usable keyboard. Examples would be keyboard PCBs like the Kyria or Lily58. The shield is usually the big PCB containing all the keys [^12].

### What are Modules

ZMK makes use of Zephyr modules to include additional source code or configuration files into its build. You can think of them as similar to plugins or themes. The most common uses of this feature are:

* Building firmware for a keyboard external to ZMK's tree [^13]
* Adding functionality to ZMK, such as a driver or a behavior [^13]

## Official Resources

* [ZMK Documentation](https://zmk.dev/docs) - The primary source for all information regarding ZMK.
* [ZMK GitHub Repository](https://github.com/zmkfirmware/zmk) ⭐ 4,219 | 🐛 420 | 🌐 C | 📅 2026-08-17 - The source code and development hub.
* [ZMK Discord Server](https://discord.com/invite/sycytVQ) - The main hub for community discussion, support, and development.

### Additional Resources

Zephyr Project:

* [Zephyr Project Documentation](https://docs.zephyrproject.org/latest/develop/getting_started/index.html) - The underlying RTOS for ZMK. Useful for deep-dives and driver development.
* [Zephyr Project Code Repository on GitHub](https://github.com/zephyrproject-rtos/zephyr) ⭐ 16,233 | 🐛 3,877 | 🌐 C | 📅 2026-08-17 - Primary Git Repository for the Zephyr Project. Zephyr is a new generation, scalable, optimized, secure RTOS for multiple hardware architectures.

Nordic Semiconductor:

* [nRF Connect SDK (sdk-nrf)](https://github.com/nrfconnect/sdk-nrf) ⭐ 1,408 | 🐛 257 | 🌐 C | 📅 2026-08-17 - Main nRF Connect SDK repository (west manifest, subsystems, samples).
* [Nordic Developer Academy / Tutorials](https://github.com/NordicDeveloperAcademy/ncs-fund) ⭐ 114 | 🐛 2 | 🌐 C | 📅 2026-07-30 - self-paced courses and examples (useful to onboard newcomers).
* [Nordic DevZone (Q\&A & Forums)](https://devzone.nordicsemi.com) - official community forum and tech Q\&A (searchable issues, examples, vendor replies).
* [nRF Connect SDK docs / install guide](https://docs.nordicsemi.com/bundle/ncs-latest/page/nrf/installation/install_ncs.html) - official installation & platform-specific setup for NCS.

ZSWatch - Zephyr Smartwatch:

* [jakkra/ZSWatch](https://github.com/jakkra/ZSWatch) ⭐ 82 | 🐛 0 | 🌐 C | 📅 2026-04-22 - ZSWatch the Open Source Zephyr™ based Smartwatch, including both HW and FW.
  * [ZSWatch](https://zswatch.dev/) - Smartwatch built from scratch, both hardware and software. Built on the Zephyr™ Project RTOS, hence the name ZSWatch - Zephyr Smartwatch.

## Quick Start

* [Unified ZMK Config Template](https://github.com/zmkfirmware/unified-zmk-config-template) ⭐ 51 | 🐛 2 | 📅 2025-12-13 - A template for managing multiple boards and shields in a single configuration repository.
* [ZMK Module Template](https://github.com/zmkfirmware/zmk-module-template) ⭐ 7 | 🐛 0 | 📅 2025-02-15 - A template for creating your own external ZMK modules (behaviors, drivers, etc.).
* [Getting Started Guide](https://zmk.dev/docs/user-setup) - The official guide to setting up your `zmk-config` repository.

## Community zmk-config user configurations

* [urob/zmk-config](https://github.com/urob/zmk-config) ⭐ 1,362 | 🐛 2 | 🌐 C++ | 📅 2026-08-14 - Personal ZMK firmware configuration for various boards (34-keys, Corneish Zen, Planck)
* [sunaku/glove80-keymaps](https://github.com/sunaku/glove80-keymaps) ⭐ 759 | 🐛 21 | 🌐 HTML | 📅 2026-03-12 - Glorious Engrammer keymap for Glove80 keyboard
* [manna-harbour/miryoku\_zmk](https://github.com/manna-harbour/miryoku_zmk) ⭐ 646 | 🐛 14 | 🌐 C | 📅 2025-06-27 - Miryoku is an ergonomic, minimal, orthogonal, and universal keyboard layout. Miryoku ZMK is the Miryoku implementation for ZMK.
* [mctechnology17/zmk-config](https://github.com/mctechnology17/zmk-config) ⭐ 317 | 🐛 3 | 🌐 C++ | 📅 2026-01-11 - Quickly and easily configure your Wireless corne - sofle - lily58 keyboard with ZMK
* [eigatech/zmk-config](https://github.com/eigatech/zmk-config) ⭐ 222 | 🐛 1 | 📅 2026-07-02 - ZMK Firmware Configuration
* [aroum/zmk-enki42-dongle](https://github.com/aroum/zmk-enki42-dongle) ⭐ 180 | 🐛 0 | 📅 2025-01-12 - ZMK config for enki42 keyboard with dongle
* [caksoylar/zmk-config](https://github.com/caksoylar/zmk-config) ⭐ 139 | 🐛 0 | 🌐 C | 📅 2026-08-04 - ZMK user config containing keymap for 26-36 key keyboards
* [a741725193/zmk-new\_corne](https://github.com/a741725193/zmk-new_corne) ⭐ 135 | 🐛 2 | 📅 2026-08-01 - ZMK Firmware Configuration
* [kumamuk-git/zmk-config-roBa](https://github.com/kumamuk-git/zmk-config-roBa) ⭐ 77 | 🐛 4 | 📅 2026-04-07 - zmk-config-roBa
* [SethMilliken/zmk-config aka araxia](https://github.com/SethMilliken/zmk-config) ⭐ 63 | 🐛 0 | 📅 2026-08-09 - ZMK Firmware Configuration
* [englmaxi/zmk-config](https://github.com/englmaxi/zmk-config) ⭐ 56 | 🐛 0 | 🌐 C | 📅 2026-05-11 - Personal zmk-config for my ergo keyboards
* [badjeff/zmk-config](https://github.com/badjeff/zmk-config) ⭐ 24 | 🐛 0 | 🌐 C | 📅 2026-08-14 - Personal ZMK firmware configuration for various boards
* [tokyo2006/zmk-config-corne](https://github.com/tokyo2006/zmk-config-corne) ⭐ 16 | 🐛 0 | 🌐 CMake | 📅 2025-12-16 - ZMK Firmware Configuration
* [MickiusMousius/RolioFirmware](https://github.com/MickiusMousius/RolioFirmware) ⭐ 14 | 🐛 1 | 🌐 C | 📅 2026-08-08 - Firmware for the Rolio split wireless keyboard.
* [sadekbaroudi/zmk-fingerpunch-keyboards](https://github.com/sadekbaroudi/zmk-fingerpunch-keyboards) ⭐ 13 | 🐛 2 | 🌐 CMake | 📅 2026-07-05 - The purpose of this repository is to house all the ZMK boards and shields associated with fingerpunch keyboards.
* [a741725193/zmk-corne-oled](https://github.com/a741725193/zmk-corne-oled) ⭐ 7 | 🐛 1 | 📅 2026-06-26 - (Eyelash Peripherals) Corne ZMK Repository with oled screen

### Split Wired

* [paulshir/zmk-board-iris-ce](https://github.com/paulshir/zmk-board-iris-ce.git) ⭐ 6 | 🐛 0 | 🌐 CMake | 📅 2026-01-04 - ZMK board definition for Iris CE by Keebio
* [petejohanson/splitkb-halcyon-zmk-config](https://github.com/petejohanson/splitkb-halcyon-zmk-config) ⭐ 4 | 🐛 0 | 📅 2025-09-24 - Unofficial [splitkb.com Halcyon](https://splitkb.com/products/halcyon-kyria?srsltid=AfmBOoo-Cv2EjX1G1NHV5swo4dR6QqYDoxO30uTHhAOrlnbu1AvAVtPW) ZMK Config
* [petejohanson/splitkb-halcyon-zmk-module](https://github.com/petejohanson/splitkb-halcyon-zmk-module) ⭐ 4 | 🐛 1 | 🌐 CMake | 📅 2025-12-14 - SplitKB Halcyon ZMK Module
* [SSheldon/zmk-keyboard-chiri-ce](https://github.com/SSheldon/zmk-keyboard-chiri-ce) ⭐ 0 | 🐛 0 | 📅 2025-05-19 - [The Chiri CE (Compact Edition)](https://keeb.io/products/chiri-ce-keyboard-kit?srsltid=AfmBOopwnxFWr1kaGPoG6r7je1GEXMA29YCX01t8OEYUgrCqfq4o1ZUD) is just like the Iris CE, but with one less row to make it even more compact, like a Corne!
* [ZMK Documentation Wired Splits](https://zmk.dev/docs/config/split#wired-splits) - **WARNING** Hardware UARTs have a few different modes/approaches to sending and receiving data, with different levels of complexity and performance...
* [ZMK Documentation Wired Splits (Board Pin Control - rp2040)](https://zmk.dev/docs/development/hardware-integration/pinctrl) - **WARNING** The details of pin control can vary from vendor to vendor.

## Community Documentation

* [joric/nrfmicro/wiki](https://github.com/joric/nrfmicro/wiki) ⭐ 1,856 | 🐛 0 | 🌐 HTML | 📅 2025-08-04 - Joric's nRFMicro Wiki, an extensive wiki covering the nRFMicro board, batteries, displays, and ZMK.
* [maksimdrachov/zephyr-rtos-tutorial](https://github.com/maksimdrachov/zephyr-rtos-tutorial) ⭐ 470 | 🐛 10 | 🌐 C | 📅 2024-04-07 - Zephyr: Tutorial for beginners
* [golioth/awesome-zephyr-rtos](https://github.com/golioth/awesome-zephyr-rtos) ⭐ 227 | 🐛 2 | 📅 2024-12-11 - Awesome Zephyr (curated resources), community-curated lists of tools, guides & projects.
* [whoop-t/nice-shield-base](https://github.com/whoop-t/nice-shield-base) ⭐ 31 | 🐛 0 | 🌐 C | 📅 2026-02-14 -  create your own!
* [araxia.net/keyboards](https://araxia.net/keyboards/) - Personal blog with detailed build logs and ZMK insights.
* [Codethetical/reddit.com](https://www.reddit.com/r/ErgoMechKeyboards/comments/15t3o6k/custom_art_on_niceview_displays/) - Custom Art on Nice!View Displays

### Useful Awesome List

* [fffaraz/awesome-cpp](https://github.com/fffaraz/awesome-cpp) ⭐ 72,800 | 🐛 313 | 📅 2026-08-04 - A curated list of awesome C++ (or C) frameworks, libraries, resources, and shiny things.
* [veggiemonk/awesome-docker](https://github.com/veggiemonk/awesome-docker) ⭐ 36,658 | 🐛 26 | 📅 2026-07-29 - A curated list of Docker resources and related projects about the Docker ecosystem.
* [sdras/awesome-actions](https://github.com/sdras/awesome-actions) ⭐ 28,138 | 🐛 259 | 📅 2024-09-01 - A curated list of awesome things related to GitHub Actions.
* [dictcp/awesome-git](https://github.com/dictcp/awesome-git) ⭐ 2,927 | 🐛 66 | 📅 2026-07-07 - A curated list of amazingly awesome Git tools, resources and shiny things.
* [moul/awesome-ssh](https://github.com/moul/awesome-ssh) ⭐ 2,832 | 🐛 46 | 📅 2023-08-10 - A curated list of SSH apps, libraries and resources.
* [dreftymac/awesome-yaml](https://github.com/dreftymac/awesome-yaml) ⭐ 57 | 🐛 3 | 📅 2022-11-14 - A curated collection of YAML tools, templating libraries and related resources.

### Vendor Documentation

* [42keebs](https://42keebs.eu/build-guides/)
* [Bastard Keyboards](https://docs.bastardkb.com/)
* [beekeeb](https://docs.beekeeb.com/)
* [Keebio](https://docs.keeb.io/main)
* [MoErgo (Glove80)](https://docs.moergo.com/layout-editor-guide/)
* [SplitKB](https://docs.splitkb.com/)
* [Typeractive](https://docs.typeractive.xyz/)
* [MBUK - mechboards](https://guides-mechboards.gitbook.io/guides)

## Community firmware Modules and Behaviors

### Custom Behaviors

* [urob/zmk-helpers](https://github.com/urob/zmk-helpers) ⭐ 413 | 🐛 4 | 🌐 C | 📅 2026-05-21 - Convenience macros simplifying ZMK's keymap configuration
* [urob/zmk-auto-layer](https://github.com/urob/zmk-auto-layer) ⭐ 83 | 🐛 3 | 🌐 C | 📅 2026-05-21 - Auto-layer (including num-word) implementation.
* [badjeff/zmk-feature-split-esb](https://github.com/badjeff/zmk-feature-split-esb) ⭐ 54 | 🐛 0 | 🌐 C | 📅 2026-08-11
* [urob/zmk-leader-key](https://github.com/urob/zmk-leader-key) ⭐ 52 | 🐛 5 | 🌐 C | 📅 2026-05-21 - A ZMK module adding a leader-key behavior.
* [zzeneg/zmk-raw-hid](https://github.com/zzeneg/zmk-raw-hid) ⭐ 46 | 🐛 2 | 🌐 C | 📅 2026-05-11 - ZMK module for Raw HID communication
* [urob/zmk-unicode](https://github.com/urob/zmk-unicode) ⭐ 40 | 🐛 5 | 🌐 C | 📅 2026-08-06 - ZMK module for Unicode input
* [englmaxi/zmk-hid-trackball-interface](https://github.com/englmaxi/zmk-hid-trackball-interface) ⭐ 33 | 🐛 1 | 🌐 C | 📅 2024-09-07 - ZMK trackball interface using HID indicators
* [urob/zmk-adaptive-key](https://github.com/urob/zmk-adaptive-key) ⭐ 31 | 🐛 8 | 🌐 C | 📅 2026-05-21 - A ZMK module adding a adaptive-key behavior.
* [ssbb/zmk-listeners](https://github.com/ssbb/zmk-listeners) ⭐ 21 | 🐛 0 | 🌐 C | 📅 2025-12-20- ZMK module to invoke behaviors on certain events.
* [dhruvinsh/zmk-tri-state](https://github.com/dhruvinsh/zmk-tri-state) ⭐ 20 | 🐛 4 | 🌐 C | 📅 2025-03-16 - Tri-state (swapper) implementation.
* [ssbb/zmk-antecedent-morph](https://github.com/ssbb/zmk-antecedent-morph) ⭐ 19 | 🐛 0 | 🌐 C | 📅 2024-12-11 - ZMK Antecedent Morph Behavior aka Adaptive Keys.
* [badjeff/zmk-split-peripheral-input-relay](https://github.com/badjeff/zmk-split-peripheral-input-relay) ⚠️ Archived - This would allow, for example, sending trackpoint events from the peripheral to the center split.
* [badjeff/zmk-hid-io](https://github.com/badjeff/zmk-hid-io) ⭐ 15 | 🐛 1 | 🌐 C | 📅 2026-03-08 - This module add new HID Usage Page for ZMK.
* [elpekenin/zmk-userspace](https://github.com/elpekenin/zmk-userspace) ⭐ 14 | 🐛 0 | 🌐 C | 📅 2026-07-07 - "tiny" and "useful" bits to reuse across ZMK boards
* [badjeff/zmk-output-behavior-listener](https://github.com/badjeff/zmk-output-behavior-listener) ⭐ 12 | 🐛 0 | 🌐 C | 📅 2025-09-02 - It allows to config a feedback of state change event by binding behaviors to feedback devices, such as, eccentric rotating mass (ERM) motors, Linear Resonant Actuator (LRA) vibration motors, LED indicators, serve motors, motorized fader, etc.
* [george-norton/zmk-behavior-sensor-attr-cycle](https://github.com/george-norton/zmk-behavior-sensor-attr-cycle) ⭐ 11 | 🐛 0 | 🌐 C | 📅 2026-04-05 - A ZMK behaviour for cycling sensor attributes
* [badjeff/zmk-behavior-insomnia](https://github.com/badjeff/zmk-behavior-insomnia/) ⭐ 10 | 🐛 0 | 🌐 C | 📅 2026-03-08 - Insomnia Behavior for ZMK. This module prevents the board from entering sleep mode if BLE is connected, useful for multi-peripheral setups to avoid continuous BLE advertisement scanning.
* [dhruvinsh/zmk-num-word](https://github.com/dhruvinsh/zmk-num-word) ⭐ 7 | 🐛 0 | 🌐 C | 📅 2024-08-06 - Num-word implementation.
* [badjeff/zmk-split-peripheral-output-relay](https://github.com/badjeff/zmk-split-peripheral-output-relay) ⭐ 5 | 🐛 0 | 🌐 C | 📅 2024-08-14 - This is a [ZMK](https://zmk.dev) *Split Transport* module adding support for [Enhanced ShockBurst (ESB)](https://docs.nordicsemi.com/bundle/ncs-latest/page/nrf/protocols/esb/index.html) protocol on Nordic nRF5 Series device.
* [badjeff/zmk-input-processor-xyz](https://github.com/badjeff/zmk-input-processor-xyz) ⭐ 5 | 🐛 0 | 🌐 C | 📅 2026-08-14 - This module is used to quantize X and Y value set to fit inside single payload of pointing device on split peripheral, to reduce the bluetooth connection loading between the peripherals and the central.
* [badjeff/zmk-split-peripheral-bonding-tweak](https://github.com/badjeff/zmk-split-peripheral-bonding-tweak) ⭐ 3 | 🐛 0 | 🌐 C | 📅 2025-11-22 - This an experimental of an experimental module that grant ability to a split central and peripherals to bond on top of a forgettable bluetooth pairing. Two add-on feature are designed to serve this purpose on ZMK.
* [badjeff/zmk-split-peripheral-bonding-tweak](https://github.com/badjeff/zmk-split-peripheral-bonding-tweak) ⭐ 3 | 🐛 0 | 🌐 C | 📅 2025-11-22 - This an experimental of an experimental module that grant ability to a split central and peripherals to bond on top of a forgettable bluetooth pairing.
* [badjeff/zmk-behavior-battery-percentage-printer](https://github.com/badjeff/zmk-behavior-battery-percentage-printer) ⭐ 3 | 🐛 0 | 🌐 C | 📅 2025-11-17 - This is a modified version of [alan0ford's behavior\_battery\_printer.c](https://github.com/alan0ford/zmk-lplancks/blob/GHPilotBatt/boards/shields/lplancks/behavior_battery_printer.c) ⭐ 1 | 🐛 0 | 📅 2026-01-19. Changes has been added to make the behavior awaring of peripheral id.
* [ssbb/zmk-deadkey-slayer](https://github.com/ssbb/zmk-deadkey-slayer) ⭐ 3 | 🐛 0 | 🌐 C | 📅 2025-01-11 - A ZMK module to drop illegal keycodes.
* [badjeff/zmk-input-processor-mixer](https://github.com/badjeff/zmk-input-processor-mixer) ⭐ 2 | 🐛 0 | 🌐 C | 📅 2025-09-06 - This module interrupt, combine, sync incoming input events from Zephyr input subsystem for ZMK.
* [badjeff/zmk-behavior-key-press-lip](https://github.com/badjeff/zmk-behavior-key-press-lip) ⭐ 2 | 🐛 0 | 🌐 C | 📅 2025-05-28 - Implementation of [Last Input Priority](https://www.hitboxarcade.com/blogs/support/what-is-socd) key press favor for ZMK.
* [a741725193/zmk-tog-io](https://github.com/a741725193/zmk-tog-io) ⭐ 0 | 🐛 0 | 🌐 C | 📅 2025-07-23 - simple behavior that toggles io on falling and rising edge of the keyswitch press
* [ZMK Behaviors Documentation](https://zmk.dev/docs/keymaps/behaviors) - Official documentation on how behaviors work.

### Drivers

#### Drivers Trackpad

* [AYM1607/zmk-driver-azoteq-iqs5xx](https://github.com/AYM1607/zmk-driver-azoteq-iqs5xx) ⭐ 72 | 🐛 1 | 🌐 C | 📅 2025-12-31 - ZMK driver for Azoteq IQS5XX trackpads
* [petejohanson/cirque-input-module](https://github.com/petejohanson/cirque-input-module) ⭐ 51 | 🐛 7 | 🌐 C | 📅 2025-02-18 - Zephyr module for the Cirque Pinnacle input driver.
* [sekigon-gonnoc/iqs7211e-trackpad-module](https://github.com/sekigon-gonnoc/iqs7211e-trackpad-module) ⭐ 7 | 🐛 0 | 🌐 C | 📅 2025-12-02 - iQS7211E sensor driver with 30 mm diameter trackpad, low consumption (\~ 1.5 mA) and admits multitactile (two points).
* [Ahmed-M-Osman1/zmk-driver-azoteq](https://github.com/Ahmed-M-Osman1/zmk-driver-azoteq) ⭐ 6 | 🐛 0 | 🌐 C | 📅 2026-02-08 - ZMK driver for Azoteq IQS5XX trackpads
* [ZitaoTech/zmk-config-9981-pro](https://github.com/ZitaoTech/zmk-config-9981-pro/tree/main) ⭐ 4 | 🐛 2 | 🌐 C | 📅 2025-12-12 - zmk firmware config for 9981 keyboard with trackpad(pro version)
  * [HackberryPi-4B example](https://github.com/ZitaoTech/HackberryPi-4B) ⭐ 70 | 🐛 0 | 🌐 DataWeave | 📅 2025-02-12 - A handheld Linux device using Raspberry Pi4B as Core with 4" 720X720 TFT Touch display
  * [Full Guide](https://github.com/ZitaoTech/9981_BLE_USB_Keyboard_Pro/tree/main) ⭐ 26 | 🐛 1 | 🌐 C | 📅 2026-05-03 - The fully open-sourced P9981 BLE\&USB Keyboard is the smallest ZMK-powered keyboard mouse combo and features n-Key rollover that other original blackberry keyboards don't have!
  * [zmk fork](https://github.com/ZitaoTech/zmk/tree/bbkeyboard_tp/app/module/drivers/sensor/a320) ⭐ 6 | 🐛 0 | 🌐 C | 📅 2025-07-02

#### Drivers Trackball

* [badjeff/zmk-pmw3610-driver](https://github.com/badjeff/zmk-pmw3610-driver) ⭐ 129 | 🐛 5 | 🌐 C | 📅 2026-04-16 - PMW3610 sensor driver.
* [inorichi/zmk-pmw3610-driver](https://github.com/inorichi/zmk-pmw3610-driver) ⭐ 95 | 🐛 3 | 🌐 C | 📅 2024-05-02 - PMW3610 sensor driver.
* [badjeff/zmk-paw3395-driver](https://github.com/badjeff/zmk-paw3395-driver) ⭐ 30 | 🐛 0 | 🌐 C | 📅 2026-06-18 - This is an ZMK pointer input module, that grant ability to call a non-disclosed PAW3395 driver library.
  * [badjeff/paw3395-pcb](https://github.com/badjeff/paw3395-pcb) ⭐ 32 | 🐛 0 | 📅 2026-06-18 - PixArt PAW3395DM-T6QU low power laser mouse sensor breakout board.
* [sekigon-gonnoc/zmk-driver-paw3222](https://github.com/sekigon-gonnoc/zmk-driver-paw3222) ⭐ 9 | 🐛 0 | 🌐 C | 📅 2026-02-23 - This driver enables the use of the PIXART PAW3222 optical sensor with the ZMK framework.
* [george-norton/zmk-driver-pmw3360](https://github.com/george-norton/zmk-driver-pmw3360) ⭐ 9 | 🐛 0 | 🌐 C | 📅 2025-10-14 - A ZMK driver for the Pixart PMW3360 optical mouse sensor
* [kzyz/zmk-az1uball-driver](https://github.com/kzyz/zmk-az1uball-driver.git) ⭐ 5 | 🐛 0 | 🌐 C | 📅 2026-05-16 - A 16x16mm I2C trackball module 5,3mm (0x0A) compatible with 3.3V/5V, consuming \~8mA, offering PIM447 data/power compatibility with higher precision and 50% less power (non-illuminated), detailed on GitHub at [palette-system/az1uball](https://github.com/palette-system/az1uball) ⭐ 49 | 🐛 0 | 🌐 C++ | 📅 2026-08-01
  * [kzyz/corne-ulp-ball](https://github.com/kzyz/corne-ulp-ball.git) ⭐ 0 | 🐛 0 | 📅 2026-05-08 - example with a xiao MCU + zmk 0.3
  * [buy a AZ1UBALL on booth (japan)](https://booth.pm/ja/items/4202085?srsltid=AfmBOorsZkPYZq80An_3UKa-HHpciWQeS2lXHikH4J_Y13bmAngWI2rI)
* [t0bybr/pim447](https://github.com/t0bybr/pim447) ⭐ 5 | 🐛 0 | 🌐 C | 📅 2026-06-17 - Pimoroni PIM447 trackball driver
  * [Pimoroni PIM447 trackball driver use docs](https://github.com/cdc-mkb/zmk/commit/eb8889883d1e91f58a42f0babc17a10fa3fa1b4a) ⭐ 23 | 🐛 0 | 📅 2021-11-29
  * [t0bybr/zmk-config-kailhx](https://github.com/t0bybr/zmk-config-kailhx)

#### Drivers Trackpoint

* [infused-kim/zmk-ps2-mouse-trackpoint-driver](https://github.com/infused-kim/kb_zmk_ps2_mouse_trackpoint_driver) ⭐ 236 | 🐛 11 | 🌐 C | 📅 2024-08-18 - PS/2 trackpoint driver.
* [badjeff/kb\_zmk\_ps2\_mouse\_trackpoint\_driver](https://github.com/badjeff/kb_zmk_ps2_mouse_trackpoint_driver) ⭐ 7 | 🐛 0 | 🌐 C | 📅 2026-06-05 - PS/2 trackpoint driver fork updated for mainline ZMK.

#### Drivers Analog Joystick

* [badjeff/zmk-analog-input-driver](https://github.com/badjeff/zmk-analog-input-driver) ⭐ 47 | 🐛 0 | 🌐 C | 📅 2026-04-06 - This driver groups ADC io channels into single input event for input subsystem.
* [letmegobacktosleep/zmk-keyboard-joystick-wasd](https://github.com/letmegobacktosleep/zmk-keyboard-joystick-wasd) ⭐ 1 | 🐛 1 | 🌐 C | 📅 2026-05-14 - An attempt at making a joystick act as a four-directional switch, in a keyboard.

#### Drivers Haptic

* [badjeff/zmk-drv2605-driver](https://github.com/badjeff/zmk-drv2605-driver/) ⭐ 6 | 🐛 0 | 🌐 C | 📅 2024-09-21 - DRV2605 haptic feedback driver.

#### Drivers Display

* [mctechnology17/zmk-oled-adapter](https://github.com/mctechnology17/zmk-oled-adapter) ⭐ 24 | 🐛 0 | 🌐 C | 📅 2025-11-09 - use different OLED screen sizes without modifying code (for 128x32, 128x64 and 128x128 OLED screens)
* [MickiusMousius/zmk-ls0xxvcom-driver](https://github.com/MickiusMousius/zmk-ls0xxvcom-driver) ⭐ 2 | 🐛 0 | 🌐 C | 📅 2026-08-17 - Zephyr driver for LS0XX displays with the VCOM fix applied

#### Drivers LEDS Backlight Underglow

> \[!NOTE]
> [elpekenin/zmk-userspace](https://github.com/elpekenin/zmk-userspace) ⭐ 14 | 🐛 0 | 🌐 C | 📅 2026-07-07 These drivers can be easily located here and not only in behaviors

* [caksoylar/zmk-rgbled-widget](https://github.com/caksoylar/zmk-rgbled-widget) ⭐ 231 | 🐛 0 | 🌐 C | 📅 2026-07-09 - A ZMK module to add battery & BT indicators using an RGB LED (like in Xiao BLEs).
* [englmaxi/zmk-config](https://github.com/englmaxi/zmk-config/tree/main/boards/shields/led_indicator) ⭐ 56 | 🐛 0 | 🌐 C | 📅 2026-05-11 - single LED indicator widget based on [caksoylar/zmk-rgbled-widget](https://github.com/caksoylar/zmk-rgbled-widget) ⭐ 231 | 🐛 0 | 🌐 C | 📅 2026-07-09
* [sekigon-gonnoc/zmk-feature-status-led](https://github.com/sekigon-gonnoc/zmk-feature-status-led) ⭐ 12 | 🐛 0 | 🌐 C | 📅 2026-07-22 - This module provides LED status indicators for ZMK keyboards using gpio-leds.
* [aroum/zmk-kabarga](https://github.com/aroum/zmk-kabarga) ⭐ 7 | 🐛 0 | 🌐 C | 📅 2026-03-31 - This project features the implementation of an LED status indicator. A similar indicator approach is utilized across many of my other projects (fEnki, mEnki, gbEnki, yolochka, etc.).
* [dhruvinsh/zmk-config](https://github.com/dhruvinsh/zmk-config/tree/legacy) ⭐ 4 | 🐛 0 | 🌐 Shell | 📅 2026-07-23 - **legacy branch** This repository tracks my keyboard configuration.
* [4mplelab/zmk-feature-charge-indicator](https://github.com/4mplelab/zmk-feature-charge-indicator) ⭐ 4 | 🐛 0 | 🌐 C | 📅 2026-01-24 - A ZMK feature module to indicate battery charging status on an RGB LED, designed to coexist with the `rgbled_widget`
* [joelspadin/zmk-keyboards](https://github.com/joelspadin/zmk-keyboards) ⭐ 1 | 🐛 0 | 🌐 C | 📅 2025-11-28 - marten\_numpad and indicator LEDs driver

#### Drivers Others

* [petejohanson/ec-support-zmk-module](https://github.com/petejohanson/ec-support-zmk-module) ⭐ 15 | 🐛 0 | 🌐 C | 📅 2025-06-16 - Electrostatic Capacitive (Topre) matrix scan implementation.
* [sekigon-gonnoc/zmk-feature-non-lipo-battery-management](https://github.com/sekigon-gonnoc/zmk-feature-non-lipo-battery-management) ⭐ 5 | 🐛 0 | 🌐 C | 📅 2026-08-14 - This module provides battery management functionality for non-LiPo batteries (such as alkaline or NiMH) in ZMK keyboards. It includes voltage monitoring, battery percentage calculation, and power management features.
* [badjeff/zmk-adns9800-driver](https://github.com/badjeff/zmk-adns9800-driver) ⭐ 4 | 🐛 0 | 🌐 C | 📅 2026-04-16 - ADNS9800 sensor driver.
* [george-norton/zmk-driver-rp2040-sleep](https://github.com/george-norton/zmk-driver-rp2040-sleep) ⭐ 1 | 🐛 0 | 🌐 C | 📅 2025-10-14 - ZMK driver to setup the RP2040 sleep mode
* [badjeff/zmk-tb6612fng-driver](https://github.com/badjeff/zmk-tb6612fng-driver) ⭐ 0 | 🐛 0 | 🌐 C | 📅 2024-09-15 - This module exposes TB6612FNG inputs via Zephyr's sensor\_driver\_api and key press behavior.
* [badjeff/zmk-drv883x-driver](https://github.com/badjeff/zmk-drv883x-driver) ⭐ 0 | 🐛 0 | 🌐 C | 📅 2024-08-27 - This module exposes DRV883x inputs via Zephyr's sensor\_driver\_api and key press behavior.

### Display Modules

* [mctechnology17/zmk-nice-oled](https://github.com/mctechnology17/zmk-nice-oled) ⭐ 488 | 🐛 9 | 🌐 C | 📅 2026-01-26 - vertical widgets for oled and niceview screens using zmk (for split and non-split keyboards)
* [M165437/nice-view-gem](https://github.com/M165437/nice-view-gem) ⭐ 385 | 🐛 3 | 🌐 C | 📅 2026-02-27 - A sleek customization for the nice!view shield
* [GPeye/urchin-peripheral-animation](https://github.com/GPeye/urchin-peripheral-animation) ⭐ 163 | 🐛 1 | 🌐 C | 📅 2024-09-13 - Urchin Peripheral Animation
* [GPeye/hammerbeam-slideshow](https://github.com/GPeye/hammerbeam-slideshow) ⭐ 104 | 🐛 3 | 🌐 C | 📅 2024-09-14 - A zmk module to implement a slideshow of 30 of Hammerbeam's 1 bit art on the peripheral (right) nice!view display.
* [infely/nice-view-battery](https://github.com/infely/nice-view-battery) ⭐ 100 | 🐛 2 | 🌐 C | 📅 2024-10-27 - A clean customization for the nice!view displays
* [kevinpastor/nice-view-elemental](https://github.com/kevinpastor/nice-view-elemental) ⭐ 90 | 🐛 2 | 🌐 C | 📅 2026-06-05 - A bold while minimalistic interface for your keyboard's display
* [dsifry/nice-view-mod](https://github.com/dsifry/nice-view-mod) ⭐ 38 | 🐛 0 | 🌐 C | 📅 2025-03-31 - A copy of the nice!view shield from the official ZMK repo as a ZMK module for the purposes of easily customizing
* [mctechnology17/zmk-dongle-display-view](https://github.com/mctechnology17/zmk-dongle-display-view) ⭐ 37 | 🐛 0 | 🌐 C | 📅 2024-08-25 - horizontal widgets for keyboards with dongles, splits and non-splits using the nice!view (bongocat, wpm, caps, batt, etc.)
* [zzeneg/zmk-nice-view-hid](https://github.com/zzeneg/zmk-nice-view-hid) ⭐ 19 | 🐛 0 | 🌐 C | 📅 2026-05-29 - ZMK module for nice!view widget with Raw HID functionality
* [GPeye/mario-peripheral-animation](https://github.com/GPeye/mario-peripheral-animation) ⭐ 18 | 🐛 0 | 🌐 C | 📅 2024-09-02 - Urchin Peripheral Animation
* [MickiusMousius/RolioFirmware (for Vista508)](https://github.com/MickiusMousius/RolioFirmware) ⭐ 14 | 🐛 1 | 🌐 C | 📅 2026-08-08 - The Vista508 is a low-power, high refresh rate display meant to replace I2C OLEDs traditionally used.
* [whoop-t/nice-adventure-time](https://github.com/whoop-t/nice-adventure-time) ⭐ 14 | 🐛 0 | 🌐 C | 📅 2025-03-07 - adventure time
* [Ziembski/nice-view-press-start](https://github.com/Ziembski/nice-view-press-start) ⭐ 12 | 🐛 1 | 🌐 C | 📅 2025-08-22 - Custom shield for nice!view with retro feeling
* [whoop-t/nice-one-punch-ok](https://github.com/whoop-t/nice-one-punch-ok) ⭐ 11 | 🐛 0 | 🌐 C | 📅 2026-01-25 - one punch
* [whoop-t/nice-fry-button-miss](https://github.com/whoop-t/nice-fry-button-miss) ⭐ 5 | 🐛 0 | 🌐 C | 📅 2025-03-08 - futurama fry
* [whoop-t/nice-luffy-wanted](https://github.com/whoop-t/nice-luffy-wanted) ⭐ 5 | 🐛 0 | 🌐 C | 📅 2025-03-10 - luffy
* [whoop-t/nice-futurama-sus](https://github.com/whoop-t/nice-futurama-sus) ⭐ 4 | 🐛 0 | 🌐 C | 📅 2025-03-08 - futurama
* [Jestar342/nice-view-spacemarine](https://github.com/Jestar342/nice-view-spacemarine) ⭐ 2 | 🐛 0 | 🌐 C | 📅 2025-04-21 - This is a base repo to help anyone get started creating their own images/animations for their nice!view.
* [whoop-t/nice-luffy-gear-five](https://github.com/whoop-t/nice-luffy-gear-five) ⭐ 0 | 🐛 0 | 🌐 C | 📅 2025-03-12 - luffy gear five

#### Dongles Modules

> NOTE
> ZMK Supports Dongle scheme for 3 controllers (host + 2 halves). It's a little bit more battery friendly (up to a month on a 100 mAh) than a battery-powered BT host (up to 7 days) [^7].

* [englmaxi/zmk-dongle-display](https://github.com/englmaxi/zmk-dongle-display) ⭐ 262 | 🐛 5 | 🌐 C | 📅 2026-02-21 - Custom status screen for zmk dongles
* [janpfischer/zmk-dongle-screen](https://github.com/janpfischer/zmk-dongle-screen.git) ⭐ 255 | 🐛 7 | 🌐 C | 📅 2026-03-19 - YADS - Yet another Dongle Screen for ZMK
* [carrefinho/prospector-zmk-module](https://github.com/carrefinho/prospector-zmk-module) ⭐ 165 | 🐛 11 | 🌐 C | 📅 2026-02-17 - ZMK module for the Prospector dongle
* [mctechnology17/zmk-dongle-display-view](https://github.com/mctechnology17/zmk-dongle-display-view) ⭐ 37 | 🐛 0 | 🌐 C | 📅 2024-08-25 - horizontal widgets for keyboards with dongles, splits and non-splits using the nice!view (bongocat, wpm, caps, batt, etc.)
* [rschenk/zmk-component-raytac-dongle](https://github.com/rschenk/zmk-component-raytac-dongle) ⭐ 34 | 🐛 1 | 🌐 CMake | 📅 2026-04-12 - ZMK module to support the Raytac MDBT50Q-RX USB key as a dongle
  * [Please read the section "Caveat: Buy One With A UF2 Bootloader Installed"](https://github.com/rschenk/zmk-component-raytac-dongle?tab=readme-ov-file#caveat-buy-one-with-auf2-bootloader-installed) ⭐ 34 | 🐛 1 | 🌐 CMake | 📅 2026-04-12
* [victorlucachi/charybdis-zmk-module](https://github.com/victorlucachi/charybdis-zmk-module) ⭐ 32 | 🐛 1 | 📅 2025-12-03 - zmk module for bkb charybdis mini/nano with pmw3610 and xiao/nicenano dongle
* [t-ogura/prospector-zmk-module](https://github.com/t-ogura/prospector-zmk-module) ⭐ 10 | 🐛 0 | 🌐 C | 📅 2026-08-01 - Keyboard broadcasts status via BLE Advertisement (observer mode)
  * [t-ogura/zmk-config-prospector](https://github.com/t-ogura/zmk-config-prospector) ⭐ 64 | 🐛 2 | 📅 2026-08-01 - Prospector only listens - does NOT connect to keyboard
* [joaopedropio/snake-module](https://github.com/joaopedropio/snake-module.git) ⭐ 2 | 🐛 2 | 🌐 C | 📅 2026-03-11 - Snake Dongle Shell 🐍
* [dhruvinsh/zmk-prospector](https://github.com/dhruvinsh/zmk-prospector) ⭐ 0 | 🐛 0 | 🌐 C | 📅 2025-04-28 - Prospector but for ST7735S display

##### Dongles Design

* [carrefinho/prospector](https://github.com/carrefinho/prospector) ⭐ 786 | 🐛 11 | 📅 2025-11-22 - Desktop ZMK Dongle with color 1.69-inch IPS LCD screen with curved cover glass screen
* [rafaelromao/keyboards](https://github.com/rafaelromao/keyboards/tree/main/stls/Dongle) ⭐ 492 | 🐛 0 | 🌐 Shell | 📅 2026-05-08 - Cyberdeck
* [rafaelromao/keyboards](https://github.com/rafaelromao/keyboards/tree/main/src/keyboards/bastardkb/dilemma/boards/shields/dilemma) ⭐ 492 | 🐛 0 | 🌐 Shell | 📅 2026-05-08 - Dilemma DIY with 128x32 OLED
* [englmaxi/zmk-dongle-display 1](https://github.com/englmaxi/zmk-dongle-display/tree/main/cases) ⭐ 262 | 🐛 5 | 🌐 C | 📅 2026-02-21 - case1
* [englmaxi/zmk-dongle-display 2](https://github.com/englmaxi/zmk-dongle-display/tree/main/cases) ⭐ 262 | 🐛 5 | 🌐 C | 📅 2026-02-21 - case2
* [rain2813/zmk-cygnus-oled](https://github.com/rain2813/zmk-cygnus-oled) ⭐ 60 | 🐛 0 | 🌐 C | 📅 2024-07-22 - This is keymap configuration for redox zmk firmware, 1.3-inch I2C OLED display
* [joaopedropio/snake-dongle](https://github.com/joaopedropio/snake-dongle.git) ⭐ 47 | 🐛 1 | 📅 2026-03-06 - Snake Dongle is a compact, highly customizable ZMK-powered dongle that features a Snake‑game-style animation and optional sound effects.
  * [joaopedropio/snake-dongle-shell](https://github.com/joaopedropio/snake-dongle-shell.git) ⭐ 0 | 🐛 0 | 📅 2025-10-23 - Snake Dongle Shell 🐍
* [dohn-joh/dongle-zmk](https://github.com/dohn-joh/dongle-zmk) ⭐ 27 | 🐛 0 | 🌐 JavaScript | 📅 2024-11-09 - Dongle ZMK
* [leafflat/sai44](https://github.com/leafflat/sai44/tree/main/STL/Dongle) ⭐ 19 | 🐛 0 | 🌐 C | 📅 2025-08-01 - sai44 Dongle
* [spe2/zmk\_dongle\_hardware](https://github.com/spe2/zmk_dongle_hardware) ⭐ 14 | 🐛 0 | 📅 2024-03-01 - Dongle PCB
* [tokyo2006/prospector-zmk-module/support\_nicenano](https://github.com/tokyo2006/prospector-zmk-module/blob/support_nicenano/stl/Back.stl) ⭐ 11 | 🐛 0 | 🌐 C | 📅 2026-02-17 - Desktop ZMK Dongle with color 1.69-inch IPS LCD screen with curved cover glass screen
* [rain2813/makerworld.com](https://makerworld.com/en/models/403660) - Macintosh
* [rurounikexin/makerworld.com](https://makerworld.com/en/models/242951) - Redox
* [yingeling/makerworld.com](https://makerworld.com/en/models/496738) - ZMK Display Dongle
* [James\_909973/printables.com](https://www.printables.com/model/1207682-zmk-nice-nano-128x64-oled-dongle) - ZMK Nice Nano 128x64 OLED Dongle

##### Dongle Prospector Vendor

* [keycapsss.com/Prospector Kit - ZMK dongle with full color LCD screen (standard)](https://keycapsss.com/Prospector-Kit-ZMK-dongle-with-full-color-LCD-screen/KC10254-STD) - The Prospector is a customisable status screen designed for wireless ZMK-based keyboards. It features a full-colour LCD screen and an ambient light sensor (not Eco variant).
* [keycapsss.com/Prospector Kit - ZMK dongle with full color LCD screen (ECO)](https://keycapsss.com/Prospector-Kit-ZMK-dongle-with-full-color-LCD-screen/KC10254-ECO) - NO Adafruit APDS9960 (Proximity, Light, RGB, and Gesture Sensor)
* [beekeeb.com/Pre-soldered Prospector - ZMK Dongle](https://shop.beekeeb.com/products/pre-soldered-prospector-zmk-dongle?variant=52494461600051) - NO Adafruit APDS9960 (Proximity, Light, RGB, and Gesture Sensor)
* [beekeeb.com/ZMK Dongle - Prospector DIY Kit](https://shop.beekeeb.com/products/zmk-wireless-dongle-prospector-diy-kit) - NO Adafruit APDS9960 (Proximity, Light, RGB, and Gesture Sensor)
* [ergohaven.xyz/Ergohaven's Qube](https://ergohaven.xyz/shop/tproduct/767895441-375223366762-ergohavens-qube) - This universal device is designed to be an essential companion for wireless keyboards. It works as a dongle and displays useful information and reduces your keyboard's energy consumption

#### Display Modules Hardware

* [OLED Display 128x32](https://keycapsss.com/0.91-OLED-LCD-Display-128x32-SSD1306-I2C/KC10048-BL) - 0.91 OLED LCD Display 128x32 SSD1306 I2C
* [OLED Display 128x64](https://keycapsss.com/0.96-OLED-LCD-Display-128x64-SSD1306-I2C/KC10129-BL) - 0.96 OLED LCD Display 128x64 SSD1306 I2C
* [nice!view](https://nicekeyboards.com/docs/nice-view/) - A sharp, low-power E-Ink display designed to be easily added to a nice!nano. SHARP MiP DISPLAYS, cutting edge Memory-in-Pixel technology - 30Hz at minmal power draw.
* [VISTA508 Low Power Display](https://keydio.shop/products/vista508-low-power-display) - The Vista508 is a MIPS display with excellent power consumption characteristics that is pin compatible with the very popular nice!view display.
* [Vista272 Low Power Display](https://keydio.shop/products/vista272) - The Vista272 is a drop in replacement for the nice!view display, it uses the exact same MIPS display module.
* [Halcyon TFT LCD Display](https://splitkb.com/products/halcyon-tft-lcd-display-module?_pos=2&_sid=89f88ba1c&_ss=r) - The Halcyon TFT LCD Display Module provides your Halcyon keyboard with a responsive and vibrant colour display

## Tools and Software

### Keymap Editors GUI

* [ZMK Studio (Offline via BLE)](https://github.com/zmkfirmware/zmk-studio/releases) ⭐ 312 | 🐛 58 | 🌐 TypeScript | 📅 2026-07-02 - A desktop application that allows you to modify your keymap offline via Bluetooth.
* [MrMarble/zmk-viewer](https://github.com/MrMarble/zmk-viewer) ⭐ 178 | 🐛 8 | 🌐 Go | 📅 2024-06-26 - cli tool to generate preview images from a zmk .keymap file
* [joelspadin/zmk-locale-generator](https://github.com/joelspadin/zmk-locale-generator) ⭐ 105 | 🐛 3 | 🌐 Python | 📅 2025-03-09 - Python module to generate localized keyboard layout headers for ZMK Firmware.
* [efogdev/zmk-keymap-shell](https://github.com/efogdev/zmk-keymap-shell) ⭐ 9 | 🐛 0 | 🌐 C | 📅 2026-07-01 - Shell commands and behaviors (ToDo) for managing multiple keymap profiles on ZMK keyboards.
* [ZMK Studio - Official GUI Support (Online via USB)](https://zmk.studio/) - ZMK Studio provides runtime update functionality to ZMK powered devices, allowing users to change their keymap layers without flashing new firmware to their keyboards.
* [nickcoutsos/keymap-editor](https://nickcoutsos.github.io/keymap-editor/) - A web based graphical editor of ZMK keymaps.
  * [nickcoutsos/keymap-editor](https://github.com/nickcoutsos/keymap-editor) ⭐ 2,062 | 🐛 64 | 🌐 JavaScript | 📅 2025-10-10 -  source code on GitHub
  * [nickcoutsos/keymap-editor/wiki](https://github.com/nickcoutsos/keymap-editor/wiki) ⭐ 2,062 | 🐛 64 | 🌐 JavaScript | 📅 2025-10-10 - keymap-editor wiki!
* [caksoylar/keymap-drawer](https://keymap-drawer.streamlit.app/) - Visualize keymaps that use advanced features like hold-taps and combos, with automatic parsing.
  * [caksoylar/keymap-drawer](https://github.com/caksoylar/keymap-drawer) ⭐ 1,313 | 🐛 27 | 🌐 Python | 📅 2026-08-12 - source code on GitHub
* [ZMK Firmware official hardware-integration/physical-layouts](https://zmk.dev/docs/development/hardware-integration/physical-layouts) - Physical Layouts
  * [zmk-physical-layout-converter by caksoylar](https://zmk-physical-layout-converter.streamlit.app/) - Web app for converting between physical layout formats for ZMK Studio [^11].
    * [caksoylar/zmk-physical-layout-converter](https://github.com/caksoylar/zmk-physical-layout-converter) ⭐ 13 | 🐛 0 | 🌐 Python | 📅 2025-12-09 - source code on GitHub
  * [keymap-layout-tools by nickcoutsos](https://nickcoutsos.github.io/keymap-layout-tools/) - Helper code for dealing with rendering keyboard layouts. [^11].
    * [nickcoutsos/keymap-layout-tools](https://github.com/nickcoutsos/keymap-layout-tools) ⭐ 38 | 🐛 3 | 🌐 JavaScript | 📅 2026-03-14 - source code on GitHub
* [An experimental tool to create ZMK shields by Genteure](https://shield-wizard.genteure.workers.dev) - A web-based tool to create ZMK configurations for custom keyboards.

### Power Estimation

* [kot149/zmk-battery-center](https://github.com/kot149/zmk-battery-center) ⭐ 180 | 🐛 5 | 🌐 TypeScript | 📅 2026-08-07 - A system tray app to monitor the battery level of ZMK-based keyboards for MacOS/Windows
* [Maksim-Isakau/zmk-split-battery](https://github.com/Maksim-Isakau/zmk-split-battery) ⭐ 105 | 🐛 3 | 🌐 C# | 📅 2025-08-05 ZMK Split Battery Status in system tray for Windows
* [codyd51/Mighty-Mitts](https://github.com/codyd51/Mighty-Mitts) ⭐ 78 | 🐛 5 | 🌐 Objective-C | 📅 2024-06-14 - macOS menu bar applet for battery levels of ZMK split keyboards
* [mh4x0f/zmkBATx](https://github.com/mh4x0f/zmkBATx) ⭐ 56 | 🐛 0 | 🌐 C++ | 📅 2025-01-03 - Opensource tool for peripheral battery monitoring zmk split keyboard over BLE for linux
* [JanValiska/ZmkBatteryClient](https://github.com/JanValiska/ZmkBatteryClient) ⭐ 8 | 🐛 0 | 🌐 Rust | 📅 2025-12-16 - Waybar custom module for ZMK powered keyboards
* [ZMK Power Profiler](https://zmk.dev/power-profiler) - An online tool to estimate your keyboard's power usage and battery life based on its components
* [Online Power Profiler for BLE](https://devzone.nordicsemi.com/power/w/opp/2/online-power-profiler-for-bluetooth-le) - The tool is based on a model of measured values, and is not showing the actual measurement [^5].

### Display Utilities

* [LVGL Image Converter](https://lvgl.io/tools/imageconverter) - Convert BMP, JPG, PNG or SVG files to C arrays (or various binary formats) for use with LVGL.
* [javl/image2cpp](https://javl.github.io/image2cpp/) - image2cpp is a simple tool to change images into byte arrays (or arrays back into images) for use with (monochrome) displays such as OLEDs on your Arduino or Raspberry Pi.
* [joric/qle (QMK Logo Editor)](https://joric.github.io/qle/) - QMK Logo Editor is a lightweight web editor for creating and exporting small monochrome logos / glyphs for keyboard OLEDs.
* [notisrac/FileToCArray](https://notisrac.github.io/FileToCArray/) - Coverts any file to a C style array. (It can also do image color format and size coversion)

### RAW HID Host

* [zzeneg/qmk-hid-host](https://github.com/zzeneg/qmk-hid-host) ⭐ 76 | 🐛 2 | 🌐 Rust | 📅 2026-06-29 - ZMK and QMK HID Host. Host component for communicating with ZMK and QMK keyboards using Raw HID feature.
* [badjeff/zmk-companion-macos](https://github.com/badjeff/zmk-companion-macos) ⭐ 3 | 🐛 0 | 🌐 Swift | 📅 2024-12-31 - ZMK Companion. A main menu macOS application communicate to ZMK powered HID device.

### CLI and Utilities

* [aroum/cn\_tester](https://github.com/aroum/cn_tester) ⭐ 35 | 🐛 0 | 🌐 Python | 📅 2026-07-19 - A tool for testing n!n pins and Chinese-manufactured clones.
* [zmkfirmware/zmk-docker](https://github.com/zmkfirmware/zmk-docker) ⭐ 34 | 🐛 19 | 🌐 Dockerfile | 📅 2026-06-11 - Lightweight Docker images for ZMK
* [zmkfirmware/zmk-cli](https://github.com/zmkfirmware/zmk-cli) ⭐ 19 | 🐛 17 | 🌐 Python | 📅 2026-05-08 - Command line tool for ZMK Firmware
* [urob/zmk-actions](https://github.com/urob/zmk-actions) ⭐ 4 | 🐛 3 | 🌐 Shell | 📅 2026-08-01 - Github workflows for maintaining ZMK modules

## Hardware Addons must-have

* [hazels-garage/battpack](https://github.com/hazels-garage/battpack) ⭐ 66 | 🐛 0 | 📅 2026-03-26 - A 'backpack' for the nice!nano to make wiring up a battery cleaner on boards without native support
* [davidphilipbarr/nicehatharry](https://github.com/davidphilipbarr/nicehatharry) ⭐ 43 | 🐛 1 | 📅 2024-02-25 - A small 'hat' that sits ontop of the nice!nano to support a nice!view
* [george-norton/vik-hat](https://github.com/george-norton/vik-hat) ⭐ 6 | 🐛 0 | 📅 2025-07-11 - A ProMicro hat with a VIK connector
* [boardsource/Battery Helper](https://boardsource.xyz/products/battery-helper-ble-upgrade?_pos=10&_sid=cc9b52a5b&_ss=r) - Upgrade your Bluetooth Low Energy (BLE) controller with the nope, a cutting-edge PCB that empowers you to seamlessly integrate a power switch into any keyboard PCB, regardless of the make or model.

## Community Pointing Projects as Computer Mouse

* [aroum/ufa](https://github.com/aroum/ufa) ⭐ 40 | 🐛 1 | 📅 2026-08-17 - Focuses on porting the ZMK firmware to commercial gaming mice.
* [tokyo2006/zmk-for-cygnus](https://github.com/tokyo2006/zmk-for-cygnus/tree/main) ⭐ 11 | 🐛 1 | 🌐 C | 📅 2025-03-17 - The zmk configuration repo is here
  * [Pull requests](https://github.com/ploopyco/nano-trackball/pull/8) ⭐ 557 | 🐛 7 | 📅 2021-08-24
  * [tokyo2006/nano-trackball](https://github.com/tokyo2006/nano-trackball/tree/add_zmk_support) ⭐ 4 | 🐛 0 | 📅 2026-04-22 Using PMW3610 instead of ADNS-5050, Using type c instead of mini USB, Modify 3d model with Sharp3d, Using micro nrf52840 as MCU, Taobao link: Micro nrf52840, Aliexpress : Micro nrf52840, The schematic uses JLC EDA PRO so the project file is epro suffix.
* [george-norton/zmk-keyboard-ploopy](https://github.com/george-norton/zmk-keyboard-ploopy) ⭐ 7 | 🐛 0 | 🌐 C | 📅 2026-02-12 - Work in progress ZMK firmware for Ploopy RP2040 devices
* [badjeff/moudabella-zmk-config](https://github.com/badjeff/moudabella-zmk-config) ⭐ 6 | 🐛 0 | 📅 2026-03-18 - This is the ZMK firmware config repository for [moudabella](https://github.com/badjeff/moudabella) ⭐ 41 | 🐛 2 | 📅 2025-08-04, an open source bluetooth mouse 🐭 for CAD 🐱.
* [M-Tolbot/zmk-comfig-mouset](https://github.com/M-Tolbot/zmk-comfig-mouset) ⭐ 6 | 🐛 0 | 📅 2025-10-08 - This keyboard/mouse hybrid is my vision of a split keyboard with trackball - Inspired by my Hertao mouse.
* [badjeff/leylabella-zmk-config](https://github.com/badjeff/leylabella-zmk-config) ⭐ 3 | 🐛 0 | 📅 2026-03-18 - This is the ZMK firmware config repository for [leylabella](https://github.com/badjeff/leylabella) ⭐ 40 | 🐛 0 | 📅 2026-08-14, a computer mouse 🐭.

## Guides and Tutorials

### Bootloader and Reset

* [adafruit/RPI-RP2](https://learn.adafruit.com/adafruit-kb2040/circuitpython) - for rp2040 and kb2040. If your board ever gets into a really weird state and CIRCUITPY doesn't show up as a disk drive after installing CircuitPython, try loading this 'nuke' UF2 to RPI-RP2. which will do a 'deep clean' on your Flash Memory. You will lose all the files on the board, but at least you'll be able to revive it!
* [circuitpython/Update UF2 Bootloader](https://circuitpython.org/downloads) - After you update, check INFO\_UF2.TXT to verify that the bootloader version has been updated.
* [circuitpython/nice\_nano/Update UF2 Bootloader](https://circuitpython.org/board/nice_nano/) - After you update, check INFO\_UF2.TXT to verify that the bootloader version has been updated.
* [circuitpython/supermini\_nrf52840/Update UF2 Bootloader](https://circuitpython.org/board/supermini_nrf52840/) - After you update, check INFO\_UF2.TXT to verify that the bootloader version has been updated.
* [nicekeyboards/nice-nano/troubleshooting](https://nicekeyboards.com/docs/nice-nano/troubleshooting) - Troubleshooting your nice!nano often falls on to the firmware of choice, but a few directly hardware related items can be addressed.
* [aroum/nRF52\_Bootloader\_custom\_LED](https://github.com/aroum/nRF52_Bootloader_custom_LED) ⭐ 4 | 🐛 0 | 🌐 C | 📅 2026-07-05 - Contains various low-level modifications and hacks, such as converting the reset pin into a standard GPIO and implementing extended indication during Device Firmware Update (DFU) mode.

### Solder and Desolder Tools

> NOTE
> These tools have been tested first -hand (Except for Parllel Clamping, I have a model very similar to that) and could say that they are essential (personal perspective) helped me and still help me repeatedly and they have validated every penny!

* [PINECIL – Smart Mini Portable Soldering Iron (Version 2)](https://pine64.com/product/pinecil-smart-mini-portable-soldering-iron/) - The Pinecil is a smart mini portable soldering iron with a 32-bit RISC-V SoC featuring a sleek design, auto standby and it heats up to an operating temperature in just 6 seconds!
* [Stannol Kristall 611 Fairtin Solder](https://keycapsss.com/accessories/229/stannol-kristall-611-fairtin-solder-lead-free-lead-free-sn99-3cu0-7-rem1-100g-0.5-mm) - Stannol Kristall 611 Fairtin Solder, lead-free Lead-free Sn99,3Cu0,7 REM1 100g 0.5 mm
* [flux paste](https://www.amazon.de/Flussmittel-Paste-flussmittel-l%C3%B6tflussmittel-Mechaniker-Bauelemente/dp/B0BQCHSQLB/ref=sr_1_3?brr=1\&dib=eyJ2IjoiMSJ9.i5OJNeqPZsOWvTWOPhJfemcq5Vshx8bOfpCJvo6uHYeaUnEt59THLE2HTngdkTB0kjbNvZELXJhgKUJy4JlBEo9yrfwOefmYt4wOzco4nsFQ_Ix-K5YO4a-nP6tIzJ1dKX5az_weIXCalzWCMHaGoT0MreIIoBJWN7o8F7KgG9SAJwwzp-kgdFTWAuIR8dcTRO_G7AajTdJjWuZiPDkgBcbX9nSu2ME2bCNHZBr4344.SV-83bxaSj-1NyW18QdA39UbNKZxFD8JSyUCKXEizek\&dib_tag=se\&qid=1759839725\&rd=1\&s=diy\&sr=1-3) - 1 piece of 10g of flux paste, soldering fat flux, soldering paste, soldering fluid, soldier paste, solder paste, for mechanics, metal, tin, telephone, PC cards, components
* [Liquiq flux no-clean](https://www.amazon.de/Flasche-Pinsel-L%C3%B6twasser-Weichl%C3%B6ten-Flussmittel/dp/B0C1C4S5BT/ref=sr_1_73?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91\&dib=eyJ2IjoiMSJ9.wg0NoP9fb_OM2clfuWyenF-EWg_MTOOICkLDWaJI7xCmIIZl0t0y8HvM_FIxR9icffXTV0Byerp2-jmj373ERgL4S7pMtyUy1pEMV8JPNTvgIzcsNV5c5A-7oQNqVHAkTuYRlJ7dRXM3BRnQClWDgh7dp7XVGXfRSaGOHqTIywC-bAqKXPS9J-hAC5l16lmG.v_EGninoAXlVV0GqPDScXjWAgo4HKGNV9A9ErBMppRE\&dib_tag=se\&keywords=flux+no+clean+for+soldering\&qid=1759839868\&s=diy\&sr=1-73\&xpid=1eHgHndJ67fZa) - 50 ml bottle with brush soldering water soldering soft soldering river SMD BGA zinc
* [Desolder / solder SEQURE HT140 2-IN-1 Hot Tweezers](https://sequremall.com/products/sequre-ht140-2in1-hot-tweezers-soldering-iron-desoldering-repair-tool-for-smd?variant=44204748308668) - SEQURE HT140 2-IN-1 Hot Tweezers And Soldering Iron Compatible with C210 Soldering Tips And C120 Hot Tweezers Cartridge Tips Desoldering Tips Support PD QC DC Power Supply Desoldering Repair Tool for SMD
* [Desolder pump](https://de.aliexpress.com/item/1005005632540345.html?spm=a2g0o.order_list.order_list_main.329.49775c5fDIIQvQ\&gatewayAdapt=glo2deu) - Tin-suction vacuum with 3-suction nozzle, EU/US plug, soldering, removal of the pump, electrical soldering device ADT03, new removal machine
* [Desolder / solder air pump](https://de.aliexpress.com/item/1005006284776301.html?spm=a2g0o.order_list.order_list_main.324.49775c5fDIIQvQ\&gatewayAdapt=glo2deu) - Yihua micro hot air pistol C/F temp set 8858IV 700 W solder rework welding station LCD digital hot air pistol BGA IC soldering tools
* [Parallel Clamping](https://omnifixo.com/en-eu) - Firm grip that keeps components in place, large jaw opening (9/16", 14mm), no bitemarks or scratching, narrow and flat jaws, easy to find somewhere to hold
* [Precision Tweezers Set](https://www.ifixit.com/products/precision-tweezers-set) - Grab everything from screws to eyebrows with iFixit's Precision Tweezers Set.
* [Soldering Tip Cleaning Ball Hakko 599B](https://www.ifixit.com/products/soldering-tip-cleaning-ball-hakko-599b) - The HAKKO 599B cleans your soldering iron tips without water! The 599B is made from coils of brass, which is softer than the tip plating yet harder than the oxidation that forms on the tip.
* [Diagonal Cutters](https://www.adafruit.com/product/152) - Diagonal cutters, large super-comfortable grip to use and have strong nippers for perfect trimming of wires and leads

### How to Solder

* [Making a good solder joint](https://learn.adafruit.com/adafruit-guide-excellent-soldering/making-a-good-solder-joint) - by Bill Earl published September 06, 2012, last edited May 01, 2024 posted in Tools/ Hand Tools Tools/ Soldering
* [Surface Mount Components](https://learn.adafruit.com/adafruit-guide-excellent-soldering/surface-mount) - by Bill Earl published September 06, 2012, last edited May 01, 2024 posted in Tools/ Hand Tools Tools/ Soldering
* [Common Soldering Problems](https://learn.adafruit.com/adafruit-guide-excellent-soldering/common-problems) - by Bill Earl published September 06, 2012, last edited May 01, 2024 posted in Tools/ Hand Tools Tools/ Soldering
* [Tools](https://learn.adafruit.com/adafruit-guide-excellent-soldering/) - Personally I prefer the tools above "[Solder and Desolder Tools](#solder-and-desolder-tools)", but of course those are much cheaper!
* [How to Solder: Through-Hole Soldering](https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering) - Soldering is one of the most fundamental skills needed to dabble in the world of electronics.
* [How to Test Diodes with a Digital Multimete](https://www.fluke.com/en-au/learn/blog/digital-multimeters/how-to-test-diodes) - Digital multimeters can test diodes using one of two methods

### How to Desolder

* [How To Solder and Desolder Connections](https://www.ifixit.com/Guide/How+To+Solder+and+Desolder+Connections/750) - While many repairs can be accomplished without soldering, there are times when it's necessary to replace soldered-down components, e.g., joysticks, headphone batteries, and rumble motors.
* [The Ultimate Guide to Desoldering](https://www.instructables.com/The-Ultimate-Guide-to-Desoldering/) - From using desoldering irons to sketchily knocking breadboard components off on the side of a table, there are tons of ways to remove components from a circuit board.

### Solder and Desolder Videos

* [mrsolderfix3996/youtube.com](https://www.youtube.com/@mrsolderfix3996) - My video's will be covering many aspects of soldering ,  ranging from the very basic stuff to the very extreme difficult projects, with the odd fun project to make popped in along the way
* [paceworldwide/youtube.com](https://www.youtube.com/@paceworldwide) - For over forty years, PACE, Inc. has provided state-of-the-art, hands-on solder training to the electronics industry around the world. Courses and support materials are available for Surface Mount Technology, Through-Hole Technology and Multilayer PCB Repairs.
* [How to solder and desolder SMD using hot air](https://www.youtube.com/watch?v=pIX3sGDs3CQ) - A quick and complete tutorial about surface mount components (SMD/SMT) soldering and desoldering using hot air station.

### Supported Hardware

> NOTE
> These are the most popular boards, [but there are more](https://zmk.dev/docs/hardware)

Wireless - Pro Micro Interconnect (nRF52840 and others)

* [nRFMicro 1.1/1.2](https://github.com/joric/nrfmicro) ⭐ 1,856 | 🐛 0 | 🌐 HTML | 📅 2025-08-04 - Board: `nrfmicro_11`
* [nRFMicro 1.3/1.4](https://github.com/joric/nrfmicro) ⭐ 1,856 | 🐛 0 | 🌐 HTML | 📅 2025-08-04 - Board: `nrfmicro_13`
* [Mikoto](https://github.com/zhiayang/mikoto) ⭐ 351 | 🐛 6 | 🌐 HTML | 📅 2025-03-14 - Board: `mikoto`
* [nice!nano v2](https://nicekeyboards.com/nice-nano/) - Board: `nice_nano_v2`
* [nice!nano v1](https://nicekeyboards.com/nice-nano/) - Board: `nice_nano`
* [Puchi-BLE V1](https://keycapsss.com/keyboard-parts/mcu-controller/202/puchi-ble-wireless-microcontroller-pro-micro-replacement) - Board: `puchi_ble_v1`
* [SuperMini NRF54840](https://de.aliexpress.com/item/1005006035267231.html?gatewayAdapt=glo2deu) - Board: `nice_nano_v2`
* [Vikoto](https://fingerpunch.xyz/product/vikoto/) - Board: `vikoto`

Wired - Pro Micro Interconnect (RP2040 and others)

* [SparkFun Pro Micro RP2040](https://www.sparkfun.com/sparkfun-pro-micro-rp2040.html) - Board: `sparkfun_pro_micro_rp2040`
* [BoardSource blok RP2040](https://peg.software/docs/blok) - Board: `boardsource_blok`
* [Adafruit KB2040](https://www.adafruit.com/product/5302) - Board: `adafruit_kb2040`
* [QMK Proton-C](https://www.google.com/search?q=https://qmk.fm/proton-c/) - Board: `proton_c`
* [Svlinky](https://fingerpunch.xyz/product/svlinky/) - Board: `svlinky@0.2.0` and `svlinky@0.1.0`

Wireless - Seeed XIAO Interconnect (nRF52840 and others)

* [Seeed Studio XIAO nRF52840](https://www.seeedstudio.com/Seeed-XIAO-BLE-nRF52840-p-5201.html) - Board: `seeeduino_xiao_ble`

Wired - Seeed XIAO Interconnect (RP2040 and others)

* [Adafruit QT Py RP2040](https://www.adafruit.com/product/4900) - Board: `adafruit_qt_py_rp2040`
* [Seeed Studio XIAO RP2040](https://www.seeedstudio.com/XIAO-RP2040-v1-0-p-5026.html) - Board: `seeeduino_xiao_rp2040`
* [Seeed Studio XIAO SAMD21](https://wiki.seeedstudio.com/Seeeduino-XIAO/) - Board: `seeeduino_xiao`
* [Xivik](https://fingerpunch.xyz/product/xivik/) - Board: `xivik@0.1.0`,`xivik@0.2.0` and `xivik@0.3.0`

### Hardware Tutorials

* [diimdeep/awesome-split-keyboards](https://github.com/diimdeep/awesome-split-keyboards) ⭐ 5,849 | 🐛 36 | 📅 2024-07-06 - A collection of ergonomic split keyboards
* [ebastler/zmk-designguide](https://github.com/ebastler/zmk-designguide) ⭐ 491 | 🐛 6 | 📅 2024-07-06 - A short hardware-designguide for ZMK keyboards.
* [ebastler/zmk-designguide](https://github.com/ebastler/zmk-designguide) ⭐ 491 | 🐛 6 | 📅 2024-07-06 - A community-written guide for designing PCBs intended to be used with ZMK.
* [GOLEM keyboard project](https://golem.hu/board/) - Split keyboard database
  * [Typing tests and Keyboard sounds](https://golem.hu/sound/)
* [Thumb cluster comfort from SplitKB made by jhelvy](https://compare.splitkb.com/) - Thumb cluster comfort is pretty individual based on hand size. You can use  scaled on a screen or printout to get an idea of how your hand fits different thumb clusters.
* [Compare Keycaps Profiles](https://www.keycaps.info/) - Support Choc and Cherry MX

### Software Tutorials

* [Maintaining a personal ZMK fork](https://gist.github.com/urob/68a1e206b2356a01b876ed02d3f542c7) - A cookbook approach to maintaining a personal ZMK fork.
* [mod-tap/mod-tap/homerow mods bible](https://precondition.github.io/home-row-mods) - behaviors bible
* [KeymapDB](https://keymapdb.com/) - KeymapDB (“Keymap Database”) is a public and open-source online database for keymaps of programmable keyboards, with a focus on ZMK / QMK ergonomic keyboards.

### Learn Touch Typing

* [Typeracer](https://play.typeracer.com/) - The award-winning online typing competition, TypeRacer, allows people to race each-other by typing quotes from books, movies, and songs. It is the first multiplayer typing game on the web.
* [Monkeytype](https://monkeytype.com/) - Monkeytype is a minimalistic and customizable typing test.
* [keybr](https://www.keybr.com/) - This web application will help you to learn touch typing which means typing through muscle memory without using your eyesight to find the keys. With multiplayer typing game on the web

## Keyboard News

* [kbd.news](https://kbd.news/) - KBD.news is a blog and newsletter on DIY mechanical keyboards. A hand-picked selection of posts from a keyboard enthusiast's perspective
* [ErgoMechKeyboards/reddit.com](https://www.reddit.com/r/ErgoMechKeyboards/) - A community focused around Ergonomic Mechanical Keyboards and strange input devices. Embrace the jank. Created Sep 2, 2019
* [crkbd/reddit.com](https://www.reddit.com/r/crkbd/) - crkbd, a.k.a. Corne Keyboard <https://github.com/foostan/crkbd> ⭐ 7,605 | 🐛 23 | 🌐 Makefile | 📅 2025-05-10 <https://discord.com/invite/aWCZWnS> Created Dec 16, 2019

### Keyboard News Videos

* [Building Open Keyboards with ZMK & Zephyr // Zephyr Tech Talk #010 ](https://www.youtube.com/live/Eb04hyUY4BE?si=l4-114QAmFnJbyc7\&t=1) - Tune in on Wednesday, January 24 (9:00 AM EST / 3:00 PM CET) for a new Zephyr Tech Talk live stream where Benjamin will be joined by Pete Johanson, creator and project lead of the ZMK project.
* [Naya Create: From Hate To Love To Regret - Full Review](https://youtu.be/gqzrcoNpgGU?si=cVFWv9tcqKLYdO14) - The Naya Create is/was an amazing feat, it actually delivered on almost all of the promises. However, there are quite a few hardware issues, some which can be fixed others you'll have to live with.

<!-- ### Keyboard News ErgoMechKeyboards -->

<!-- REDDIT:START -->

<!-- REDDIT:END -->

## Keyboard Shops

* [mechanical keyboard vendors list](https://kbd.news/vendors) - Where to buy mechanical keyboards, switches or keycaps? This keyboard shop database lists 600+ stores offering keyboards, kits, various parts and accessories.

## Projects using ZMK closed-source or not upstreamed

* [nrfconnect/sdk-nrf/../pmw3360](https://github.com/nrfconnect/sdk-nrf/tree/main/drivers/sensor/pmw3360) ⭐ 1,408 | 🐛 257 | 🌐 C | 📅 2026-08-17 - PMW3360 mouse optical sensor
  * [LicenseID:  LicenseRef-Nordic-5-Clause](https://github.com/nrfconnect/sdk-nrf/blob/main/LICENSE) ⭐ 1,408 | 🐛 257 | 🌐 C | 📅 2026-08-17 - Copyright (c) 2018, Nordic Semiconductor ASA
* [taichan1113/AdeptBLE](https://github.com/taichan1113/AdeptBLE) ⭐ 159 | 🐛 4 | 📅 2025-04-02 - This is alpha version of Ploopy Adept BLE modification.
  * [Post on reddit](https://www.reddit.com/r/Trackballs/comments/rtmeeq/a_portable_trackball_i_wanted_zmk_powered_some/)
  * [Video and photos](https://imgur.com/gallery/zmk-trackball-prototype-RhXke0e)
* [rianadon/zmk](https://github.com/rianadon/zmk/tree/main) ⭐ 1 | 🐛 1 | 🌐 C | 📅 2026-06-01 - fork for cosmos
  * [ryanis/Custom-Build (web)](https://ryanis.cool/cosmos/) - Custom-Build A Keyboard Fit To You. Don't Settle. For One-Size-Fits-All
  * [Lemon Wireless Microcontroller](https://ryanis.cool/cosmos/lemon/) - Store for buy the MCU
* [Naya Keyboard](https://naya.tech/) - Fully modular hardware and endlessly customizable software engineered for effortless ergonomics and peak performance.
* [Keychron B1 Pro Ultra-Slim Wireless Keyboard](https://www.keychron.com/products/keychron-b1-pro-ultra-slim-wireless-keyboard) - Keychron B1 Pro is an ultra-slim wireless keyboard. It supports 2.4 GHz, Bluetooth, and a wired connection.
  * [Keychron source code on GitHub](https://github.com/Keychron/zmk/tree/keychron_bpro/app/boards/shields/keychron) ⭐ 45 | 🐛 4 | 🌐 C | 📅 2026-05-28
* [Advantage360 Professional](https://kinesis-ergo.com/shop/adv360pro/) - Our flagship fully-split contoured keyboard designed to provide maximum comfort and adjustability.
  * [Adv360-Pro-ZMK source code on GitHub](https://github.com/KinesisCorporation/Adv360-Pro-ZMK) ⭐ 599 | 🐛 26 | 🌐 Shell | 📅 2026-06-14 - Production repository for the all-new Advantage360 Professional using ZMK engine
* [Disconnect MK1](https://www.hidergo.fi/) - The culmination of function, productivity and appearance. Disconnect MK1 is the ultimate keyboard for work and play.
  * [osmakari/zmk source code on GitHub](https://github.com/osmakari/zmk) ⭐ 11 | 🐛 0 | 🌐 C | 📅 2023-08-11 - For the curious, we keep the firmware open source! You are free to hack away on the firmware and make it truly your own!

## Related projects

* [dotintent/awesome-ble](https://github.com/dotintent/awesome-ble) ⭐ 145 | 🐛 3 | 📅 2025-05-30 - general BLE resources (useful Nordic links included).
* [whoop-t/nice-shield-collection](https://github.com/whoop-t/nice-shield-collection) ⭐ 76 | 🐛 0 | 📅 2026-01-25 - A collection of links to nice!view shield designs
* [ssbb/awesome-zmk](https://github.com/ssbb/awesome-zmk) ⭐ 35 | 🐛 0 | 📅 2026-04-29 - curated list of ZMK drivers, behaviors, tools and guides.
* [iDoka/awesome-nRF5](https://github.com/iDoka/awesome-nRF5) ⭐ 7 | 🐛 0 | 📅 2021-06-14 - curated resources for nRF5 (libraries, examples, build helpers).

## License

This list is licensed under the [Creative Commons Zero v1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/).

<p align="right">
  <a href="#top">⬆️  back to Table of Contents</a>
</p>

[^1]: ZMK Firmware official website: <https://zmk.dev>

[^2]: ZMK Firmware official code repository: <https://github.com/zmkfirmware/zmk> ⭐ 4,219 | 🐛 420 | 🌐 C | 📅 2026-08-17

[^3]: Zephyr Project official website: <https://www.zephyrproject.org>

[^4]: Zephyr Project Code Repository: <https://github.com/zephyrproject-rtos/zephyr> ⭐ 16,233 | 🐛 3,877 | 🌐 C | 📅 2026-08-17

[^5]: Online Power Profiler for Bluetooth LE: <https://devzone.nordicsemi.com/power/w/opp>

[^6]: Pete Johanson: <https://petejohanson.dev/>

[^7]: joric dongles wiki: <https://github.com/joric/nrfmicro/wiki/Alternatives#dongles> ⭐ 1,856 | 🐛 0 | 🌐 HTML | 📅 2025-08-04

[^11]: ZMK Firmware official physical layouts integration: We recommend the use of this tool for writing a physical layout or converting one from a QMK JSON definition. If your keyboard already has a physical layout defined for the use with KLE, we recommend using this other tool first to convert your existing layout into QMK JSON. The second tool can also import the position data from KiCAD, if said program was used to design the keyboard - <https://zmk.dev/docs/development/hardware-integration/physical-layouts>

[^12]: Hardware Integration: <https://zmk.dev/docs/development/hardware-integration#what-is-a-shield>

[^13]: Modules: <https://zmk.dev/docs/features/modules>

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-08-17._

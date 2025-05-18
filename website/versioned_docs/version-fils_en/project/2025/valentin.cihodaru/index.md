# Project Name
A one line project description

:::info 

**Author**: Cihodaru Valentin-Alexandru \
**GitHub Project Link**: https://github.com/UPB-PMRust-Students/project-Vulisu

:::

## Description

An mp3/wav player that reads the song from a sd card and plays it on a bluetooth speaker. The mp3 
player also has a potentiometer that is used to change the volume, a play/pause button and skip 
song and backwards buttons. 
## Motivation

I chose this project because I think an mp3 bluetooth player that has the songs stored offline can be helpful when there is no internet access.
## Architecture 
### Raspberry Pi Pico 2W

Acts as the main microcontroller.

Connected to various GPIOs for peripherals like buttons, SD card, and LED.

### SD Card Reader

Connected via SPI:

CS, SCK, MOSI, MISO

For reading audio or data files.

### MH-M28 Bluetooth Audio Module 

Handles audio output over Bluetooth.

Connected to 5V, GND, and analog outputs (L, R).

Includes AGND for audio ground isolation.

Volume control via potentiometer.

### Potentiometer 

Connected to the audio module for analog volume control.

### Push Buttons (SW1, SW2, SW3)

Functions:

SW1: Pause/Play

SW2: Next Song

SW3: Previous Song

Connected to GPIOs of the RP2040.

### LED Indicator 

LED with a current-limiting resistor (220Ω).

Used for indicating if the song is paused or playing.
![Schematic diagram](schema.webp)


## Log

<!-- write your progress here every week -->

### Week 5 - 11 May

### Week 12 - 18 May

### Week 19 - 25 May

## Hardware

1xRaspberry pi pico 2W
1xSd card reader module
1x MH-M28 bluetooth transimtter
1xPotentiometer
3xPush buttons
1xLED

### Schematics

![Schematic diagram](kicad.webp)

### Bill of Materials

<!-- Fill out this table with all the hardware components that you might need.

The format is 
```
| [Device](link://to/device) | This is used ... | [price](link://to/store) |

```

-->

| Device | Usage | Price |
|--------|--------|-------|
| [Raspberry Pi Pico W](https://www.raspberrypi.com/documentation/microcontrollers/raspberry-pi-pico.html) | The microcontroller | [35 RON](https://www.optimusdigital.ro/en/raspberry-pi-boards/12394-raspberry-pi-pico-w.html) |


## Software

| Library | Description | Usage |
|---------|-------------|-------|
| [st7789](https://github.com/almindor/st7789) | Display driver for ST7789 | Used for the display for the Pico Explorer Base |
| [embedded-graphics](https://github.com/embedded-graphics/embedded-graphics) | 2D graphics library | Used for drawing to the display |

## Links

<!-- Add a few links that inspired you and that you think you will use for your project -->

1. [link](https://example.com)
2. [link](https://example3.com)
...

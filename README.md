# 🏁 Fast Line Follower

> Raspberry Pi Pico 2W · TB6612FNG · 8-channel IR array · Custom EasyEDA PCB

![Status](https://img.shields.io/badge/status-in%20progress-yellow)
![MCU](https://img.shields.io/badge/MCU-Pico%202W-c51a4a)
![Firmware](https://img.shields.io/badge/firmware-Arduino%20C%2B%2B-00979D)

<!-- TODO: robot photo -> media/hero.jpg -->
<!-- TODO: track run video/GIF -> media/run.gif -->

## Overview

A competition-style fast line follower on a custom PCB. Motor-driver bring-up was tested in CircuitPython. The main firmware is being written in Arduino C++ on the earlephilhower arduino-pico core.

## Hardware

| Part | Detail |
|---|---|
| Controller | Raspberry Pi Pico 2W |
| Line sensor | Yahboom 8-channel IR array (onboard STM8L151), read over UART |
| Motors | 2 × N20 500 RPM with encoders |
| Driver | TB6612FNG dual H-bridge |
| Power | 2S LiHV, MC7805 → 5 V into Pico VBUS, XT30 connector |
| Indicators | 2 LEDs driven by BC547 transistors |

<!-- TODO: block diagram -> media/block-diagram.png -->

## Pico pin map

| Function | GPIO |
|---|---|
| PWMA / PWMB | GP0 / GP1 |
| AIN1, AIN2 / BIN1, BIN2 | GP2, GP3 / GP4, GP5 |
| Driver standby | GP6 |
| Indicator LEDs | GP7 |
| IR sensor lines x1–x8 | GP8–GP15 |
| Sensor UART RX / TX | GP16 / GP17 |
| Motor A encoder | GP18 / GP19 |
| Motor B encoder | GP26 / GP27 |
| Button / reset | GP20 / GP21 |

## PCB

EasyEDA project "fastLineFollower", rev 1.0, made by JLCPCB.

<!-- TODO: schematic PDF -> hardware/schematic.pdf, PCB render -> media/pcb.png, Gerbers -> hardware/gerbers/ -->

## Roadmap

- [x] Schematic and PCB
- [x] Motor driver bring-up
- [ ] Encoder-based speed control
- [ ] PID line tracking and tuning
- [ ] Lap-time results

## Author

**Jasin Jesin** · [LinkedIn](https://www.linkedin.com/in/jasinjesin/)

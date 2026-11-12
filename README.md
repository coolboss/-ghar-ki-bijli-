# Ghar Ki Bijli

An interactive explainer of home electricity in India. It follows the electricity from the MGVCL substation to the socket in your room, as one flow in seven stages:

Substation → Transformer → Street line → Meter → Board → Wall → Room

**Open it:** https://coolboss.github.io/-ghar-ki-bijli-/ (once GitHub Pages is turned on for this repo)

## What you can do

- **Switch something on.** Pick an LED bulb, fan, iron, AC or geyser. Every stage shows its own numbers, for example 8.7 A in the wall but only 0.18 A on the 11 kV feeder.
- **Break something.** Pick overload, short circuit or earth leakage and see which device trips and what goes dead after it.
- **Tap a stage** to open its chapters. The Chapters tab lists all of them:
  - volt, ampere, watt and unit
  - single phase vs three phase
  - smart meters and a 30-minute known-load test
  - MCB, RCCB, RCBO and SPD: who protects whom
  - a tap-through distribution board
  - MDB and SDB, with a phase balancing tool
  - inverter and UPS sizing
  - wire colours, exactly
  - quiet faults and the I²R heater
  - room wiring, switches and sockets
  - earthing
- **Passport.** The idea of a QR code on every meter box that points to the house's wiring record, with a builder to make your own.
- **Exam.** Twelve questions an ITI wireman should get right.

## How it is built

One file, `index.html`. No build step and no server. It works on a phone and on a desktop, in light and dark mode.

It loads two things from the internet: three Google Fonts, and the `qrcodejs` library from cdnjs for the QR builder. Everything else works offline.

## Please note

This is for learning. It follows Indian practice (230 V single phase, 415 V three phase, 50 Hz; IS 732, IS 3043, NEC-India 2023) and uses MGVCL and Vadodara as the worked example. Currents shown in the flow are simplified: watts ÷ volts, with losses and power factor ignored.

It is not a substitute for a licensed electrician. Do not work on live wiring.

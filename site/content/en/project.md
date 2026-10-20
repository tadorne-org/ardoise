---
title: "The instrument"
translationKey: project
url: /project/
description: "A mast-foot display, readable from the cockpit, on the boat's NMEA 2000 bus."
params:
  eyebrow: "Ardoise"
  figures:
    - label: "Power and data"
      value: "NMEA 2000"
    - label: "Other sources"
      value: "Signal K · phone"
    - label: "Refresh"
      value: "1 Hz"
    - label: "Control"
      value: "Phone, no buttons"
---

## The need

When racing, the useful numbers are read at a glance from the cockpit or the rail: countdown, speed, heading and lift, wind angle and strength. At three to six metres, in full sun, with or without polarised glasses.

## The screen

A reflective memory screen: black on white, refreshed every second, without the ghosting of e-paper. It returns daylight the way a printed sheet does. The pages are drawn for distance: three giant digits rather than four small ones.

<div class="photo-grid">
  <img src="/img/ecran-pre-depart.webp" alt="Screen mock-up: start countdown 4:59 in giant digits.">
  <img src="/img/ecran-pre-depart-inverse.webp" alt="Screen mock-up: last minute before the start, inverted.">
  <img src="/img/ecran-pres.webp" alt="Screen mock-up: upwind, large heading, lift, speed and polar percentage.">
  <img src="/img/ecran-portant.webp" alt="Screen mock-up: downwind, two stacked values.">
  <img src="/img/ecran-neutre.webp" alt="Screen mock-up: four values, speed and wind.">
  <img src="/img/ecran-tendance-vent.webp" alt="Screen mock-up: ten-minute wind trend.">
</div>

*Design mock-ups, example values. Resolution and typefaces of the series may differ.*

## The sources

Ardoise reads the **NMEA 2000 bus** it is plugged into: speed, heading, wind, depth, position. If there is a **Signal K** server on board, it reads that too, over Wi-Fi. The phone sets the pages, pings the line and syncs the start. The countdown runs on the instrument's own clock: if the link drops, it carries on.

An on-board compass gives heading, heel and pitch, even with no other instrument on board.

## One cable

A single connector, at the bottom of the tube: the bus drop powers it and brings the data. No other cable entry, no buttons.

## Endurance

A machined aluminium tube, closed by a flush window and an aluminium plate. The foot of the mast takes green water, UV, the heat of a surface in the sun and the vibration of the rig. Sealing and environmental tests will be run, and their reports published.

## Service

Firmware updates over the air, as signed images. The enclosure opens with tools and its seals are replaceable: the atelier will be able to repair every unit.

## The making

Ardoise will be made in small numbered series.

On request. [Get in touch](mailto:contact@tadorne.org?subject=Ardoise)

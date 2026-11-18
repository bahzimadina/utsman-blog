---
title: "Utsman Device Progress: Full Circular Display, Local Sync, and Watcher Camera"
date: 2026-11-18
slug: utsman-device-hardware-progress
lang: en
pair: utsman-device-progress
cover: /blog/images/utsman-device-watcher-2026-11.jpg
excerpt: Development update on the physical Utsman Device prototype built on SenseCAP Watcher, covering full-screen circular camera previews and local MQTT sync.
tags: [utsman-device, hardware, watcher, progress]
draft: false
---

Until now, Utsman has mostly lived inside phone screens through WhatsApp, Telegram, and email. This week marks an early step into physical hardware: a dedicated desk prototype called **Utsman Device**, built on top of the **Seeed Studio SenseCAP Watcher**.

Inside its translucent enclosure, Utsman moves beyond a chat window. The front houses a circular touchscreen paired with a camera lens in the top corner, built-in microphones, and a speaker. In today's test run, the custom interface is already live on the round display: Wi-Fi and battery status icons sit at the top, the **"Mendengarkan..."** listening prompt appears cleanly underneath, and Utsman's avatar rests at the center of the circle.

Work during this session focused on two practical areas: reliable reconnection right after flashing firmware and making camera previews fit the round screen properly.

## Local networking with utsman.local and MQTT

To keep voice interaction and image handling responsive without relying solely on external hops, the prototype connects directly to our local server at `utsman.local` over MQTT. Initial network onboarding now supports **Wi-Fi QR** provisioning as well, cutting down setup friction on a fresh device.

One small snag showed up right after flashing: the unit took roughly two minutes to come back online because opening the USB serial port triggered an unexpected reset cycle. After inspecting the serial logs and server connection state, the boot sequence settled down—bringing Wi-Fi, MQTT messaging, voice conversation, and camera capture back to normal.

## Full-bleed camera preview on a round display

The most visible change in this update is how captured camera frames appear on the front display. Previously, a 240x240 image was scaled down into a smaller 200x200 square in the center, leaving noticeable empty borders around the circular bezel.

With the latest firmware updates in `xiaoai-client.patch` and `client.cpp`, the camera preview now fills the full 360x360 circular screen while preserving aspect ratio:

- Captured photos span edge to edge across the circular panel instead of shrinking into a centered square, trimming only a thin margin along the left and right edges to match the circle.
- Top status indicators and bottom prompt text remain visible cleanly over the preview layer.
- Images uploaded to the server stay completely untouched at full 480x480 resolution so downstream visual processing keeps full detail.

## What comes next

With full-screen circular framing, Wi-Fi QR setup, and `utsman.local` connectivity verified on the hardware, the next step is testing the interaction menu and running end-to-end camera capture checks before committing the firmware changes.

The immediate goal stays grounded: a compact desk companion that plugs in, joins the local network, and stands ready to listen or inspect documents and surroundings directly.

# Network Monitor – Rainmeter Skin

A compact Rainmeter widget that displays real-time Upload and Download network speeds in a clean, minimal panel.

---

## Features

- Live **Upload** and **Download** speeds  
- Auto-scaled values (KB/s, MB/s) with one-decimal precision  
- Smooth indicator bars scaled to your connection’s max bandwidth  
- Lightweight translucent panel with rounded corners  
- Fully self-contained skin with zero dependencies  

---

## Preview

<img width="270" height="124" alt="image" src="https://github.com/user-attachments/assets/81bf3227-740d-42fc-9472-e8010c154973" />

---

## How It Works

The skin uses two built-in Rainmeter measures:

- **NetIn**  
  Reports incoming network speed in bytes/sec.  
  Scaled using `NetInSpeed = MaxDownload` so the Download bar fills proportionally.

- **NetOut**  
  Reports outgoing network speed in bytes/sec.  
  Scaled using `NetOutSpeed = MaxUpload` so the Upload bar fills proportionally.

Both values refresh every **1000 ms**, ensuring smooth and stable updates.

The panel is rendered using two layered shapes:

- Primary rounded rectangle  
- Translucent header strip  

Indicator bars use Rainmeter’s built-in `Bar` meter with `HORIZONTAL` orientation.

---

## Performance Cost

The skin is rendered from a single `network_monitor.ini` file, keeping overhead extremely low.

Typical system usage:

- **RAM:** ~10–30 MB depending on system  
- **CPU:** ~0% in steady state  

The runtime footprint is negligible and suitable for permanent desktop use.

---

## Customization (Optional)

All visual and functional parameters are contained in the `[Variables]` section.

You may adjust:

- Panel width, height, padding, and corner radius  
- Primary font and text sizes  
- Bar colors, bar height, and background opacity  
- Maximum upload and download speeds (affects bar scaling)

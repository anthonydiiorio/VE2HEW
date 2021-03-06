---
layout: post
title:  "PowerSDR Skin: Flat Blue"
date:   2019-12-17
categories: sdr thetis
image: img/2019/12/VE2HEW-Flat-Blue-thumb.png
---

This is my first skin for PowerSDR, OpenHPSDR, Thetis, NaP3, etc. It's clean and simple. All the project files are in the repo for you to edit in Photoshop. I'll probably make some more as time allows.

<!-- Place this tag where you want the button to render. -->
<a class="github-button" href="https://github.com/anthonydiiorio/PowerSDR-Skins" data-color-scheme="no-preference: dark; light: light; dark: dark;" data-size="large" aria-label="Download anthonydiiorio/LZ1AQ-Loop-Controller on GitHub">Download on GitHub</a>

![](/img/2019/12/VE2HEW-Flat-Blue.png)

### Setup -> Appearance 

#### General 
<div style="overflow-x:auto;" markdown="block">

| VFO | RGB | Band Data |  RGB |
|---|---|---|---|
| Inactive | 255 255 255 | Inactive | 191 191 191 |
| Active | 255 255 255 | Active | 218 218 218 |
| Background | 0 0 0 | Out of Band | 105 105 105 |
| Small Color | 255 255 255 | Background | 0 0 0 |
| Info Color | 255 140 0 |

</div>

#### RX Display 

<div style="overflow-x:auto;" markdown="block">

| Panadapter | RGB | Grid | RGB | Cursor/Peak Readout | RGB |
|---|---|---|---|---|---|
| Main RX Filter | 255 255 255 | Background | 0 0 0 | Peak Text | 30 144 255 |
| TX Filter | 64 159 255 | V-Grid | 255 255 255 | Background | 0 0 0 |
| Band Edge | 255 0 0 | V-Grid Fine | 255 255 255 |
| MultiRX Filter | 64 159 255 | H-Grid | 255 255 255 |
| MultiRX Zero Line | 135 206 250 | Zero Line | 255 255 255 |
| GrayLine | 0 0 0 | Text | 255 255 255 |

</div>

## Instructions

### PowerSDR, OpenHPSDR, Thetis

**Thetis:** copy skin folder to **`%AppData%\OpenHPSDR\Skins`**

**PowerSDR & mRX PS:** copy skin folder to **`%AppData%\FlexRadio Systems\PowerSDR\skins`**

Enable Skin: **`Setup -> Appearance -> General -> Skins`**

### NaP3

**Build:** Run **`Skin Folder\Console\Base\build-NaP3.bat`** to generate NaP3 skin

**NaP3:** copy skin folder to **`%ProgramFiles(x86)%\NaP3\Skins`**

Enable Skin: **`Setup -> Configure Nap3 -> Colours -> General -> Skins`**

### Modding

.PSD Files available in **`Skin Folder\Console\Base`**

Rebuild theme with **`build-PowerSDR.bat`** or **`build-NaP3.bat`**

<!-- Place this tag in your head or just before your close body tag. -->
<script async defer src="https://buttons.github.io/buttons.js"></script>


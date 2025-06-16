# 💾 ROM Dumping & Patching Guide

Bad ROMs and pre-patched files are the #1 cause of crashes, freezes, and save issues on EZ-Flash Omega and Omega DE. This guide ensures you're using clean, compatible ROMs and applying patches properly.

---

## 🧼 Start with a Clean ROM

A clean ROM is an unmodified game dump that exactly matches the original cartridge.

### ✅ Best Practices
- Use **No-Intro verified ROMs** when possible
- File extensions: `.gba`, `.gb`, `.gbc`, `.nes`
- Avoid downloading "pre-patched" or "ROM hack included" files

> 💡 Tip: Use [Hashtab](https://implbits.com/products/hashtab/) to verify your ROM hash matches known good dumps.

---

## 🧪 Patching a ROM Hack

Most ROM hacks come as a patch file (.IPS, .UPS, or .BPS) and must be applied to a clean ROM.

### 📋 Required Tools
| Patch Type | Tool | Notes |
|------------|------|-------|
| IPS        | [Lunar IPS](https://www.romhacking.net/utilities/240/) | Simple tool for `.ips` patches |
| UPS        | [NUPS](https://www.romhacking.net/utilities/606/), [Tsukuyomi](https://www.romhacking.net/utilities/519/) | `.ups` patches are common for FireRed hacks |
| BPS        | [Flips](https://www.romhacking.net/utilities/1040/) | Used in newer ROM hacks |
| Online     | [ROM Patcher JS](https://www.marcrobledo.com/RomPatcher.js/) | Browser-based patcher for all formats |

### 🔧 How to Patch (Example for NUPS)
1. Open NUPS
2. Select "Apply an UPS Patch to a File"
3. Load the clean ROM
4. Load the `.ups` patch file
5. Save as a new `.gba` file

> ✅ Always test the patched ROM on a PC emulator (e.g. mGBA or VBA-M) before using on EZ-Flash

---

## 🔁 How to Verify a Clean ROM

You can verify a clean ROM by comparing it against a No-Intro database.

- Use [Hashtab](https://implbits.com/products/hashtab/) or [QuickHash](https://sourceforge.net/projects/quickhash/)
- Match the CRC32, SHA1, or MD5 to known dumps from No-Intro
- FireRed v1.0 CRC32: `84EE4776`

---

## 🗂️ Organizing Patched ROMs

After patching, you can:
- Place `.gba` files in `/GBA/`
- Rename the file for clarity (e.g. `Pokemon Odyssey v4.gba`) (Make it simplier if save issues occurs)
- Avoid symbols and long names
- Delete leftover `.ips` or `.ups` files from your microSD

> ⚠️ Do not rename `.sav` or `.cht` files manually — let the kernel handle them or use [Online Converter](https://savefileconverter.com/#/mister)

---

## ❌ Avoid These Mistakes
- 🚫 Using v1.1 FireRed for v1.0 hacks
- 🚫 Applying patches to already-patched ROMs
- 🚫 Using zipped or 7z ROM files (must be extracted)
- 🚫 Trying to patch inside a mobile file manager app

---

## 🧠 Final Tips
- 🔁 Always backup your original ROM before patching
- 🎮 Test ROMs on emulators before using them on hardware
- 🧪 Reapply patches if you're unsure — it's safer than guessing

---

📁 Return to: [Troubleshooting Guide](https://github.com/ChimeraGaming/GBA-EZ-Flash-2025-Guide/tree/main/Troubleshooting)

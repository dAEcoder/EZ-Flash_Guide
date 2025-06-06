# 🛠️ Troubleshooting Guide

This section covers common problems with EZ-Flash devices and how to avoid or resolve them. Whether you're having save issues, broken ROMs, cheat bugs, or boot problems — this guide helps you get back on track.

---

## ❓ ROM Doesn't Show Up

**Causes:**
- Unsupported extension (`.gba`, `.gb`, `.gbc`, `.nes` supported)
- ROM is too deeply nested
- Corrupted or misnamed ROM file

**Fix:**
- Place ROMs directly in `/GBA/`, `/GB/`, etc.
- Keep folder paths short
- Remove special characters in filenames
- Ensure your ROM is clean — see [ROM Patching Guide](https://github.com/ChimeraGaming/GBA-EZ-Flash-2025-Guide/blob/main/Troubleshooting.md#-rom-dumping--patching-best-practices)

---

## 💾 Save File Not Working or Keeps Resetting

**Causes:**
- Save wasn't committed (non-FRAM models)
- Save type mismatch
- Rev B board issues with dual-bank saves (e.g., Pokémon)

**Fix:**
- Save **twice** before exiting (especially Pokémon)
- Always return to the kernel menu before powering off
- Check `/SAVER/` for `.sav` file
- Learn more in the [Save Behavior Guide](https://github.com/ChimeraGaming/GBA-EZ-Flash-2025-Guide/blob/main/Save.md)

---

## ⚠️ Pokémon: “Save is Corrupted” Message

**Why this happens:**
- Pokémon uses 128KB Flash with dual save slots. If one is skipped, it flags corruption.

**Fix:**
- Save **twice**
- Return to the menu after saving
- Delete or restore `.sav` if fully corrupted

---

## 🔁 Game Boots Then Instantly Reboots

**Causes:**
- Invalid patch or ROM mismatch
- Incompatible file format
- Header/save issues

**Fix:**
- Use [GBATA](https://www.romhacking.net/utilities/601/) to clean headers
- Verify CRC32 before patching
- Repatch from a clean dump

---

## 🧱 Omega Freezes on Boot / Game Won’t Start

**Causes:**
- Bad kernel or microSD format
- Corrupted theme files

**Fix:**
- Reformat SD (FAT32 or exFAT, 32KB clusters)
- Reinstall kernel from [ezflash.cn](https://www.ezflash.cn/download)
- Revert to default theme if using a custom one

---

## 🎮 Controls Lag / Menu Is Glitchy

**Causes:**
- Theme bug
- Region-locked ROM or unsupported feature

**Fix:**
- Use default theme
- Try a clean US ROM
- Update your kernel version

---

## 🧩 Cheat Menu Doesn’t Show Up

**Causes:**
- Cheat support is **disabled by default**
- Missing or mismatched `CHEAT.DB`
- Incorrect ROM title in cheat database

**Fix:**
- Enable cheats in the cart menu:  
  → `Start` ➝ `Options` ➝ **Cheat Support = On**
- Place `CHEAT.DB` in `/CHEAT/`
- Rename ROM to match the name in the DB
- Convert custom codes using the [Cheat Guide](https://github.com/ChimeraGaming/GBA-EZ-Flash-2025-Guide/blob/main/Cheats.md)

---

## ❄️ Game Freezes or Glitches After Starting With Cheats

**Cause:**
- Incorrect, malformed, or incompatible cheat codes

**Fix:**
- Only use **RAM write** codes
- Never use raw GameShark/Codebreaker codes without converting
- See how to convert properly:  
  [Cheat Code Conversion Guide](https://github.com/ChimeraGaming/GBA-EZ-Flash-2025-Guide/blob/main/Cheats.md)

---

## 📦 ROM Dumping & Patching Best Practices

Bad ROMs and pre-patched files are the #1 cause of game issues.

### ✅ Tips:

- Always patch your **own** clean ROMs
- Verify ROMs with [No-Intro](https://datomatic.no-intro.org/) sets or CRC32
- Never trust random “pre-patched” files

### 🧰 Tools:

| Patch Type | Tool |
|------------|------|
| IPS | [Lunar IPS](https://www.romhacking.net/utilities/240/) |
| UPS | [NUPS](https://www.romhacking.net/utilities/606/), [Tsukuyomi](https://www.romhacking.net/utilities/519/) |
| Online | [ROM Patcher JS](https://www.marcrobledo.com/RomPatcher.js/) |
| Utilities | [GBATA](https://www.romhacking.net/utilities/601/), [Hashtab](https://implbits.com/products/hashtab/) |

### ✔ Check Before You Play:

- ✅ File ends in `.gba`
- ✅ ROM size looks normal (e.g. ~16MB for FireRed)
- ✅ Boot to title screen works
- ✅ Save file appears in `/SAVER/`

---

## 📤 Still Need Help?

Open an [Issue on GitHub](https://github.com/ChimeraGaming/GBA-EZ-Flash-2025-Guide/issues/new) and include:

- Your cart model and revision (e.g., Omega DE Rev B)
- Game name and region
- Kernel version
- Steps you’ve tried
- Any `.sav` or `.cht` issues you can replicate

---

🧠 Following these best practices will prevent 90% of common issues with EZ-Flash devices.

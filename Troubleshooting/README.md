# 🛠️ Troubleshooting Guide

This section covers common problems with EZ-Flash Omega Definitive Edition and how to fix or avoid them. Whether you're dealing with missing ROMs, save corruption, boot errors, or cheat issues — this guide has you covered.

---

## ❓ ROM Doesn’t Show Up

**Possible Causes:**
- Wrong file extension (`.gba`, `.gb`, `.gbc`, `.nes` supported)
- ROM placed too deep in folders
- Special characters in filename
- Corrupted or incompatible ROM file

**Fixes:**
- Place ROMs in `/GBA/`, `/GB/`, etc.
- Use short folder names and paths
- Remove symbols or odd characters in filenames
- Use a verified clean ROM — see [ROM Dumping & Patching](#-rom-dumping--patching-best-practices)

---

## 💾 Save File Not Working or Keeps Resetting

**Causes:**
- Didn’t return to menu before powering off
- Save type mismatch
- Dual-save games like Pokémon not handled properly

**Fixes:**
- Save twice in-game before exiting
- Always return to the EZ-Flash menu before turning off
- Check for a `.sav` file in `/SAVER/`
- More help: [Save Behavior Guide](../Docs/Save.md)

---

## ⚠️ Pokémon: “Save is Corrupted” Message

**Why it happens:**  
Pokémon games use 128KB Flash with dual-slot redundancy. If one slot isn’t updated, it flags as “corrupt.”

**Fix:**
- Save **twice** before quitting
- Exit to the kernel menu
- If it persists, delete and re-create the `.sav` file

---

## 🔁 Game Boots Then Instantly Reboots

**Causes:**
- Bad patch or ROM mismatch
- Incorrect file format
- Save type issues

**Fixes:**
- Use [GBATA](https://www.romhacking.net/utilities/601/) to clean headers
- Verify ROM hashes before patching
- Repatch using a known clean ROM

---

## ⚪ Game Loads to White Screen

**Causes:**
- FireRed v1.1 used instead of v1.0 (common with ROM hacks)
- Corrupt or mismatched `.sav` or `.cht` files
- SD card improperly formatted
- Cheats causing crashes
- Outdated kernel or broken theme

**Fixes:**
- Use **FireRed v1.0** for ROM hacks
- Delete `.sav` and `.cht` — let the cart regenerate them
- Format SD as **FAT32, 64KB allocation**
- Disable cheats before loading
- Update to latest kernel: [ezflash.cn](https://www.ezflash.cn/download)
- Patch hacks using [NUPS](https://www.romhacking.net/utilities/606/)

> 💡 Always save twice and return to the menu before powering off — especially in Pokémon games.

---

## 🧱 Cart Freezes on Boot / Game Won’t Start

**Causes:**
- Corrupted theme
- Broken SD format or kernel

**Fixes:**
- Format SD card (FAT32, 32K/64K cluster)
- Reinstall the kernel from [ezflash.cn](https://www.ezflash.cn/download)
- Use the default `.skn` theme

---

## 🎮 Controls Lag / Menu Glitches

**Causes:**
- Corrupt or buggy custom theme
- Region-incompatible ROMs

**Fixes:**
- Switch back to the default theme
- Try a verified US-region ROM
- Update to the latest kernel

---

## 🧩 Cheat Menu Doesn’t Show Up

**Causes:**
- Cheats disabled in settings
- `CHEAT.DB` missing or doesn’t match ROM

**Fixes:**
- Enable cheats:  
  → Press `Start` ➝ `Options` ➝ Toggle **Cheat Support = On**
- Place `CHEAT.DB` in `/CHEAT/`
- Rename ROM to match DB entry
- See: [Cheat Guide](../Tutorials/Cheats.md)

---

## ❄️ Game Freezes or Crashes When Cheats Are On

**Cause:**  
Malformed or incompatible cheat codes — especially AR/GameShark codes not converted correctly.

**Fix:**
- Only use properly converted RAM-based codes
- Avoid unconverted Codebreaker/GS codes
- Guide: [Cheat Code Conversion](../Tutorials/Cheats.md)

---

## 📦 ROM Dumping & Patching Best Practices

Bad ROMs are the #1 cause of weird errors, glitches, and white screens.

### ✅ Checklist Before You Play

- File ends in `.gba`
- ROM size makes sense (e.g., ~16MB for FireRed)
- Boots to title screen
- Creates a `.sav` in `/SAVER/`

### 🧰 Recommended Tools

| Task        | Tool |
|-------------|------|
| IPS Patch   | [Lunar IPS](https://www.romhacking.net/utilities/240/) |
| UPS Patch   | [NUPS](https://www.romhacking.net/utilities/606/), [Tsukuyomi](https://www.romhacking.net/utilities/519/) |
| Online Patch| [ROM Patcher JS](https://www.marcrobledo.com/RomPatcher.js/) |
| Header Fix  | [GBATA](https://www.romhacking.net/utilities/601/) |
| Hash Check  | [Hashtab](https://implbits.com/products/hashtab/) |

---

## 📤 Still Need Help?

Open an issue on GitHub:  
https://github.com/ChimeraGaming/GBA-EZ-Flash-2025-Guide/issues/new

Include:
- Cart model and revision (e.g., Omega DE Rev B)
- Game name + region
- Kernel version
- What you've tried already
- `.sav` or `.cht` issues (if relevant)

---

🧠 Following these tips prevents **90% of issues** with EZ-Flash carts. Always start with clean ROMs, proper formatting, and verified patches.

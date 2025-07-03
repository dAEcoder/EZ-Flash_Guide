# 🛠️ EZ-Flash Omega (and DE) Setup Guide

The **EZ-Flash Omega** and **Omega Definitive Edition (DE)** are powerful GBA flashcarts capable of running **GBA**, **GB**, **GBC**, and **NES** ROMs. They replace older models like the **EZ-Flash IV** and **Reform** with faster load times, more stable saves, and extra features like themes, cheats, and real-time clock (RTC).

This guide walks you through setup, installation, and optional features like theming and save editing.

---

## 📦 What You'll Need

- ✅ **EZ-Flash Omega** or **Omega DE**  
- 💾 **microSD card** (4–128 GB recommended)  
- 🔌 **microSD card reader** (included with most official kits)  
- 🧠 Latest kernel firmware from [ezflash.cn](https://www.ezflash.cn)  
- 🎨 (Optional) Themes in `.skn` format  
- 🧬 (Optional) `CHEAT.DB` for cheats  
- 🖼️ (Optional) `/IMGS/` thumbnails pack

---

## 🧩 Optional: Swapping the Shell

Omega carts come with:
- A **standard shell** for GBA/GBA SP  
- A **low-profile shell** for DS Lite (flush-fit for Slot-2)

### 🔄 Swap Instructions:
1. Lay the cart face-down.
2. Remove the single screw with a small Phillips driver.
3. Carefully swap the board into the alternate shell.
4. Align the screw post and microSD slot.
5. Reinsert the screw to secure the new case.

---

## 💽 Format the microSD Card

| Format | Card Size         | Recommended? | Notes |
|--------|-------------------|--------------|-------|
| FAT32  | 4–32 GB            | ✅ Yes        | Native support; stable |
| FAT32  | 64–128 GB          | ✅ Yes        | Use [GUIFormat](https://guiformat.com/) to format |
| exFAT  | 64–256 GB+         | ⚠️ Risky      | May cause save errors; not officially supported |
| NTFS   | Any                | ❌ No         | Not recognized by EZ-Flash |
| FAT16  | 2 GB or less       | ⚠️ Limited    | Works, but not recommended |

🔧 Prefer **FAT32** with **64K allocation unit size** for best performance.

---

## 🚀 Installing Firmware & Game Files

1. Download the latest kernel from [ezflash.cn](https://www.ezflash.cn/download).
2. Extract the `.zip` using [7-Zip](https://www.7-zip.org) or WinRAR.
3. Copy these to the **root** of the microSD card:
   - `ezkernelnew.bin` (Omega DE) or `ezkernel.bin` (Classic Omega)
   - `/CHEAT/` folder (optional)
   - `/IMGS/` thumbnails (optional)
4. Add your ROMs to folders like:
   - `/GBA/` – for GBA ROMs
   - `/GB/` and `/GBC/` – for GB/GBC games
   - `/NES/` – for NES ROMs

---

## 🔄 Updating Firmware

1. Insert the microSD card into your EZ-Flash cart.
2. Insert the cart into your handheld.
3. **Hold the RIGHT shoulder button (R)** while powering on.
4. The update runs automatically if needed.

> ⚠️ Don’t power off during kernel updates. Plug into a charger for safety.

---

## 🎨 (Optional) Install a Theme

1. Create `/THEMES/` on the microSD card.
2. Drop in any `.skn` file or a theme folder.
3. On boot, **hold SELECT** → go to `Theme` → choose your theme.

🪄 You can also rename a `.skn` to `default.skn` to auto-load it.

For custom theme creation, check:  
📘 [Creating Themes.md](https://github.com/ChimeraGaming/EZ-Flash_Guide/blob/main/Tutorials/Creating_Themes.md)

---

## 💾 Saving Correctly

- Save **twice** in-game, waiting 3–5 seconds each time
- Press **L+R+A+Select** or return to the kernel menu
- Wait for **“Saving... Do not power off”**
- After that, you can safely turn off the console
- Then remove the SD card and manage `.sav` files on PC

For advanced edits:  
🧬 [Editing Save Files.md](https://github.com/ChimeraGaming/EZ-Flash_Guide/blob/main/Tutorials/Editing_Save_Files.md)

---

## 🧪 Want More Features?

- Cheats: [Cheats.md](../Tutorials/Cheats.md)
- Themes: [Theme Files.md](https://github.com/ChimeraGaming/EZ-Flash_Guide/blob/main/Docs/Theme_Files.md)

---

✅ That’s it! You’re ready to start playing, customizing, and exploring what the Omega can do.

Need help? Open a [GitHub Issue](../../issues) and we’ll try to get it resolved.

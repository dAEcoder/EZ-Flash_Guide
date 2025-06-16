# 🛠️ EZ Flash Omega Setup Guide

The **EZ Flash Omega** is the latest update in the EZ-Flash line of Game Boy Advance flashcarts, capable of playing **GBA**, **GB**, **GBC**, and **NES ROMs**. It replaces the now-discontinued **EZ-Flash IV** and **EZ-Flash Reform** models.

This guide walks you through **setup**, **installation**, and **use** of the flashcart, as well as **optional features** like cheats and thumbnails.

---

## 📦 What You'll Need

- ✅ **EZ-Flash Omega** — [Buy from ezflashomega.com](https://www.ezflashomega.com)
- 💾 **microSD card** (up to 128GB supported)
- 🔌 **microSD card reader/writer** (included with official Omega kits)
- 🧠 **Firmware kernel files** (download from [EZ Flash site](https://www.ezflash.cn))
- 🎮 (Optional) Cheats Library
- 🖼️ (Optional) Thumbnails Pack

---

## 🧩 Choosing Your Cartridge Case (Optional)

Each EZ Flash Omega comes with:
- A **full-size shell** for GBA/GBA SP
- A **slim shell** for DS Lite (fits flush in Slot-2)

### 🔄 How to Swap the Shell
1. Place the Omega cartridge **face down** on a hard surface.
2. Remove the **single screw** from the back with a small Phillips screwdriver.
3. Take off the shell and move the circuit board into the alternate shell.
4. Align the new shell properly (watch the microSD slot alignment).
5. Reinstall the screw to secure the new case.

---

## 💽 Setting Up the microSD Card

| Format Type | SD Card Size        | Notes                                                                 |
|-------------|---------------------|-----------------------------------------------------------------------|
| FAT32       | ✅ Up to 32GB        | Native support in Windows. Most stable format for EZ-Flash carts.     |
| FAT32       | ✅ 64GB – 256GB+     | Requires tools like GUIFormat. Use 64K allocation size for best results. |
| exFAT       | ⚠️ 64GB – 1TB        | May boot but prone to save/load errors. Not officially supported.     |
| NTFS        | ❌ Any size          | Not recognized by EZ-Flash firmware. Do **not** use.                  |
| FAT16       | ⚠️ 2GB or less       | Very old format. Can be used, but not recommended. Limited capacity.  |

🔧 Use your OS’s formatting tool or [SD Card Formatter](https://www.sdcard.org/downloads/formatter/).

---

## 🚀 Installing Firmware & Game Files

1. **Download** the latest kernel from the [EZ Flash Omega downloads page](https://www.ezflash.cn/download).
2. **Extract** the contents using [7-Zip](https://www.7-zip.org) or WinRAR.
3. **Copy** the firmware kernel files directly to the root of the microSD card.
4. (Optional) Add:
   - `CHEAT.DB` for cheats
   - `IMGS` folder for thumbnails
5. Organize your ROMs into folders (e.g. `GBA/`, `GB/`, `NES/`) for easier navigation.

---

## 🕹️ Loading the Flashcart

1. Insert the prepared **microSD card** into the EZ Flash Omega.
2. Insert the Omega into your **GBA**, **DS**, or **DS Lite**.
3. Power on the device.

---

## 🔄 Updating Firmware

1. Insert the microSD card into the EZ Flash Omega.
2. Insert the Omega into your console.
3. **Hold the RIGHT shoulder button** while powering on the system.
4. (Optional) Plug into a power source to prevent interruption.

> The update will begin automatically if a newer kernel is detected.

---

✅ You're now ready to enjoy games, cheats, and custom features with your EZ Flash Omega!

Need help? Open an issue on [GitHub Issues](../../issues), and if we solve it, it'll be added to this guide!

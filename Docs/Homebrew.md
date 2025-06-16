# 🎮 Homebrew on EZ-Flash

EZ-Flash cartridges such as the Omega and Omega DE fully support `.gba` homebrew files — including indie games, emulators, and utilities. This page explains how to use them.

---

## 🧩 What is Homebrew?

Homebrew refers to unofficial software created by independent developers. For the Game Boy Advance (GBA), this includes:

- 🎮 Custom games
- 🧰 Utility tools (e.g., save managers)
- 🕹️ Emulators for older systems (NES, GB, etc.)
- 🎨 Tech demos and experiments

---

## 📂 How to Use Homebrew on EZ-Flash

1. **Download a `.gba` Homebrew File**  
   Example: [PocketNES](https://github.com/pinobatch/pocketnes)

2. **Copy to microSD**  
   Place the file anywhere on your SD card. Suggested directory:
   ```
   Root/Homebrew/PocketNES.gba
   ```

3. **Insert & Launch**
   - Insert the microSD into your EZ-Flash cartridge
   - Boot your GBA and navigate to the file using the EZ-Flash browser
   - Press `A` to launch the homebrew

4. **Saving (if supported)**
   - Most homebrew doesn't require saving
   - If it does, EZ-Flash will usually auto-create a `.sav` file
   - For apps that don’t support SRAM saving natively, use [GBATA](https://www.romhacking.net/utilities/601/) to apply an SRAM patch

---

## 🧠 Tips

- Use **clean `.gba` builds** directly from the developer or trusted sites
- **Do not use IPS/UPS patches** unless instructed to
- Most homebrew does **not require a specific save type**, but if something doesn’t save, try patching it
- Avoid homebrew meant for other platforms like Atari ST or OpenDingux — they will not run on GBA hardware

---

## 📦 Example GBA Homebrews

| Name              | Type         | Link |
|-------------------|--------------|------|
| PocketNES         | NES Emulator | [GitHub](https://github.com/pinobatch/pocketnes) |
| Meteo             | Puzzle Game  | [GameBrew](https://www.gamebrew.org/wiki/Meteo_Avi-2-GBA) |
| GB Video Player  | Video Tool   | [GitHub](https://github.com/LIJI32/GBVideoPlayer) |

## Looking for more?

> Browse [Romhacking.net’s Homebrew section](https://www.romhacking.net/homebrew/) for vetted GBA-compatible projects.
> Browse [Gamebrew's GBA Section] https://www.gamebrew.org/wiki/Main_Page)

---

## 🗣️ Support

If you run into issues or want to suggest homebrew for this list, [open an issue](https://github.com/ChimeraGaming/GBA-EZ-Flash-2025-Guide/issues) or start a discussion!

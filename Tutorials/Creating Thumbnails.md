# 🖼️ Creating Thumbnails for Omega DE

This guide walks you through creating and using **game thumbnails** on your EZ-Flash Omega Definitive Edition.

---

## 🧠 What Are Thumbnails?

Thumbnails are `.bmp` images that appear beside your ROMs in the game browser. They make your flashcart look like a modern game menu.

---

## 📏 Thumbnail Requirements

| Property     | Value                        |
|--------------|------------------------------|
| File Format  | `.bmp` (bitmap)              |
| Dimensions   | **120x80 pixels**            |
| Color Depth  | **24-bit (RGB)**             |
| File Name    | Must match the **4-letter Game ID** (e.g., `BPRE.bmp`) |
| Folder       | Stored inside `/IMGS/` subfolders based on Game ID |

---

## 🆔 Finding or Making a 4-Letter Game ID

The **Game ID** is what the EZ-Flash kernel uses to match thumbnails. For official games, you can extract this code from the ROM header. For ROM hacks, you can **create your own custom ID** using **RHEA**.

### 🔍 Official ROMs

Use [GBATA](https://www.romhacking.net/utilities/601/) or [RHEA](https://www.romhacking.net/utilities/542/) to find the **Game Code** (4-letter serial) from your ROM.

Example:
- FireRed v1.0 → `BPRE`
- Metroid Fusion → `AMTE`

### 🛠️ ROM Hacks: Custom Game IDs with RHEA

Use [RHEA](https://github.com/sterophonick/rhea) to assign a custom Game Code:

> ⚠️ **RHEA Folder Bug Warning**  
> If multiple `.gba` files are in the same folder, RHEA may rename all of them to match the first ROM’s Game ID.  
> **To avoid this:**
> - Place each `.gba` file in its own folder before opening with RHEA  
>   - Suggested: `/Thumbnails/Needs Formatting/Game Name/GameName.gba`  
> - Change folders **between games** if doing multiple edits  
> - **Close and reopen RHEA after each ROM**  
> - After renaming, move each `.gba` into a clean `/Formatted/` folder to help with next steps.

---

## 🛠 Recommended Tools

- [EZ Omega Thumbmaker](https://gbatemp.net/threads/creating-your-own-thumbnails-for-the-ez-flash-omega-firmware.510210/) – Auto-format images  
- [Paint.NET](https://www.getpaint.net/) or [GIMP](https://www.gimp.org/) – Manual BMP editing  
- [RHEA](https://www.romhacking.net/utilities/542/) – View and edit ROM Game IDs  
- [GBATA](https://www.romhacking.net/utilities/601/) – Legacy tool to inspect ROMs

---

## 🔧 Auto Method (Thumbmaker)

1. Open **EZ Omega Thumbmaker**
2. Load an image (cover art or screenshot)
3. It resizes to 120×80 BMP automatically
4. Rename the BMP to the Game ID (e.g., `ODYS.bmp`)
5. Place it in the proper `/IMGS/` subfolder (see next section)

---

## 📁 Final File & Folder Structure

Once your thumbnail is complete:

- ✅ The filename must be `XXXX.bmp` where `XXXX` is the 4-letter Game ID (all caps)
- ✅ It must be placed into a **folder path based on its serial**, like so:

```
/IMGS/B/P/BPRE.bmp    ← for Game ID BPRE  
/IMGS/O/D/ODYS.bmp    ← for Game ID ODYS  
/IMGS/U/N/UNBD.bmp    ← for Game ID UNBD
```

> 📂 If the folders don't exist, **create them manually**. All folder names and file names must be **UPPERCASE**.

---

## ✅ Example Setup Table

| Game Title           | Game Code | ROM File               | Thumbnail Path         |
|----------------------|-----------|------------------------|------------------------|
| Pokémon FireRed      | `BPRE`    | `Pokemon_FireRed.gba`  | `/IMGS/B/P/BPRE.bmp`   |
| Pokémon Unbound      | `UNBD`    | `Pokemon_Unbound.gba`  | `/IMGS/U/N/UNBD.bmp`   |
| Pokémon Odyssey      | `ODYS`    | `Pokemon_Odyssey.gba`  | `/IMGS/O/D/ODYS.bmp`   |

---

📁 Return to: [Tutorials Index](https://github.com/ChimeraGaming/GBA-EZ-Flash-2025-Guide/tree/main/Troubleshooting)

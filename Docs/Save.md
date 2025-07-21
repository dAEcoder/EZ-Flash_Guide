# EZ-Flash Versions & Save Behavior Comparison

EZ-Flash carts handle **SAV (save file) behavior** differently based on the model, hardware revision, and save type used by the ROM (e.g., 128KB Flash, EEPROM, etc.). This section breaks it all down — pairing similar carts and identifying known quirks with save handling.

---

## Save Types in GBA Games

Different GBA games use different save technologies:

| Save Type   | Typical Use                          | Save File Size |
|-------------|--------------------------------------|----------------|
| SRAM        | Early/indie GBA games                | 32KB           |
| EEPROM      | Some Nintendo-published titles       | 512B – 8KB     |
| Flash 64K   | Many standard GBA games              | 64KB           |
| Flash 128K  | Pokémon, Boktai, Golden Sun, etc.    | 128KB          |
| FRAM        | Used only in newer flashcarts (e.g., Omega DE) | Varies |

**Note:** Flash 128K is the most complex and important to know — Pokémon uses two save slots inside that space (primary + backup), which can cause issues if not handled properly.

---

## SD Card Format Types & Compatibility

| Format Type | SD Card Size        | Notes                                                                 |
|-------------|---------------------|-----------------------------------------------------------------------|
| FAT32       | Up to 32GB          | Native support in Windows. Most stable format for EZ-Flash carts.     |
| FAT32       | 64GB – 256GB+       | Requires tools like GUIFormat. Use 64K allocation size for best results. |
| exFAT       | 64GB – 1TB          | May boot but prone to save/load errors. Not officially supported.     |
| NTFS        | Any size            | Not recognized by EZ-Flash firmware. Do not use.                      |
| FAT16       | 2GB or less         | Very old format. Can be used, but not recommended. Limited capacity.  |

Use your OS’s formatting tool or [SD Card Formatter](https://www.sdcard.org/downloads/formatter/).

---

## EZ-Flash Versions & How They Handle Saves

### EZ-Flash Advance
- Built-in NOR flash.
- Save transferred manually via USB linker on PC.
- No microSD; requires external software.

### EZ-Flash IV / Reform
- PSRAM → SD flow.
- Save is not committed to SD until reboot or soft reset.
- If powered off after saving, progress may be lost.
- Struggles with some 128K save games without patches.

### EZ-Flash Omega
- Saves are held in temporary RAM and committed to SD:
  - On soft reset,
  - On reboot,
  - Or when returning to the menu.
- 128K saves supported, but still follow safe shutdown habits.

### EZ-Flash Omega DE

**Rev A**
- FRAM allows instant in-game saving.
- Reliable with Pokémon and dual-save systems.

**Rev B**
- FRAM chip behaves differently.
- Save corruption can occur in 128K save games unless:
  - You save twice in-game.
  - Or return to the menu to trigger backup.

---

## Other Models

- **EZ-Flash 3in1**: No automatic backup; requires manual save dumping via DS tools.
- **EZ-Flash Junior**: SRAM → SD only on reboot/menu return. Powering off too quickly can lose data.

---

## What Happens W

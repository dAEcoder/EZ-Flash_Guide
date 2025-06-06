---
📂 Directory Structure
---

💡 **Tip:** The folder structure of your microSD card can affect how games are detected and how save files are handled by the EZ Flash Omega. While themes may allow for slightly different layouts, the general rule is:  
**Keep it simple and shallow.** The deeper your folder structure, the more likely it is that games won’t load properly or saves may not function as expected.

---

### ❌ Bad Example (Too Deep)

```
Root > Roms > GBA > Pokemon > Completed > Game.gba
```

- Looks organized, but will often **fail to load saves properly**.
- The EZ Flash Omega sometimes can’t handle deep paths or special characters in folder names.

---

### ✅ Good Example (Shallow & Reliable)

```
Root > Game.gba
```

or

```
Root > GBA > Game.gba
```

- Clean and simple.
- Keeps save files working reliably.
- Works with all themes and firmware versions.
  
🧠 Keep it tidy, and your Omega will thank you!

---

### 🗂️ Normal EZ Flash Omega Tree (Auto-generated Structure)

This is the typical layout created by the firmware after the first boot and saving a game, with manually added game folders, cheat database, and IMGS folder.

Folders appear in **alphabetical order** regardless of how you create them.

```
/
├── EZKERNEL.BIN
├── CHEAT/                # Optional: Used for Cheat Database
│   ├── Chn/              # Chinese (Can be Removed)
│   ├── Eng/              # English (Most of us will be using this)
│   ├── GameID2Cht.bin    # This is what reads the Chn & Eng Folders, You can open this VSCode to match Software Title to Game 
│   └── Game.cht          # Custom Cheat Must Match Game Name Exactly and be placed in Cheat Root Folder not Sub Folders.
├── GBA/
│   ├── Game1.gba
│   └── Game2.gba
├── GB/
│   └── Game.gb
├── GBC/
│   └── Game.gbc
├── IMGS/         # Optional: Used for thumbnails or theme UI assets
├── NES/
│   └── Game.nes
└── SAVER/        # Auto-created after first game save

```

---

### 🎨 Simple Database Tree (Used by Themes like Simple DE Dark)

This structure is used when themes are built to rely on `SYSTEM` and `PLUG` folders — common in more advanced or customized themes. Be sure to follow any specific instructions that come with the theme you’re using.

```
/
├── EZKERNEL.BIN
├── GBA/
│   └── Game.gba
├── SYSTEM/
│   ├── CHEAT/
│   │   └── CHEAT.DB
│   ├── IMGS/       # Theme graphics or thumbnails
│   ├── PATCH/      # IPS patches (optional)
│   ├── PLUG/       # Plugin scripts or theme assets
│   ├── RTS/        # Real-time save states
│   └── SAVER/      # Game save files
```

📝 **Notes:**
- `SYSTEM/` is common with Simple/Advanced themes, but not all kernels support it.
- Some themes may require you to move IMGS or PLUG folders into `SYSTEM/`.
- Always follow the README or post instructions from the theme author.

---

✅ When in doubt, use the recommended structure and adjust only as instructed by the theme you’re using. Back up your SD card before making structural changes.

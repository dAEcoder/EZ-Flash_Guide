# 🎨 Creating Themes for EZ-Flash Omega DE

The EZ-Flash Omega Definitive Edition supports full UI customization using `.skn` themes. This guide — based directly on Sterophonick’s official “How to Skin Simple” tutorial — walks you through designing, packaging, and applying your own theme.

---

## 🧰 What You’ll Need

- An **EZ-Flash Omega Definitive Edition** (themes are **not supported** on the original Omega)
- A pixel-art-friendly image editor (GIMP, Photoshop, Paint.NET, etc.)
- Python 3 (to use the provided theme compiler)
- An SD card with your Omega DE’s `EZFLASH/` folder

---

## 🛠 Tools & References

### 📘 Skinning Guide
- **How to Skin Simple – by Sterophonick**  
  https://atapi.space/site/projects/atlantis/howtoskinsimple/  
  > The definitive resource for creating `.skn` themes. Includes structure, color formatting, and Python tools.

### 🎶 Bonus – Maxmod (Not for themes)
- **Maxmod** – A sound engine for GBA/DS homebrew  
  https://maxmod.org/  
  > ⚠️ Maxmod is **not used for theming**, but is a great tool if you're building custom GBA homebrew. Be aware of its RAM demands on real hardware.

---

## 📁 Theme File Structure

A `.skn` theme is a compiled archive containing multiple indexed PNG files:

| File                  | Purpose                                 |
|-----------------------|-----------------------------------------|
| `mainmenu.png`        | Main menu background (256×192px)        |
| `font.png`            | Bitmap font sheet (optional)            |
| `rom_icon.png`        | ROM file icon                           |
| `folder_icon.png`     | Folder icon                             |
| `battery_icons.png`   | Battery charge level display            |
| `cheat_icon.png`      | Cheat availability indicator            |
| `bookmark_icon.png`   | Bookmark status indicator               |
| `keypad_icon.png`     | On-screen button icon                   |
| `helpbox.png`         | Instruction/help window background      |

All images must be **8-bit indexed PNGs** to compile properly.

---

## 🖌️ Build Your Theme (Step-by-Step)

### 1. Get the Skin Template

Download the folder structure and build script from the [How to Skin Simple](https://atapi.space/site/projects/atlantis/howtoskinsimple/) page.

---

### 2. Edit the Assets

Use your image editor to redesign the individual files. Maintain original image dimensions unless you understand the UI constraints.

💡 *Use palette-based 8-bit PNGs. 24-bit or full-RGB PNGs will not compile or may break visuals.*

---

### 3. Compile the `.skn` File

Using the Python script provided:

```bash
python build-skin.py my-theme-folder
```

This will validate your asset names and output a `.skn` file.

---

### 4. Install on SD Card

Place the `.skn` file into:

```
EZFLASH/
├── THEMES/
│   └── your-theme.skn
```

You can have multiple `.skn` files in this folder.

---

### 5. Apply the Theme

- Boot your EZ-Flash Omega DE  
- Hold **SELECT** to enter the system menu  
- Navigate to **Themes** and pick your `.skn` file  

✅ **The kernel will remember your selected theme**, and it will stay active across reboots.  
You don’t need to reapply it every time.

> 💡 Want a theme to load by default on a clean setup? Rename it to `default.skn`.

---

## 🧩 Tips for Better Themes

- Use high contrast for readability on small screens  
- Stick to a consistent pixel grid — it helps with clarity  
- Avoid overly busy or dark backgrounds  
- Test early on hardware to catch issues with color or spacing

---

📁 Return to Tutorials: [Tutorials README](./README.md)

# 🎨 Theme Files for EZ-Flash Omega Definitive Edition

This guide explains how to use, edit, and install custom themes (`.skn` files) for the **EZ-Flash Omega Definitive Edition** (Omega DE). These themes modify the appearance of the flashcart’s UI.

---

## 📁 Directory Structure

Themes must follow this folder path on your microSD card:

```
/THEMES/
    YourThemeName/
        theme.skn
        icon.bmp
        bg.bmp
        font.bmp
```

> ⚠️ **Case-sensitive on some systems.** Make sure file and folder names are uppercase as shown if your cart doesn’t detect the theme.

---

## 📦 Required Files

| File        | Description                               | Format      | Required |
|-------------|-------------------------------------------|-------------|----------|
| `theme.skn` | Compiled skin file                        | Binary `.skn` | ✅ Yes   |
| `icon.bmp`  | Top-left icon (usually cart logo)         | 16-bit BMP | ⚠️ Yes (if referenced in `.skn`) |
| `bg.bmp`    | Background image                          | 16-bit BMP | ✅ Yes   |
| `font.bmp`  | Bitmap font sheet                         | 16-bit BMP | ✅ Yes   |

---

## 🧰 Tools for Editing

- [SKN Editor (by EZ-Flash)](https://www.ezflash.cn/themeEditor/) — Official skin creation tool
- [GIMP](https://www.gimp.org/) / Photoshop — For editing `.bmp` assets
- [IrfanView](https://www.irfanview.com/) — For quick BMP conversion

> 💡 When saving BMPs, ensure they're in **16-bit (RGB565)** format. Many tools default to 24-bit, which will not load.

---

## 🎯 Best Practices

- Keep image dimensions exact (e.g., `bg.bmp` must match kernel resolution)
- Use dark fonts on light backgrounds or vice versa for readability
- Avoid spaces or special characters in folder names
- Test your theme with different ROM names to ensure legibility

---

## 🧪 Advanced Customization

- `.skn` files can store layout, transparency, cursor position, etc.
- Some community tools allow unpacking `.skn` to tweak values directly
- You can use themed kernels to apply global skin styles

---

## 📤 Where to Get Themes

- [EZ-Flash Forum Skin Section](https://bbs.ezflash.cn/forum-52-1.html)
- [GBATemp Skins Thread](https://gbatemp.net/threads/ez-flash-omega-definitive-edition-skin-thread.574149/)
- Custom themes also shared via Reddit and Discord

---

## 📚 Related Docs

- [Setup Guide](https://github.com/ChimeraGaming/EZ-Flash_Guide/blob/main/Docs/Setup.md)
- [Save Behavior](https://github.com/ChimeraGaming/EZ-Flash_Guide/blob/main/Docs/Save.md)
- [Creating Themes Tutorial](https://github.com/ChimeraGaming/EZ-Flash_Guide/blob/main/Tutorials/Creating_Themes.md)

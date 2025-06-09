## 🕒 RTC Retention Issues
### 🧩 Problem Overview

Some users experience **RTC (Real-Time Clock)** issues when transferring `.sav` files between authentic Pokémon cartridges, the EZ Flash Omega DE (EZFODE), R4 cards, and emulators like mGBA. Common symptoms include:

- Berries not growing
- Daily events not triggering
- Clock-based events stuck or desynced

This happens when the RTC in `.sav` files becomes inaccurate or unsynchronized.

---

### ✅ Solutions to Keep RTC Accurate

#### 1. 🕹️ **Use mGBA to Adjust RTC**

- Load your `.sav` and `.gba` file in **mGBA**.
- Let the game run for a few seconds to resync with real-world time.
- Save in-game and export the `.sav`.
- Move the updated `.sav` to your EZFODE `/SAVER/` folder or root, depending on your setup.

> ✅ Best for syncing real-time events (e.g. berries, tides, clocks).

---

#### 2. 🛠️ **Edit Time-Based Events Using PKHeX**

- Load the `.sav` in **PKHeX**.
- PKHeX won’t fix the RTC directly but lets you view and adjust time-sensitive flags and data (e.g. mystery gift timers, daycare, events).
- Save the file and re-export.

> 🧠 Use if in-game timers are broken but you need a quick fix.

---

#### 3. 💾 **Flash ROMs to NOR Mode on EZFODE**

- In EZFODE, press `SELECT` on your Pokémon ROM and choose **Write to NOR Clean**.
- This makes the game persistently loaded with better RTC stability between boots.
- Ensure your `.sav` file has the **exact same name** as the `.gba` file.

> 🧩 Recommended for Gen III Pokémon games to preserve RTC properly.

---

#### 4. ⚠️ **Avoid Using GB Operator for RTC Save Transfers**

- The **Epilogue GB Operator** (even in beta) does not retain RTC precisely.
- Any delay between dumping and restoring causes clock drift.
- It’s great for backups, but not reliable for syncing real-time saves.

> 🕓 Not suitable for maintaining accurate RTC.

---

#### 5. 🔋 **Replace Cartridge Battery for Authentic RTC**

- If using original carts, a dead CR2025 or CR1616 battery means no RTC.
- Replace battery, then use tools (e.g. R4 RTC fixer) to resync clock.

> 🧪 Works only on real hardware, not flash carts.

---

### 🧠 Summary Table

| Task                          | Tool        | Purpose                          |
|-------------------------------|-------------|----------------------------------|
| Fix/Sync RTC in `.sav`        | `mGBA`      | Real-time synchronization        |
| Edit time-based save data     | `PKHeX`     | Fix flags, events, timers        |
| Retain RTC across sessions    | `EZFODE NOR`| Persistent game + save pairing   |
| Avoid inaccurate clock reads  | `GB Operator` | Not RTC-safe yet (beta)         |
| Hardware RTC retention        | Real Cart   | Replace battery + fix RTC        |

---

### 📌 Tip:

Always keep `.gba` and `.sav` filenames identical, and store them in shallow folders like:

```
/GBA/YourGame.gba  
/SAVER/YourGame.sav
```

This improves save detection and RTC compatibility.


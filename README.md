<p align="right">
  <a href="./README.md"><img src="https://img.shields.io/badge/Language-EN-B91C1C?style=for-the-badge" alt="English" /></a>
  <a href="./README.ru.md"><img src="https://img.shields.io/badge/Перевод-RU-18080F?style=for-the-badge" alt="Русский" /></a>
</p>

<p align="center">
  <img src="./assets/phrolova-banner.svg" alt="Nyah Banner" width="100%" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Printer-Bambu_Lab-B91C1C?style=for-the-badge&logo=bambulab&logoColor=FFF1F2" alt="Bambu Lab" />
  <img src="https://img.shields.io/badge/ESP32_%2F_BLE_%2F_WS2812B-18080F?style=for-the-badge&logo=espressif&logoColor=FB7185" alt="ESP32" />
  <img src="https://img.shields.io/badge/C%2B%2B_%2F_Arduino-7F1D1D?style=for-the-badge&logo=cplusplus&logoColor=FFF1F2" alt="C++" />
  <img src="https://img.shields.io/badge/Discord-c.lappland-2A0B15?style=for-the-badge&logo=discord&logoColor=FDA4AF" alt="Discord: c.lappland" />
</p>

<p align="center">
  <img src="./assets/crimson-divider.svg" alt="Divider" width="90%" />
</p>

<p align="center">
  <img src="./assets/phrolova.jpg" alt="Phrolova" width="740" />
</p>

<p align="center">
  <img src="./assets/crimson-divider.svg" alt="Divider" width="90%" />
</p>

### ◆ About

Hey, I'm **Nyah**. I make 3D-printed cosplay weapons and wire them up with ESP32s and LEDs.

I print mostly on a **Bambu Lab** (using **eSUN Transparent PETG** for glowing blade edges and regular PETG for cases) and write my own C++ firmware for the lights. Everything here is stuff I actually built and tested, plus a few guides I wrote down along the way.

- **Done:** Endministrator's Sword (*Arknights: Endfield*, LED + BLE) and Rossi's Sword (*Arknights: Endfield*, simple non-LED print)
- **Working on:** Hoshimi Miyabi's Katana (*ZZZ*) with WS2812B + MPU6500 + Hall sensor in the scabbard, and Frostmourne
- **Control:** all my lit props connect to one ESP32 CYD remote (or just a phone over BLE)
- **Discord:** `c.lappland`

<p align="center">
  <img src="./assets/crimson-divider.svg" alt="Divider" width="90%" />
</p>

### ◆ One Remote for Everything

All my LED props use the same BLE UART protocol, so one CYD remote (or any BLE terminal app on a phone) can control all of them:

```text
  [ ESP32 CYD Remote ]  or  [ Phone (BLE) ]
                   │
                   ▼
     ┌─────────────┼─────────────┐
     ▼             ▼             ▼
Endmin's Sword  Miyabi Katana   Next builds
(ESP32-C3 PWM)  (WS2812B+IMU)   (same BLE)
```

<p align="center">
  <img src="./assets/crimson-divider.svg" alt="Divider" width="90%" />
</p>

### ◆ Repositories

| Repo | Tech | What's in it |
| :--- | :--- | :--- |
| [**cyd-cosplay-remote**](https://github.com/Nyahhentai/cyd-cosplay-remote) | `ESP32` `ESP32-C3` `BLE` | Firmware for the CYD touchscreen remote (12 FX, up to 3 props) + the ESP32-C3 MOSFET dimmer inside the sword. |
| [**cosplay-craft-tutorials**](https://github.com/Nyahhentai/cosplay-craft-tutorials) | `Electronics` `C++` `3D Print` | Guides on prop soldering/batteries, ESP32/Arduino code, and sanding/painting 3D prints. |
| [**cosplay-prop-builds**](https://github.com/Nyahhentai/cosplay-prop-builds) | `Builds` `Photos` | Photos, wiring notes, and WIP progress for Endmin's Sword, Rossi's Sword, Miyabi's Katana, and Frostmourne. |

<p align="center">
  <img src="./assets/crimson-divider.svg" alt="Divider" width="90%" />
</p>

### ◆ Builds

<table>
  <tr>
    <td align="center" width="50%">
      <img src="./assets/cyd-remote-demo.jpg" alt="CYD Remote and Endministrator's Sword" height="260" /><br/>
      <strong>CYD Remote + Endmin's Sword</strong><br/>
      <sub>Arknights: Endfield · BLE brightness, FX &amp; battery</sub>
    </td>
    <td align="center" width="50%">
      <img src="./assets/led-blade-full.jpg" alt="Endministrator's Sword" height="260" /><br/>
      <strong>Endministrator's Sword</strong><br/>
      <sub>Bambu Lab + eSUN Transparent PETG edge</sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="50%">
      <img src="./assets/rossi-sword.jpg" alt="Rossi's Sword" height="260" /><br/>
      <strong>Rossi's Sword</strong><br/>
      <sub>Arknights: Endfield · simple 3D print, no LEDs</sub>
    </td>
    <td align="center" width="50%">
      <img src="./assets/frostmourne.jpg" alt="Frostmourne WIP" height="260" /><br/>
      <strong>Frostmourne (WIP)</strong><br/>
      <sub>World of Warcraft · still working on sanding &amp; paint</sub>
    </td>
  </tr>
</table>

<p align="center">
  <img src="./assets/crimson-divider.svg" alt="Divider" width="90%" />
</p>

### ◆ Progress

| Build | From | Progress | Notes |
| :--- | :--- | :---: | :--- |
| **Endministrator's Sword** | *Arknights: Endfield* | `██████████` 100% | ESP32-C3, IRLB8721, eSUN Transparent PETG, CYD BLE |
| **Rossi's Sword** | *Arknights: Endfield* | `██████████` 100% | Bambu Lab multi-part print |
| **Miyabi's Katana (Tailless)** | *Zenless Zone Zero* | `█████░░░░░` 50% | ESP32-C3 (60 FPS), WS2812B 60 LEDs, MPU6500, 49E Hall, 18650 |
| **Frostmourne** | *World of Warcraft* | `██████░░░░` 60% | Printed, finishing seams &amp; paint |

<p align="center">
  <img src="./assets/crimson-divider.svg" alt="Divider" width="90%" />
</p>

### ◆ Stuff I Use

<p align="center">
  <img src="https://img.shields.io/badge/Bambu_Lab-18080F?style=flat-square&logo=bambulab&logoColor=FB7185" />
  <img src="https://img.shields.io/badge/eSUN_Transparent_PETG-18080F?style=flat-square&logoColor=FB7185" />
  <img src="https://img.shields.io/badge/ESP32--2432S028R_(CYD)-18080F?style=flat-square&logo=espressif&logoColor=FB7185" />
  <img src="https://img.shields.io/badge/ESP32--C3_SuperMini-18080F?style=flat-square&logo=espressif&logoColor=FB7185" />
  <img src="https://img.shields.io/badge/WS2812B_%2F_MPU6500_%2F_49E-18080F?style=flat-square&logoColor=FB7185" />
  <img src="https://img.shields.io/badge/LovyanGFX_%26_BLE-18080F?style=flat-square&logo=bluetooth&logoColor=FB7185" />
  <img src="https://img.shields.io/badge/C%2B%2B_%2F_Blender_%2F_Unity-18080F?style=flat-square&logo=cplusplus&logoColor=FB7185" />
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Nyahhentai&show_icons=true&bg_color=0D090E&border_color=9F1239&title_color=FB7185&icon_color=E11D48&text_color=E2D5DB&hide_rank=false" height="165" alt="GitHub Stats" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Nyahhentai&layout=compact&bg_color=0D090E&border_color=9F1239&title_color=FB7185&text_color=E2D5DB" height="165" alt="Top Languages" />
</p>

<br/>

<!-- 4E 79 61 68 // c.lappland -->

<details>
  <summary align="center">◆ <em>[ don't click ]</em> ◆</summary>
  <br/>

```cpp
// "Silence says more than code ever could."
class Nyah {
public:
  const char* firstRepo = "just-calc-on-c- (im just start lol)";
  const char* now       = "glowing swords & esp32 stuff";
  const char* discord   = "c.lappland";
};
```

  <p align="center">
    <sub>Where it all started: <a href="https://github.com/Nyahhentai/just-calc-on-c-"><strong>just-calc-on-c-</strong></a> 🧮</sub>
  </p>

  <details>
    <summary align="center"><sub>◆ <em>[ ok fine, one more ]</em> ◆</sub></summary>
    <br/>

```text
times i forgot heat-shrink before soldering : too many
boost converters used in miyabi's katana    : 0
remaining battery after sanding frostmourne : 3.72 V (18%)
FX_TOUCH_GRASS                              : TODO
```

    <p align="center">
      <sub>send <code>0x4E594148</code> in discord <code>c.lappland</code> if you actually read this far</sub>
    </p>
  </details>
</details>

<p align="center">
  <img src="./assets/crimson-divider.svg" alt="Divider" width="90%" />
</p>

<p align="center">
  <img src="./assets/phrolova-edit.webp" alt="Phrolova loop" width="840" />
</p>

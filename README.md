## Luminosity Windows 11 Theme Pack (Beta)
Early access to the Luminosity updates. They may contain issues and messy code. Luminosity is a theme pack for Windhawk's Windows 11 Styler mods.

# ⚠️ Beta Warning
**This is a Beta release.**
While the themes have been tested, they are not final. Expect issues, unfinished features, and visual inconsistencies. Feedback is appreciated!

Theme JSON is up to date, but README information likely isn't!

**A major update is planned:**
- Better and clearer `README.md`
- Major Taskbar fixes
- Long term - Taskbar v2 with more changes and fixes

However, updates will take a while; I'm not having proper time to work on it, but I'm doing it slowly... (very slowly)


## Credits
<details>
<summary>(click to expand)</summary>

- [WindowGlass](https://github.com/Nathaniel4JC/Windows-11-Taskbar-Styler/tree/main/Themes/WindowGlass) - `{ThemeResource SystemChromeMediumColor}` and a few targets
- [Fluid](https://github.com/ramensoftware/windows-11-start-menu-styling-guide/tree/main/Themes/Fluid) - Right-Click and mouse hovering animations.
</details>



## Installation Guide

<details>
<summary>Content to Install (click to expand)</summary>

To apply the theme, you will need:
- [Windhawk](https://windhawk.net/) (Of course)

### Required Windhawk Mods
**Taskbar**
- [Windows 11 Taskbar Styler](https://windhawk.net/mods/windows-11-taskbar-styler)
  
  **Required for Compact Taskbar**
  - [Taskbar Labels for Windows 11](https://windhawk.net/mods/taskbar-labels)
  - [Taskbar Clock Customization](https://windhawk.net/mods/taskbar-clock-customization)

**Start Menu**
- [Windows 11 Start Menu Styler](https://windhawk.net/mods/windows-11-start-menu-styler)

**Notification / Action Center**
- [Windows 11 Notification Center Styler](https://windhawk.net/mods/windows-11-notification-center-styler)

**File Explerer**
- [Windows 11 File Explorer Styler](https://windhawk.net/mods/windows-11-file-explorer-styler)

**Recommended**
- [Translucent Windows](https://windhawk.net/mods/translucent-windows) (use Mica or MicaAlt)
</details>

---

# Introduction

![demo](demo.png)
![ac](ac.png)

![fe](fe.png)

**Luminosity** is based on Windows's native Acrylic, using the maximum `TintLuminosityOpacity` value as its backdrop and more rounded UI elements.

It's meant to work well on dark windows, with **Mica** or **MicaAlt** backdrops, with or without the **Translucent Windows** mod.

---

## Theme Status
| Component                         | Version   | Status              | Notes                            |
| --------------------------------- | --------- | ------------------- | -------------------------------- |
| **Taskbar**                       | **1.1.1** | 🔧 Work in Progress | Many issues in multiple displays |
| **Start Menu**                    | **0.2.1** | 🔧 Work in Progress | Missing screenshots  |
| **Notification / Control Center** | **0.1.0** | 🔧 Work in Progress | Messy code, missing styles       |
| **File Explorer**                 | **0.1.0** | ⚠️ Heavy WIP        | Messy code, multiple issues      |

---

# 📜 Changelog

<details>
<summary>(Click to expand)</summary>
*All notable changes to this project will be documented in this file.*

This changelog follows **[Keep a Changelog](https://keepachangelog.com/en/1.0.0/)** and uses **Semantic Versioning**.

---

# Planned

### Taskbar
- Virtual Desktops Right-Click menus.

### Start Menu
- Is passing through a complete rewrite, many hovering effects from [Fluid](https://github.com/ramensoftware/windows-11-start-menu-styling-guide/tree/main/Themes/Fluid) are planned to be added here.

### Notification / Action Center
- Attempt to add missing JumpLists menu animations, and maybe remove more separation borders in other areas of the Action Center (Wired Display & Project).

### File Explorer
- Attempt to remove drop shadows and add matching corner radius and borders to more XAML elements.
	- I believe I can't add the Luminosity backdrop.

---

# Theme-Specific Versions

## **Taskbar**

### **[1.1.1] – Current**

**Status:** 🔧 Work in Progress

**Added**

N/A

**Fixed**

- `MultiWindowElement` looking weird on 25h2. (I suppose)

**Known Issues**

* Multiple issues related to multiple displays setups. Version available at [ramensoftware's Repository](https://github.com/ramensoftware/windows-11-taskbar-styling-guide/tree/main/Themes/Luminosity) is more stable.
  I'll try to provide the fixes sometime in May or June.

---

## **Start Menu**

### **[0.2.1] – Current**

**Status:** Work in Progress

**Added**

- Aligned `Windows.UI.Xaml.Controls.TextBlock#NoSuggestionsWithoutSettingsLink` With the Recommended header.

**Known Issues**

* Missing screenshots.
* Some UI elements not themed yet

---

## **Notification / Control Center**

### **[0.1.0] – Current**

**Status:** Work in Progress

**Added**

* Hovering and Right-Click Menu animations

**Known Issues**

* Visual issues in lower screen resolutions.
* Messy code.
* Some UI elements not themed yet.

---

## **File Explorer**

### **[0.1.0] – Current**

**Status:** Heavy Work in Progress

**Added**

* Many styles.

**Known Issues**

* Multiple visual issues.
* Messy code.

---

# Older Versions

## **Taskbar**

### **[1.1.0]**

**Status:** Under Testing

**Added**

May get a final update soon after checking the public's preference for the Virtual Desktops Bar backup backdrop.
https://www.reddit.com/r/Windhawk/comments/1qfdv2y/which_backdrop_do_you_prefer_design_question_for/

- Darker backdrop
- Removed always visible border in elements
- Removed dropshadow

**Fixed**

N/A

### **[0.9.0]**

**Status:** Stable

**Added**

- Custom hovering and Menu animations thanks to [SandTechStuff's Fluid Start Menu theme](https://github.com/ramensoftware/windows-11-start-menu-styling-guide/tree/main/Themes/Fluid).

**Fixed**

- Animation speeds.

---

## **Start Menu**

### **[0.2.0]**

**Status:** Work in Progress

**Added**

- Better organized JSON
- Fixed many vague targets changing multiple other things and breaking them by accident (Couldn't specify all, but issues seems to be gone for me)
- Styles for the previous cleaner look got removed to mitigate overlapping issues with the New Start Menu and lower resolution displays. A separated minimal layout will be available in the future, like I did with the Taskbar.
- Suggestions grid is now aligned with the pinned items
- Overall it should be working better

**Known Issues**

* Missing screenshots.
* Some UI elements not themed yet


### **[0.1.0]**

**Status:** Work in Progress

**Added**

- Moved the main grid up to remove Search Box and typing UI. Only hiding the Search UI elements still keeps the text navigation beam.
- Moved the Recommendation section down.
- Moved the lower icons for overall consistency with the Right Companion (Phone Link).
- Hovering and Menu animations.

**Known Issues**

* Visual issues in lower screen resolutions.
* Messy code.
* Missing screenshots.
* Some UI elements not themed yet



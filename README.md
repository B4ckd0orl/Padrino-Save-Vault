# 👑 Padrino Save Vault (PS5 Savegame Manager)

> **Universal Save Data Backup & Restoration System for PlayStation 5**  
> **Firmware Support:** 3.00 to 13.60 (PS5 Fat, Slim & Pro)  
> **Integration:** Compatible with Payload Manager (etaHEN, Relapse, ItemzFlow & Netcat)

---

## 🌟 Overview

**Padrino Save Vault** is a high-performance standalone payload and application designed to safeguard your entire PlayStation 5 gaming progress directly to an external USB Hard Drive / SSD (`/mnt/usb0` to `/mnt/usb7`).

Whenever a console crashes, panics, or requires a full factory reset, Padrino Save Vault lets you recover and restore every save file, trophy cache, and database entry with zero data loss.

---

## ✨ Features

* 🚀 **Universal Game Support:** Backs up all native PS5 titles (`PPSA`), backwards-compatible PS4 games (`CUSA`), PlayStation Classics (PS1/PS2/PSP), and Homebrew emulators (`RetroArch`).
* 🔑 **Keystone Preservation:** Automatically preserves cryptographic `keystone` signatures to eliminate "Corrupt Save Data" errors upon restoration.
* 🔄 **Smart Account Re-binding:** Injects restored saves directly into the active user profile upon system reinstalls.
* ⚡ **High-Speed Transfer Engine:** 2MB I/O streaming buffers reaching 140+ MB/s over USB 3.2.
* 🎨 **Obsidian & Gold Visual Dashboard:** 1080p cinematic splash loading screen, external drive capacity gauge, and DualSense controller navigation.
* 🔔 **Native Pop-up Notifications:** Real-time on-screen alerts using `sceKernelSendNotificationRequest`.

---

## 📂 Project Structure

```
padrino-save-vault/
├── GUIA_INSTALACION_Y_USO.md    <-- Step-by-step user installation manual
├── README.md                     <-- Technical documentation
├── test_dashboard.py             <-- Local web preview server (port 1455)
├── ui/                           <-- Full graphical dashboard & splash screen
│   ├── index.html
│   ├── style.css
│   ├── app.js
│   └── assets/
│       ├── icon0.png             <-- 512x512 official emblem
│       ├── logo.jpg              <-- High-resolution shield badge
│       └── splash.jpg            <-- 1920x1080 cinematic vault background
└── src/                          <-- C Source engine for PS5 Prospero OS
    ├── main.c                    <-- Entrypoint and execution modes
    ├── vault_engine.c            <-- USB detection, recursive copy & restore engine
    ├── vault_engine.h
    ├── notify.c                  <-- PS5 native on-screen pop-up notifications
    └── notify.h
```

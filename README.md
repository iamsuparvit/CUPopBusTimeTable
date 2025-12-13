# 🚌 CUPopBusTimeTable

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Platform](https://img.shields.io/badge/Platform-iOS%20Shortcuts-blue)](https://support.apple.com/guide/shortcuts/welcome/ios)

A smart, lightweight, and offline-capable **Apple Shortcut** designed to check Chulalongkorn University Pop Bus schedules instantly.

Instead of navigating through large image files, this shortcut utilizes an embedded JSON database to retrieve precise departure times based on the current day and time.

## ✨ Features

- **⚡️ Instant Lookup:** Zero loading time. Uses a local dictionary (JSON) within the shortcut.
- **🧠 Smart Time Detection:**
  - Automatically detects the current hour.
  - **Buffer Logic:** If the current minute is **> 55**, the shortcut automatically fetches the schedule for the *next hour* to ensure you don't miss the bus.
- **📅 Day Awareness:** automatically distinguishes between **Weekdays** and **Saturdays** (and alerts if there is no service on Sundays).
- **📱 Native Experience:** Clean, simple interface using standard iOS alerts.

## 🚀 Installation

1. Ensure you have the **Shortcuts** app installed on your iPhone or iPad.
2. Click the link below to add the shortcut to your library:

   <a href="https://www.icloud.com/shortcuts/11a4ec7047804a119aabc2d55ee05d27"><img src="https://img.shields.io/badge/Download-Add%20to%20Shortcuts-000000?style=for-the-badge&logo=apple&logoColor=white" alt="Download Shortcut"></a>

   **[Or click here for the direct iCloud Link](https://www.icloud.com/shortcuts/11a4ec7047804a119aabc2d55ee05d27)**

## 🛠 How It Works

This project demonstrates how to build efficient shortcuts using data structures rather than complex `If/Else` chains.

1. **Data Storage:** All timetables are stored in a single **JSON Text** block.
2. **Logic Flow:**
   - The shortcut extracts the current day (`EEE`), hour (`HH`), and minute (`mm`).
   - It calculates the target hour (Current Hour + 1 if Minute > 55).
   - It performs a **Dictionary Lookup**: `Bus Line` → `Day Type` → `Hour`.
3. **Display:** The result is parsed and alerted to the user.

## 📋 Supported Lines

- **Line 1:** Sala Phra Kieo - BTS Siam
- **Line 2:** Sala Phra Kieo - BTS National Stadium
- **Line 3:** Sala Phra Kieo - Faculty of Engineering - MBK *(Weekday only)*
- **Line 4:** Sala Phra Kieo - Samyan Mitrtown
- **Line 5:** Rabieng Chamchuri - Sala Phra Kieo *(Weekday only)*

## 📄 License

This project is licensed under the **MIT License**.

## ⚠️ Disclaimer

- This is an unofficial tool created for educational and productivity purposes.
- Timetable data is based on the schedule effective from **04/08/2568 to 30/09/2568**.
- Actual arrival times may vary due to traffic conditions.

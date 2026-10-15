# 📝 Taskly

<p align="center">
  <img src="https://raw.githubusercontent.com/mebsoruhavuzu-boop/taskly/main/docs/screenshots/feature_graphic.png" alt="Taskly Feature Graphic" width="100%">
</p>

<p align="center">
  <strong>Taskly</strong> is a sleek, responsive, and minimalist to-do list application crafted with Flutter, featuring real-time bidirectional cloud synchronization between <strong>Android</strong>, <strong>Linux Desktop</strong>, and the <strong>Web</strong>.
</p>

<p align="center">
  <a href="https://play.google.com/store/apps/details?id=com.note.taskly"><img src="https://img.shields.io/badge/Google_Play-Taskly-green?logo=google-play&style=for-the-badge" alt="Google Play"></a>
  <a href="https://taskly-notes.web.app"><img src="https://img.shields.io/badge/Web_App-Live-orange?logo=firebase&style=for-the-badge" alt="Web App"></a>
  <a href="https://github.com/mebsoruhavuzu-boop/taskly/releases/latest"><img src="https://img.shields.io/github/v/release/mebsoruhavuzu-boop/taskly?style=for-the-badge&logo=github" alt="Latest Release"></a>
</p>

---

## 📱 Screenshots

<p align="center">
  <img src="https://raw.githubusercontent.com/mebsoruhavuzu-boop/taskly/main/docs/screenshots/home_tasks.png" width="30%" alt="Tasks List">
  &nbsp;&nbsp;&nbsp;&nbsp;
  <img src="https://raw.githubusercontent.com/mebsoruhavuzu-boop/taskly/main/docs/screenshots/folders.png" width="30%" alt="Categories & Folders">
  &nbsp;&nbsp;&nbsp;&nbsp;
  <img src="https://raw.githubusercontent.com/mebsoruhavuzu-boop/taskly/main/docs/screenshots/splash.png" width="30%" alt="Splash Screen">
</p>

---

## 🔄 How Cloud Synchronization Works

Taskly is designed around an **Offline-First, Real-Time Sync** architecture:

1. **Sign In With Google:**
   - On **Android**: Tap the account icon in Settings or the drawer and sign in with your Google Account.
   - On **Linux Desktop**: Sign in using your browser via secure loopback OAuth.
   - On **Web**: Visit [taskly-notes.web.app](https://taskly-notes.web.app) and sign in.
2. **Instant Bidirectional Sync:**
   - Any task created, edited, categorized, or marked as completed on your phone instantly reflects on your Linux desktop via **Firebase Realtime SSE (Server-Sent Events)** streams.
   - If you work offline on your laptop during a flight or without Wi-Fi, your changes are queued and automatically merge safely when you reconnect without overwriting newer data.
3. **Data Integrity & Tombstone Deletion:**
   - Deleted tasks are tracked with timestamps to ensure deletions sync across all paired devices cleanly.

---

## ✨ Key Features

- ⚡ **Offline-First Productivity:** Work anywhere, anytime without an active internet connection.
- ⏰ **Due Dates & Deadlines:** Set exact due dates and times with countdown badges.
- 🔔 **Native Notifications:** 
  - Android: Timely reminders and system alerts.
  - Linux: D-Bus desktop notifications and system tray support (minimizes to tray when closed).
- 🏷️ **Tags & Smart Search:** Tag tasks with `#tags` and filter by category or instant search.
- 📋 **Subtasks (Checklists):** Break large tasks into smaller action items with visual completion progress.
- 🎨 **Aesthetic Themes:** Light, Dark, and deep AMOLED Black modes with custom accent colors.
- 📱 **Home Screen Widget:** Android 4x2 interactive home widget showing your pending tasks and quick status.

---

## 🚀 Installation Guide

### 🐧 Linux (Arch Linux / Manjaro / EndeavourOS)

#### Option 1: Using makepkg from source (Recommended)
```bash
git clone https://github.com/mebsoruhavuzu-boop/taskly.git
cd taskly
makepkg -si
```

#### Option 2: Prebuilt Binary Tarball
Download the standalone executable bundle from [GitHub Releases](https://github.com/mebsoruhavuzu-boop/taskly/releases/latest):
```bash
tar -xzf taskly-1.0.9-x86_64.tar.gz
cd taskly-1.0.9-x86_64
./taskly
```

#### Option 3: AUR Package (When registrations reopen)
Once official AUR registration opens, install with any AUR helper:
```bash
yay -S taskly-bin
```

---

### 📱 Android
Install directly from the **Google Play Store**:  
👉 **[Download Taskly on Google Play](https://play.google.com/store/apps/details?id=com.note.taskly)**

---

### 🌐 Web Browser
Open Taskly on any operating system without installing:  
👉 **[Open Web Application](https://taskly-notes.web.app)**

---

## 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

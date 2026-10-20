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
  <a href="https://taskly-notes.web.app/downloads.html">Download Taskly 1.0.13 — Linux / Arch</a>
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

## Taskly 1.0.13 — Linux / Arch Linux

Taskly is a Flutter to-do app with Turkish and English interfaces. Tasks sync across Android, Linux and the web when signed in with the same Google account. Offline changes merge when the app reconnects.

**Current downloads:** [taskly-notes.web.app/downloads.html](https://taskly-notes.web.app/downloads.html)

[Web app](https://taskly-notes.web.app/) · [Google Play](https://play.google.com/store/apps/details?id=com.note.taskly) · [Guide](https://taskly-notes.web.app/guide_taskly.html) · [Privacy](https://taskly-notes.web.app/privacy_taskly.html) · [Account deletion](https://taskly-notes.web.app/delete-account.html)

## Arch Linux installation

This repository provides the PKGBUILD installation recipe. **There is currently no official AUR listing for `taskly-bin`.**

```bash
git clone https://github.com/mebsoruhavuzu-boop/taskly.git
cd taskly
makepkg -si
```

The recipe downloads the versioned Linux archive from Taskly Firebase Hosting, verifies its SHA-256 checksum, and installs the app in `/opt/taskly` with a launcher and desktop entry. GTK 3, libepoxy and the Ayatana AppIndicator runtime are declared as dependencies.

Alternatively, download the ready-built Arch package from the downloads page and install it with:

```bash
sudo pacman -U taskly-bin-1.0.13-1-x86_64.pkg.tar.zst
```

## Other Linux distributions (x86_64)

Download `taskly-1.0.13-x86_64.tar.gz` and compare its checksum with the published `SHA256SUMS`. Extract the complete bundle:

```bash
mkdir -p taskly-1.0.13
tar -xzf taskly-1.0.13-x86_64.tar.gz -C taskly-1.0.13
./taskly-1.0.13/taskly
```

Keep `taskly`, `lib/`, and `data/` together. Install GTK 3 and the Ayatana AppIndicator runtime using your distribution's package manager. Linux reminders require the app to be running; web reminders are not supported.

## 1.0.13 changes

Version 1.0.13 delivers performance enhancements, smoother real-time cloud synchronization between Android, Linux Desktop, and Web, unified release synchronization across all platforms, and essential stability improvements.

The current Linux/Arch binaries are distributed through the downloads page. Older GitHub Releases remain historical artifacts. The Android store version depends on Google Play review and rollout.

## Platform Synchronization Policy / Platform Senkronizasyon Kuralı

Taskly updates are strictly synchronized across all three distribution channels:
1. **Google Play Store:** Official Android app releases (AAB/APK).
2. **Arch Linux:** Built packages (`taskly-bin`) and download archives on Firebase Hosting.
3. **GitHub Repository:** The `PKGBUILD`, `.SRCINFO` recipes and release notes.

Whenever a new release is prepared, version tags, binaries, and build recipes across all three channels must remain in 100% lockstep parity.

## Türkçe kısa bilgi

Güncel Linux ve Arch paketleri yukarıdaki indirme sayfasındadır. Bu depo kurulum tarifini içerir; resmî AUR kaydı değildir. Aynı Google hesabıyla Android, Linux ve web görevleri eşitlenir. Tüm cihazları güncelleyin. Linux hatırlatıcıları uygulama çalışırken kullanılır; web hatırlatıcıları desteklenmez.

Sürüm 1.0.13 ile birlikte performans iyileştirmeleri, Android, Linux Masaüstü ve Web arasında daha akıcı gerçek zamanlı bulut senkronizasyonu, platformlar arası eşzamanlı sürüm uyumu ve daha temiz bir görev yönetimi deneyimi sunulmaktadır.

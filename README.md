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
  <a href="https://taskly-notes.web.app/downloads.html">Download Taskly 1.0.24 — Linux / Arch</a>
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

## Taskly 1.0.24 — Linux / Arch Linux

Taskly is a Flutter to-do app with 10 languages, with English as the default. Tasks sync across Android, Linux and the web when signed in with the same Google account. Offline changes merge when the app reconnects.

**Current downloads:** [taskly-notes.web.app/downloads.html](https://taskly-notes.web.app/downloads.html)

[Web app](https://taskly-notes.web.app/) · [Google Play](https://play.google.com/store/apps/details?id=com.note.taskly) · [Guide](https://taskly-notes.web.app/guide_taskly.html) · [Privacy](https://taskly-notes.web.app/privacy_taskly.html) · [Account deletion](https://taskly-notes.web.app/delete-account.html)

## Arch Linux installation

This repository provides the PKGBUILD installation recipe. **There is currently no official AUR listing for `taskly-bin`.**

```bash
git clone https://github.com/mebsoruhavuzu-boop/taskly.git
cd taskly
makepkg -si
```

The recipe downloads the versioned Linux archive from Taskly Firebase Hosting, verifies its SHA-256 checksum, and installs the app in `/opt/taskly` with a launcher and desktop entry. GTK 3, libepoxy, the Ayatana AppIndicator runtime and libsecret are declared as dependencies.

Alternatively, download the ready-built Arch package from the downloads page and install it with:

```bash
sudo pacman -U taskly-bin-1.0.24-2-x86_64.pkg.tar.zst
```

## Other Linux distributions (x86_64)

Download `taskly-1.0.24-x86_64.tar.gz` and compare its checksum with the published `SHA256SUMS`. Extract the complete bundle:

```bash
mkdir -p taskly-1.0.24
tar -xzf taskly-1.0.24-x86_64.tar.gz -C taskly-1.0.24
./taskly-1.0.24/taskly
```

Keep `taskly`, `lib/`, and `data/` together. Install GTK 3, the Ayatana AppIndicator runtime and libsecret using your distribution's package manager. Linux reminders require the app to be running; web reminders are not supported.

## 1.0.24 changes

- Recurring tasks: daily, weekly or monthly. Completing a recurring task moves its due date to the next occurrence.
- "Snooze 10 min" action on Android reminder notifications.
- Dynamic color (Android 12+) and a centered layout on tablets and wide screens.
- Linux: Google sign-in tokens are now stored in the system keyring via libsecret (new dependency).
- Faster startup; the version shown in Settings now comes from the installed package.
- Linux package 1.0.24-2: launching Taskly again no longer starts a new copy with another tray icon; the running window comes to the front.

The current Linux/Arch binaries are distributed through the downloads page. Older GitHub Releases remain historical artifacts. The Android store version depends on Google Play review and rollout.

## Platform Synchronization Policy / Platform Senkronizasyon Kuralı

Taskly updates are strictly synchronized across all distribution channels:
1. **Google Play Store:** Official Android app releases (AAB/APK) and release notes (TR & EN, ≤500 chars).
2. **Arch Linux:** Built packages (`taskly-bin`), `PKGBUILD`, `.SRCINFO`, and download archives on Firebase Hosting.
3. **GitHub Repository:** `PKGBUILD`, `.SRCINFO`, **`README.md`** (this file — version number, package names, changelog section, and Turkish description must all be updated in the same commit as PKGBUILD/.SRCINFO).
4. **Web Guide & Privacy Policy:** `https://taskly-notes.web.app/guide_taskly.html` and `privacy_taskly.html` — deployed to Firebase Hosting.

Whenever a new release is prepared, version tags, binaries, build recipes, and this README across all channels must remain in **100% lockstep parity**. No channel may be left on a stale version tag.

## Türkçe kısa bilgi

Güncel Linux ve Arch paketleri yukarıdaki indirme sayfasındadır. Bu depo kurulum tarifini içerir; resmî AUR kaydı değildir. Aynı Google hesabıyla Android, Linux ve web görevleri eşitlenir. Tüm cihazları güncelleyin. Linux hatırlatıcıları uygulama çalışırken kullanılır; web hatırlatıcıları desteklenmez.

Sürüm 1.0.24 ile tekrar eden görevler (her gün/hafta/ay), Android bildiriminden 10 dk erteleme ve Android 12+ dinamik renk eklendi; tablet düzeni ve açılış hızı iyileşti. Linux'ta Google oturum belirteçleri artık sistem anahtarlığında (libsecret) saklanır; Arch paketine `libsecret` bağımlılığı eklendi. Linux paketi 1.0.24-2 ile kısayol artık yeni kopya ve tepsi simgesi açmaz, çalışan pencereyi öne getirir. Her sürüm yükseltmesinde bu README, PKGBUILD ve .SRCINFO dosyaları aynı commit'te güncellenir; hiçbir platform eski sürümde bırakılmaz.

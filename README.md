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
  <a href="https://taskly-notes.web.app/downloads.html">Download Taskly 1.0.27 — Linux / Arch</a>
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

## Taskly 1.0.27 — Linux / Arch Linux

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
sudo pacman -U taskly-bin-1.0.27-2-x86_64.pkg.tar.zst
```

## Ubuntu, Debian and Fedora (x86_64)

Download `taskly_1.0.27-2_amd64.deb` or `taskly-1.0.27-2.x86_64.rpm` from the [downloads page](https://taskly-notes.web.app/downloads.html) or this repository's Releases, then install it with your package manager so dependencies are resolved:

```bash
sudo apt install ./taskly_1.0.27-2_amd64.deb      # Ubuntu 24.04+, Debian 13+
sudo dnf install ./taskly-1.0.27-2.x86_64.rpm     # Fedora 39+
```

These packages require glibc 2.38 or newer. Ubuntu 22.04 and Debian 12 are not supported. They are not published in an apt/dnf repository: to update, download the new package and install it the same way.

## Other Linux distributions (x86_64)

Download `taskly-1.0.27-x86_64.tar.gz` and compare its checksum with the published `SHA256SUMS`. Extract the complete bundle:

```bash
mkdir -p taskly-1.0.27
tar -xzf taskly-1.0.27-x86_64.tar.gz -C taskly-1.0.27
./taskly-1.0.27/taskly
```

Keep `taskly`, `lib/`, and `data/` together. Requires glibc 2.38+. Install GTK 3, the Ayatana AppIndicator runtime, libsecret and GStreamer using your distribution's package manager. Linux reminders require the app to be running; web reminders are not supported.

## 1.0.27 changes

- Restoring a backup also removes deleted tasks from the cloud and keeps changes made after the restore.
- Formatting characters (`*`, `_`, `~`) are kept in plain task text; inline formatting survives multi-line bulleted and numbered lists.
- Snoozed alarms use the current sound and "ring until stopped" setting.
- Overlong task, category, subtask and tag fields are flagged before saving or importing.
- Formatting bar (bold, italic, strikethrough, lists): above the keyboard on Android and, since package revision 1.0.27-2, below the text field on Linux and web. Shortcuts: Ctrl+B bold, Ctrl+I italic, Ctrl+Shift+X strikethrough.

The current Linux/Arch binaries are distributed through the downloads page. Older GitHub Releases remain historical artifacts. The Android store version depends on Google Play review and rollout.

## Platform Synchronization Policy / Platform Senkronizasyon Kuralı

Taskly updates are strictly synchronized across all distribution channels:
1. **Google Play Store:** Official Android app releases (AAB/APK) and release notes (TR & EN, ≤500 chars).
2. **Linux (Arch, Ubuntu/Debian, Fedora):** Arch package (`taskly-bin`), DEB and RPM packages built from the same release archive, `PKGBUILD`, `.SRCINFO`, and download archives on Firebase Hosting and GitHub Releases.
3. **GitHub Repository:** `PKGBUILD`, `.SRCINFO`, **`README.md`** (this file — version number, package names, changelog section, and Turkish description must all be updated in the same commit as PKGBUILD/.SRCINFO).
4. **Web Guide & Privacy Policy:** `https://taskly-notes.web.app/guide_taskly.html` and `privacy_taskly.html` — deployed to Firebase Hosting.

Whenever a new release is prepared, version tags, binaries, build recipes, and this README across all channels must remain in **100% lockstep parity**. No channel may be left on a stale version tag.

## Türkçe kısa bilgi

Güncel Linux, Arch, Ubuntu/Debian (.deb) ve Fedora (.rpm) paketleri yukarıdaki indirme sayfasındadır; DEB ve RPM paketleri Ubuntu 24.04+, Debian 13+ ve Fedora 39+ gerektirir. Bu depo kurulum tarifini içerir; resmî AUR kaydı değildir. Aynı Google hesabıyla Android, Linux ve web görevleri eşitlenir. Tüm cihazları güncelleyin. Linux hatırlatıcıları uygulama çalışırken kullanılır; web hatırlatıcıları desteklenmez.

Sürüm 1.0.27 ile yedekten geri yükleme, düz metindeki biçim işaretleri, ertelenen alarm sesi ve görev alanı uzunluk denetimi düzeltildi. 1.0.27-2 paketiyle biçim çubuğu (kalın, italik, üstü çizili, madde ve numaralı liste) Linux ve web'de metin alanının altında da görünür; kısayollar Ctrl+B, Ctrl+I ve Ctrl+Shift+X.

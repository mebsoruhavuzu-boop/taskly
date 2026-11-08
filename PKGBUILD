# Maintainer: Ismail Aslan <ismailaslan7879@gmail.com>
pkgname=taskly-bin
pkgver=1.0.27
pkgrel=2
pkgdesc="Flutter tabanlı, Android ve Linux arasında Google hesaplı çift yönlü görev senkronizasyonu sağlayan yapılacaklar listesi uygulaması"
arch=('x86_64')
url="https://github.com/mebsoruhavuzu-boop/taskly"
license=('MIT')
depends=('gtk3' 'glib2' 'libepoxy' 'libayatana-appindicator' 'libdbusmenu-glib' 'libsecret' 'gstreamer' 'gst-plugins-base-libs' 'gst-plugins-good' 'libglvnd')
provides=('taskly')
conflicts=('taskly')
# Önceden derlenmiş Flutter ELF içeriğini yeniden strip/debug işlemine sokma.
options=('!strip' '!debug')

source=(
  "taskly-${pkgver}-x86_64.tar.gz::https://taskly-notes.web.app/downloads/taskly-${pkgver}-x86_64.tar.gz"
  "taskly.desktop"
  "taskly.png"
)

sha256sums=(
  '8815aa35024097d935a516ca76cfb2aa29680fab47dc681b782d21ec938a5c9d'
  '2ead1fbc4eae60014b82ebbf725eb8c38ab4c034df408f2f6be5911fa36ce13e'
  'a83767f8fdabc7a4fe028d6076473762ef88fd61f7c9064803b3b530137b94cf'
)

package() {
  # Uygulama ikili dosyalarını ve kaynaklarını /opt/taskly altına yükle
  install -d "${pkgdir}/opt/taskly"
  cp -r "${srcdir}/data" "${pkgdir}/opt/taskly/"
  cp -r "${srcdir}/lib" "${pkgdir}/opt/taskly/"
  install -Dm755 "${srcdir}/taskly" "${pkgdir}/opt/taskly/taskly"

  # Sistem geneli çalıştırılabilir symlink oluştur
  install -d "${pkgdir}/usr/bin"
  ln -sf /opt/taskly/taskly "${pkgdir}/usr/bin/taskly"

  # Masaüstü entegrasyonu (.desktop dosyası)
  install -Dm644 "${srcdir}/taskly.desktop" "${pkgdir}/usr/share/applications/taskly.desktop"

  # Uygulama ikonu
  install -Dm644 "${srcdir}/taskly.png" "${pkgdir}/usr/share/icons/hicolor/256x256/apps/taskly.png"
}

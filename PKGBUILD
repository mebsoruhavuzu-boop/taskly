# Maintainer: Ismail Aslan <ismailaslan7879@gmail.com>
pkgname=taskly-bin
pkgver=1.0.9
pkgrel=1
pkgdesc="Flutter tabanlı, Android ve Linux arasında Google hesaplı çift yönlü görev senkronizasyonu sağlayan yapılacaklar listesi uygulaması"
arch=('x86_64')
url="https://github.com/mebsoruhavuzu-boop/taskly"
license=('MIT')
depends=('gtk3' 'glib2' 'libepoxy')
provides=('taskly')
conflicts=('taskly')

source=(
  "taskly-${pkgver}-x86_64.tar.gz::https://github.com/mebsoruhavuzu-boop/taskly/releases/download/v${pkgver}/taskly-${pkgver}-x86_64.tar.gz"
  "taskly.desktop"
  "taskly.png"
)

sha256sums=(
  'df5060cba986f512e7f68c08215a553bd5f41997ba0bba8c224e6462c66512f6'
  'db45e7a93c59b49b06833f19ca75eef01ca055d061d72bfa9810b03db20c2c8c'
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

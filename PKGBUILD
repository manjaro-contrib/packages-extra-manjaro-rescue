# Maintainer: Stefano Capitani <stefano@manjaro.org>

pkgname=manjaro-rescue
pkgver=3.0.0
pkgrel=1
pkgdesc="Professional system restore utility for Manjaro Linux"
arch=('any')
url="https://codeberg.org/Ste74/manjaro-rescue"
license=('GPL-3.0-or-later')
depends=('python' 'python-gobject' 'gtk4' 'libadwaita' 'os-prober' 'grub' 'polkit' 'manjaro-tools-base')
makedepends=('git' 'gettext')
optdepends=('timeshift: System restore utility for Linux'
	    'manjaro-log-helper: Gathers selected system logs and optionally sends them to the internet'
	    'bmenu: Bash scripts providing a collection of terminal applications in a simple UI')
source=("$url/archive/$pkgver.tar.gz")
sha256sums=('95fb2856bad3e390b7b62ac23d589a24602d72da85d282919f34c1a83bb2b9a7')

package() {
  cd "${srcdir}/${pkgname}"

  install -d "${pkgdir}/usr/lib/${pkgname}"
  install -d "${pkgdir}/usr/bin"
  install -d "${pkgdir}/usr/share/applications"
  install -d "${pkgdir}/usr/share/icons/hicolor/scalable/apps"

  cp -r backend utils locale "${pkgdir}/usr/lib/${pkgname}/"
  [ -d icons ] && cp -r icons "${pkgdir}/usr/lib/${pkgname}/"
  install -m755 main.py "${pkgdir}/usr/lib/${pkgname}/"
  install -m644 window.ui "${pkgdir}/usr/lib/${pkgname}/"

  ln -s "/usr/lib/${pkgname}/main.py" "${pkgdir}/usr/bin/${pkgname}"
  ln -s "/usr/lib/${pkgname}/icons/hicolor/scalable/apps/${pkgname}.svg" "${pkgdir}/usr/share/icons/hicolor/scalable/apps/${pkgname}.svg"
  install -m644 "${pkgname}.desktop" "${pkgdir}/usr/share/applications/"
}

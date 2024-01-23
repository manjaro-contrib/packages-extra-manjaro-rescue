# Maintainer: Stefano Capitani <stefanoatmanjarodotorg>

pkgname=manjaro-rescue
pkgver=2.0
pkgrel=1
arch=('any')
license=('GPL-3.0-or-later')
url='https://gitlab.manjaro.org/ste74/manjaro-rescue'
pkgdesc="Restore your installed system"
depends=('zenity' 'mkinitcpio' 'grub' 'os-prober' 'pamac-cli' 'pacman' 'util-linux' 'manjaro-tools-base' 'st'
		'manjaro-log-helper' 'bmenu')
optdepends=('timeshft: System restore utility for Linux')
source=("$url/-/archive/$pkgver/$pkgname-$pkgver.tar.gz")
sha256sums=('2174458dfad2eec5f1752cdb13831d0968d713a0274071cd7adb633d68dcfedc')

package() {
		cp -rf $srcdir/$pkgname-$pkgver/usr $pkgdir/

		chmod 755 $pkgdir/usr/bin/manjaro-rescue
		chmod 755 $pkgdir/usr/share/manjaro/grub-restore/grub-apply-efi
		chmod 755 $pkgdir/usr/share/manjaro/grub-restore/grub-apply-legacy
		chmod 755 $pkgdir/usr/share/manjaro/grub-restore/grub-restore
}


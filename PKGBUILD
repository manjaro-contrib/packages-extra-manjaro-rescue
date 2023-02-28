# Maintainer: Stefano Capitani <stefanoatmanjarodotorg>

pkgname=manjaro-rescue
pkgver=1.0
pkgrel=1
arch=('any')
license=('GPL3')
url='https://gitlab.manjaro.org/ste74/manjaro-rescue'
pkgdesc="Restore your installed system"
depends=('zenity' 'mkinitcpio' 'grub' 'os-prober' 'pamac-cli' 'pacman' 'util-linux' 'manjaro-tools-base' 'st-manjaro'
		'manjaro-log-helper' 'bmenu')
source=("$url/-/archive/$pkgver/$pkgname-$pkgver.tar.gz")
sha256sums=('7f76d6ab29459cce1cc91c5fce794c5ae946cf1299909154f1f90aeac73db06c')

package() {
		cp -rf $srcdir/$pkgname-$pkgver/usr $pkgdir/

		chmod 755 $pkgdir/usr/bin/manjaro-rescue
		chmod 755 $pkgdir/usr/share/manjaro/grub-restore/grub-apply-efi
		chmod 755 $pkgdir/usr/share/manjaro/grub-restore/grub-apply-legacy
		chmod 755 $pkgdir/usr/share/manjaro/grub-restore/grub-restore
}


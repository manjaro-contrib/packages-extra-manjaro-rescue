# Maintainer: Stefano Capitani <stefanoatmanjarodotorg>

pkgname=manjaro-rescue
pkgver=2.1
pkgrel=1
arch=('any')
license=('GPL3')
url='https://gitlab.manjaro.org/ste74/manjaro-rescue'
pkgdesc="Restore your installed system"
depends=('zenity' 'mkinitcpio' 'grub' 'os-prober' 'pamac-cli' 'pacman' 'util-linux' 'manjaro-tools-base' 'st'
		'manjaro-log-helper' 'bmenu')
optdepends=('timeshft: System restore utility for Linux')
source=("$url/-/archive/$pkgver/$pkgname-$pkgver.tar.gz")
sha256sums=('46e6dde1f0c33c3cd486869f58cf26dc6c7c9dc206881b81aaca1f67a0c14e6b')

package() {
		cp -rf $srcdir/$pkgname-$pkgver/usr $pkgdir/

		chmod 755 $pkgdir/usr/bin/manjaro-rescue
		chmod 755 $pkgdir/usr/share/manjaro/grub-restore/grub-apply-efi
		chmod 755 $pkgdir/usr/share/manjaro/grub-restore/grub-apply-legacy
		chmod 755 $pkgdir/usr/share/manjaro/grub-restore/grub-restore
}


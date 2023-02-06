#
# Maintainer: Maarten Bezemer <maarten.bezemer@gmail.com>
#

pkgname=touchpad-toggle
pkgver=0.1.1
pkgrel=1
pkgdesc="Disables touchpad when USB mouse is detected, and enables when unplugged again"
arch=('i686' 'x86_64')
license=('GPL')

depends=('xorg-xinput')
provides=('touchpad-toggle')

source=('touchpad-toggle'
    '70-touchpad-toggle.rules')

sha256sums=('4c0e1836752d972e990c8cffc18a527c9d6991dcd5bf58e52835589dd71bffc2'
    '4d1d1cf5d9be87a83370a1551806b00a01471c037761e5c8dfd4aa75e976fa9e')

package() {
  install -Dm755 "${srcdir}/touchpad-toggle" "$pkgdir/usr/bin/touchpad-toggle"
  install -Dm644 "${srcdir}/70-touchpad-toggle.rules" "$pkgdir/usr/lib/udev/rules.d/70-touchpad-toggle.rules"
}

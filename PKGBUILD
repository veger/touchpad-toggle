#
# Maintainer: Maarten Bezemer <maarten.bezemer@gmail.com>
#

pkgname=touchpad-toggle
pkgver=0.1.4
pkgrel=1
pkgdesc="Disables touchpad when USB mouse is detected, and enables when unplugged again"
arch=('i686' 'x86_64')
license=('GPL')

depends=('xorg-xinput')
provides=('touchpad-toggle')

source=('touchpad-toggle'
    '70-touchpad-toggle.rules')

sha256sums=('2219a93fea213aa8c101263a343405f4a6a7b33eea29067e31af98a54e333044'
    '4d1d1cf5d9be87a83370a1551806b00a01471c037761e5c8dfd4aa75e976fa9e')

package() {
  install -Dm755 "${srcdir}/touchpad-toggle" "$pkgdir/usr/bin/touchpad-toggle"
  install -Dm644 "${srcdir}/70-touchpad-toggle.rules" "$pkgdir/usr/lib/udev/rules.d/70-touchpad-toggle.rules"
}

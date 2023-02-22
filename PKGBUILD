#
# Maintainer: Maarten Bezemer <maarten.bezemer@gmail.com>
#

pkgname=touchpad-toggle
pkgver=0.1.3
pkgrel=1
pkgdesc="Disables touchpad when USB mouse is detected, and enables when unplugged again"
arch=('i686' 'x86_64')
license=('GPL')

depends=('xorg-xinput')
provides=('touchpad-toggle')

source=('touchpad-toggle'
    '70-touchpad-toggle.rules')

sha256sums=('682fda8939acbc0c61acd067340b25721e66d48f935c261627221dbedd8ce1dd'
    '4d1d1cf5d9be87a83370a1551806b00a01471c037761e5c8dfd4aa75e976fa9e')

package() {
  install -Dm755 "${srcdir}/touchpad-toggle" "$pkgdir/usr/bin/touchpad-toggle"
  install -Dm644 "${srcdir}/70-touchpad-toggle.rules" "$pkgdir/usr/lib/udev/rules.d/70-touchpad-toggle.rules"
}

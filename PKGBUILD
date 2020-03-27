# local pkgbuild
# Maintainer: crian <crian84@gmail.com>

pkgname=dmenu-crian-git
pkgver=4.9
pkgrel=1
pkgdesc='A generic menu for X'
arch=('x86_64')
license=('MIT')
depends=('sh' 'libxinerama' 'libxft' 'freetype2')
conflicts=('dmenu')
provides=('dmenu')

build() {
    cd ..
    make
}

package() {
    cd ..
    make PREFIX=/usr DESTDIR="$pkgdir" install
    install -m644 -D LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

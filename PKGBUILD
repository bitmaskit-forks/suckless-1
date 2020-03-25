# local pkgbuild
# Maintainer: crian <crian84@gmail.com>

pkgname=dwm-crian-git
pkgver=6.2
pkgrel=1
pkgdesc='A dynamic window manager for X'
arch=('x86_64')
license=('MIT')
depends=('libx11' 'libxinerama' 'libxft')
conflicts=('dwm')
provides=('dwm')

build() {
    cd ..
    make
}

package() {
    cd ..
    make PREFIX=/usr DESTDIR="$pkgdir" install
    install -m644 -D LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
    install -m644 -D README "$pkgdir/usr/share/doc/$pkgname/README"
    install -m644 -D dwm.desktop "$pkgdir/usr/share/xsessions/dwm.desktop"
}

# local pkgbuild
# Maintainer: crian <crian84@gmail.com>

pkgname=st-crian-git
pkgver=0.8.2
pkgrel=1
pkgdesc='A simple virtual terminal emulator for X'
arch=('x86_64')
license=('MIT')
depends=('libxft')
conflicts=('st')
provides=('st')

build() {
    cd ..
    make
}

package() {
    cd ..
    make PREFIX=/usr DESTDIR="$pkgdir" install
    install -m644 -D LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
    install -m644 -D README "$pkgdir/usr/share/doc/$pkgname/README"
}

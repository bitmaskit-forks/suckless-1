# local pkgbuild
# Maintainer: crian <crian84@gmail.com>

pkgname=tabbed-crian-git
pkgver=0.6
pkgrel=3
pkgdesc='Simple generic tabbed fronted to xembed aware applications'
arch=('x86_64')
license=('MIT')
depends=('libx11')
conflicts=('tabbed')
provides=('tabbed')

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

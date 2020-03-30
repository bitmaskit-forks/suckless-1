# local pkgbuild
# Maintainer: crian <crian84@gmail.com>

pkgname=slock-crian-git
pkgver=1.4
pkgrel=1
pkgdesc='A simple X display locker'
arch=('x86_64')
license=('MIT')
depends=('libxrandr')
conflicts=('slock')
provides=('slock')

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

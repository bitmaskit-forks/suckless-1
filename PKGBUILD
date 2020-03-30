# local pkgbuild
# Maintainer: crian <crian84@gmail.com>

pkgname=dwmblocks
pkgver=r27.9f6c26b
pkgrel=1
pkgdesc='Modular status bar for dwm'
arch=('any')
license=('GPL2')
conflicts=('dwmblocks')
provides=('dwmblocks')

pkgver() {
    cd ..
    printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
    cd ..
    make PREFIX=/usr DESTDIR="$pkgdir" install
    install -m644 -D LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
    install -m644 -D README.md "$pkgdir/usr/share/doc/$pkgname/README"
}

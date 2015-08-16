# Maintainer: Limao Luo <luolimao+AUR@gmail.com>

pkgname=ibus-table-erbi
pkgver=1.2.0.20090901
pkgrel=1
pkgdesc="The Erbi Input Method of tables engines for IBus."
arch=(any)
url=http://code.google.com/p/ibus/
license=(LGPL2.1)
makedepends=(ibus-table)
optdepends=(ibus-table-extraphrase)
provides=($pkgname=$pkgver)
options=(!libtool)
source=(http://ibus.googlecode.com/files/$pkgname-$pkgver.tar.gz)
sha256sums=('102745d9c5545aa5e1e721485ece2ae40640bc4f522bf3e191148cfc6be54d9a')
sha512sums=('495fc9dfbdabd4e30d8f048df0dc31ca66f63ac206c5344b0f385c27c3f24afe83e6a8ba72bfef153e5789190733473a38f8f2869eceb8a28b04b1d44659f7be')

build() {
    cd $pkgname-$pkgver/
    ./autogen.sh --prefix=/usr --libexecdir=/usr/lib/ibus
    make
}

package() {
    make -C $pkgname-$pkgver DESTDIR="$pkgdir" install
}

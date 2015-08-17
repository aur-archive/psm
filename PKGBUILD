# Maintainer: Eivind Uggedal <eivind@uggedal.com>

pkgname=psm
pkgver=0.7
pkgrel=1
pkgdesc="Simple, accurate RAM and swap usage"
arch=('x86_64' 'i686')
url="https://github.com/bpowers/psm"
license=('MIT')
depends=('glibc')
makedepends=('go>=2:1-2' 'asciidoc' 'xmlto')
install=psm.install
source=("https://github.com/bpowers/psm/archive/v${pkgver}.tar.gz")
md5sums=('22236798c2643acaae93ef83362c37d5')

build() {
  cd "$srcdir/$pkgname-$pkgver"

  msg2 "Compiling..."
  go build
}

package() {
  cd "$srcdir/$pkgname-$pkgver"

  make install DESTDIR="$pkgdir"

  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

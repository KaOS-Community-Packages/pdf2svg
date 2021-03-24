pkgname=pdf2svg
pkgver=0.2.3
pkgrel=1
pkgdesc="A simple PDF to SVG converter using the Poppler and Cairo libraries"
url="https://github.com/dawbarton/pdf2svg"
arch=('x86_64')
license=('GPL-2.0')
depends=("poppler" "cairo")
opdepends=() 
source=("https://github.com/dawbarton/pdf2svg/archive/refs/tags/v${pkgver}.tar.gz")
md5sums=("d398b3b1c1979f554596238a44f12123")

prepare() {
  cd pdf2svg-${pkgver}
  ./configure
}

build() {
    cd pdf2svg-${pkgver}
    make -j$(nproc) 
}

package() {
    cd pdf2svg-${pkgver}
    make install DESTDIR=${pkgdir}
}

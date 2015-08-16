# Maintainer : Martin Wimpress <code@flexion.org>
# Contributor: Giovanni "Talorno" Ricciardi <kar98k.sniper@gmail.com>
# Contributor: Xpander <xpander0@gmail.com>

pkgname=mate-file-manager-open-terminal
pkgver=1.6.0
pkgrel=7
pkgdesc="A Caja extension for opening terminals in arbitrary local paths."
url="http://mate-desktop.org/"
arch=('i686' 'x86_64' 'armv6h' 'armv7h')
license=('GPL')
depends=('gtk2' 'mate-desktop' 'mate-file-manager')
makedepends=('mate-common' 'perl-xml-parser')
options=('!emptydirs')
groups=('mate-extra')
source=("http://pub.mate-desktop.org/releases/1.6/${pkgname}-${pkgver}.tar.xz")
sha1sums=('8695ac9d0acbc27173d024340f121cd298aff0b9')
install=${pkgname}.install

build() {
    cd "${srcdir}/${pkgname}-${pkgver}"
    ./autogen.sh \
        --prefix=/usr
    make
}

package() {
    cd "${srcdir}/${pkgname}-${pkgver}"
    make DESTDIR="${pkgdir}" install
}

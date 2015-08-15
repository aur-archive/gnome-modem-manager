# Maintainer: kiv <kiv.apple@gmail.com>
pkgname=gnome-modem-manager
pkgver=20111204
pkgrel=1
pkgdesc="GUI utility for control 3G modem"
url="http://cpu-fun.ru/en/projects/gmm"
arch=('x86_64' 'i686')
license=('GPLv2')
depends=('gtk3' 'modemmanager')
optdepends=()
makedepends=(git vala)
conflicts=()
replaces=()
backup=()
#install='foo.install'
source=()
md5sums=()
 
build() {
	mkdir -p "${srcdir}/${pkgname}-${pkgver}"
	cd "${srcdir}/${pkgname}-${pkgver}"
	rm -rf *
	git clone git://github.com/kiv-apple/Gnome-Modem-Manager.git
	cd ./Gnome-Modem-Manager
	make
}
 
package() {
	cd "${srcdir}/${pkgname}-${pkgver}/Gnome-Modem-Manager"
	make DESTDIR="${pkgdir}" install
}

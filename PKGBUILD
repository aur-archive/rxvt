#Maintainer: Seblu <seblu+arch@seblu.net>
#Contributor: Malte Rabenseifer <malte@zearan.de> 
#Contributor: urist <9362773@gmail.com>
#Contributor: Tom Newsom <Jeepster@gmx.co.uk>
#Contributor: Troy Phillips <9362773@gmail.com>
#Contributor: Judd Vinet <jvinet@zeroflux.org>
pkgname=rxvt
pkgver=2.7.10
pkgrel=4
pkgdesc='A colour vt102 terminal emulator'
arch=('i686' 'x86_64')
url='http://rxvt.sourceforge.net/'
license=('GPL')
depends=('libx11')
makedepends=('libxt')
source=("http://downloads.sourceforge.net/$pkgname/$pkgname-$pkgver.tar.gz")
md5sums=('302c5c455e64047b02d1ef19ff749141')

build() {
	cd $pkgname-$pkgver
	./configure --prefix=/usr
	make
}

package() {
	cd $pkgname-$pkgver
	make prefix="$pkgdir/usr" mandir="$pkgdir/usr/share/man/man1" install
	rm "$pkgdir/usr/bin/$pkgname-$pkgver"
	rmdir "$pkgdir/usr/include"
	rmdir "$pkgdir/usr/lib"
}

# vim:set ts=2 sw=2 ft=sh et:

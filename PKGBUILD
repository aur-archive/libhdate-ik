# Contributor: Jack <nim901@gmail.com>
# Contributor: Ido Kanner <idokan@gmail.com>
pkgname=libhdate-ik
libname=libhdate
pkgver=1.4.20
pkgrel=1
pkgdesc="LibHdate is a small C,C++ library for Hebrew calendar and dates, holidays, and reading sequence"
url="http://libhdate.sourceforge.net/"
license="GPL"
arch=('i686' 'x86_64')
makedepends=("gcc" "autoconf" "automake")
provides=('libhdate')
conflict=('libhdate')
source=(http://downloads.sourceforge.net/project/$libname/$libname/$libname-$pkgver/$libname-$pkgver.tar.bz2)
md5sums=('d6d5e188989127ae05aef2bdd74daa37')

build() {
  cd $startdir/src/$libname-$pkgver
  # We install only the library not the binding features
  ./configure --prefix=/usr --disable-fpc --disable-gpc --disable-python --disable-ruby --disable-php --disable-perl 
  make
  make DESTDIR=$startdir/pkg install
}

# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Philbns <http://boringnerdystuff.wordpress.com>
pkgname=postgis
pkgver=2.0.1
pkgrel=0
pkgdesc="Adds support for geographic objects to PostgreSQL"
arch=('i686' 'x86_64')
url="http://postgis.refractions.net/"
license=('GPL')
depends=('postgresql' 'geos' 'proj' 'gtk2')
source=(http://postgis.refractions.net/download/postgis-$pkgver.tar.gz)
md5sums=('7af9ce5f7dfb22d81fea7f041e674497') #generate with 'makepkg -g'
build() {
  cd "$srcdir/$pkgname-$pkgver"
  ./configure --prefix=/usr --with-gui --with-topology --with-raster
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" install
}

# vim:set ts=2 sw=2 et:

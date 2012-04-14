# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Your Name <youremail@domain.com>
pkgname=postgis
pkgver=2.0.0
pkgrel=1
epoch=
pkgdesc="Adds support for geographic objects to PostgreSQL"
arch=('i686' 'x86_64')
url="http://postgis.refractions.net/"
license=('GPL')
groups=()
depends=('postgresql' 'geos' 'proj' 'gtk2')
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=(http://postgis.refractions.net/download/postgis-$pkgver.tar.gz)
noextract=()
md5sums=('639d2b5d6a7dc94ea2e60d6942a615bc') #generate with 'makepkg -g'
build() {
  cd "$srcdir/$pkgname-$pkgver"
  ./configure --prefix=/usr --with-gui
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" install
}

# vim:set ts=2 sw=2 et:

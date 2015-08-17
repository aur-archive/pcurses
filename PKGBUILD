# Maintainer: schuay <jakob.gruber@gmail.com>

pkgname=pcurses
pkgver=3
pkgrel=1
pkgdesc='A curses package management tool using libalpm'
arch=('x86_64' 'i686')
url="https://github.com/schuay/$pkgname"
license=('GPL')
depends=('ncurses' 'pacman>=4.1.2')
makedepends=('boost' 'cmake' 'git')
source=("git://github.com/schuay/pcurses.git#tag=pcurses-$pkgver")
md5sums=('SKIP')

build() {
  rm -rf "$srcdir/$pkgname-build"
  mkdir "$srcdir/$pkgname-build"
  cd "$srcdir/$pkgname-build"

  cmake -DCMAKE_INSTALL_PREFIX=/usr "$srcdir/$pkgname"
  make
}

package() {
  cd "$srcdir/$pkgname-build"
  make DESTDIR="$pkgdir" install
}

# vim:set ts=2 sw=2 et:

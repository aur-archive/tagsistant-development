# Maintainer: Joshua Stiefer <facedelajunk@gmail.com>

pkgname=tagsistant-development
_pkgname=tagsistant
pkgver=0.6rc4
pkgrel=1
pkgdesc="a semantic (tagging) filesystem"
arch=('i686' 'x86_64')
url="http://www.tagsistant.net/"
license=('GPL')
depends=('fuse' 'libdbi' 'libdbi-drivers' 'sqlite')
optdepends=('libexif: JPEG plugin'
			'taglib: MP3/OGG plugin')
provides=('tagistant')
conflicts=('tagsistant')
options=(!libtool)
install=tagsistant.install
source=("tagsistant-0.6-rc4.tar.gz::http://www.tagsistant.net/download/tagsistant-0-6-rc4/finish/4-tagsistant-0-6/6-tagsistant-0-6-rc4/0")
md5sums=('eba70f23da1c5b7f7cf0471d6ee240aa')

build() {
  cd "$srcdir/$_pkgname-0.6"
  ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/$_pkgname-0.6"
  make DESTDIR="$pkgdir" install
}

# Maintainer: taylorchu <tailinchu [at] gmail [dot] com>

pkgname=qmount
pkgver=20120324
pkgrel=1
pkgdesc='quick mounter'
arch=('any')
url='https://github.com/taylorchu/qmount'
license=('GPL2')
makedepends=('git')
_gitroot="https://github.com/taylorchu/qmount"
_gitname="qmount"
build() {
   cd "$srcdir"
 msg "Connecting to GIT server...."
 if [ -d $_gitname ] ; then
   cd $_gitname && git pull origin
   msg "The local files are updated."
 else
   git clone --depth=1 $_gitroot $_gitname
   cd $_gitname
 fi
 msg "GIT checkout done or server timeout"
 make DESTDIR="$pkgdir" install
}

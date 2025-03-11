_pkgname=slock
pkgname=$_pkgname-git
pkgver=1.5
pkgrel=1
pkgdesc="Simple X display locker"
url='http://tools.suckless.org/slock'
arch=('i686' 'x86_64' 'armv7h')
license=('custom:MIT/X')
depends=('libxrandr')
makedepends=('git')
provides=("$_pkgname")
conflicts=("$_pkgname")
source=('arg.h' 'config.h' 'config.mk' 'explicit_bzero.c' 
	'LICENSE' 'Makefile' 'slock.1' 'slock.c' 'util.h')
md5sums=('SKIP' 'SKIP' 'SKIP' 'SKIP'
	 'SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP')

build() {
  make PREFIX=/usr DESTDIR="$pkgdir"
}

package() {
  make PREFIX=/usr DESTDIR="$pkgdir" install
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

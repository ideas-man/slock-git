_pkgname=slock
pkgname=$_pkgname-git
pkgver=20170325.35633d4
pkgrel=1
pkgdesc="Simple X display locker"
url='http://tools.suckless.org/slock'
arch=('i686' 'x86_64' 'armv7h')
license=('custom:MIT/X')
depends=('libxrandr')
makedepends=('git')
provides=("$_pkgname")
conflicts=("$_pkgname")
source=('arg.h' 'config.h' 'config.mk' 'explicit_bzero.c' 'LICENSE' 'Makefile' 'slock.1' 'slock.c' 'util.h')
md5sums=('088564fdbdbbae55b777dce80abc602f' 'SKIP'
         '775d9f802c899d17498778e8b1d615fe' '4885a6c0db3b9f2fd6c07100fea0fe6e' '41b71f339fba66b45a89418a350ef914'
         '446f07df9345c1bf41e27575407b47cb' 'SKIP' 'SKIP' 'f26ca62b855e6d8e134f2ecdf9f0ca92')

build() {
  make PREFIX=/usr DESTDIR="$pkgdir"
}

package() {
  make PREFIX=/usr DESTDIR="$pkgdir" install
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

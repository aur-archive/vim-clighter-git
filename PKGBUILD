# Maintainer: olantwin <olantwin at gmail dot com>
pkgname=vim-clighter-git
pkgver=r425.59226cd
pkgrel=2
pkgdesc="VIM plugin to improve c-family development environment based on Clang"
arch=(any)
url="https://github.com/bbchung/clighter"
license=('GPL3')
depends=(clang python2)
makedepends=()
install=vimdoc.install
source=("git+https://github.com/bbchung/clighter.git")
sha1sums=('SKIP')

pkgver() {
  cd $srcdir/clighter
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  cd "$srcdir/clighter"
  _installpath="${pkgdir}/usr/share/vim/vimfiles"
  mkdir -p ${_installpath}/{plugin,doc,misc,autoload}
  cp -R autoload/* ${_installpath}/autoload
  cp -R plugin/* ${_installpath}/plugin
  cp -R doc/* ${_installpath}/doc
  cp -R misc/* ${_installpath}/misc
}

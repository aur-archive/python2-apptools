# Maintainer: Andrzej Giniewicz <gginiu@gmail.com>
pkgname=python2-apptools
pkgver=4.1.0
_githubtag=b04f9dd
pkgrel=1
pkgdesc="Application tools"
arch=('any')
url="https://github.com/enthought/apptools"
license=('BSD')
depends=('python2' 'python-configobj' 'python2-traitsui')
makedepends=('python2-distribute')
conflicts=('python-enthought-utils' 'python2-apptools-git' 'python-ets-apptools-svn')
options=(!emptydirs)

source=("https://github.com/enthought/apptools/tarball/${pkgver}")
md5sums=('31e07316f953a499620d818343021728')

build() {
  cd "$srcdir/enthought-apptools-${_githubtag}"

  python2 setup.py build
}

package() {
  cd "$srcdir/enthought-apptools-${_githubtag}"

  python2 setup.py install --root="$pkgdir"/  --optimize=1

  install -D "LICENSE.txt" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}


# Maintainer: Harvey Hunt <harveyhuntnexus@gmail.com>
_pkgname=barney 
pkgname=$_pkgname-git
pkgver=v0.1.r1.gbf43fef
pkgrel=1
pkgdesc="A lightweight XCB based X11 bar that utilises Cairo and Pango"
arch=(any)
url="https://github.com/HarveyHunt/barney"
license=('GPL3')
groups=()
depends=('python2' 'pygtk' 'pycairo-xcb-git' 'xorg-xpyb-git')
makedepends=('git' 'python2-setuptools' )
provides=($_pkgname)
conflicts=($_pkgname)
replaces=()
backup=()
options=(!emptydirs)
install=
source=($_pkgname::git://github.com/HarveyHunt/barney.git)
md5sums=('SKIP')

package() {
  cd "$srcdir/$_pkgname"
  python2 setup.py install --root="$pkgdir/" --optimize=1
}

pkgver() {
    cd "$srcdir/${_pkgname}"
    git describe --tags | sed -E 's/([^-]*-g)/r\1/;s/-/./g'
}

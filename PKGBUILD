# Maintainer: Damian Nowak <damian.nowak@atlashost.eu>

pkgname='nutsh'
pkgdesc='A nutty shell'
pkgver=r58.9532db5
pkgrel=1
epoch=
arch=('i686' 'x86_64')
url='https://github.com/remicmacs/nutsh'
license=('unknown')
groups=()
depends=()
makedepends=('git')
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install="$pkgname.install"
changelog=
source=("$pkgname"::'git+https://github.com/remicmacs/nutsh.git')
noextract=()
sha512sums=('SKIP')
PKGEXT='.pkg.tar.gz'

pkgver() {
  cd "$pkgname"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
  cd ${srcdir}/${pkgname}
  make
}

package() {
  mkdir -p ${pkgdir}/usr/bin
  cd ${srcdir}/${pkgname}
  PKGDIR=${pkgdir} make install
}
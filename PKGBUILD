# Maintainer: specimen-hub

_pkgname=st
pkgname=$_pkgname-git
pkgver=0.8.4
pkgrel=1
pkgdesc="Simple terminal from suckless.org"
url='https://git.suckless.org/st/'
arch=('i686' 'x86_64')
license=('MIT')
depends=('libxft')
makedepends=('ncurses' 'libxext' 'git')
optdepends=('dmenu: feed urls to dmenu')
provides=($_pkgname)
source=('arg.h' 'config.h' 'config.mk' 'LICENSE' 'Makefile'
	'st.1' 'st.c' 'st.h' 'st.info' 'win.h' 
	'x.c')
md5sums=('SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP'
	'SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP'
	'SKIP')

build() {
	make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11
}

package() {
	make PREFIX=/usr DESTDIR="${pkgdir}" install
	install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}

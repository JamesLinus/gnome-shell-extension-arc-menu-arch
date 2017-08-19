# Maintainer: lexruee <a.rueedlinger at gmail.com>
# This PKGBUILD is maintained on GitHub <https://github.com/lexruee/gnome-shell-extension-arc-menu-arch>.

pkgname=gnome-shell-extension-arc-menu-git
pkgver=14
pkgrel=1
pkgdesc="The new applications menu for GNOME 3."
arch=('any')
url="https://github.com/LinxGem33/Arc-Menu"
license=('GPL2')
provides=("${pkgname%-git}")
conflicts=("${pkgname%-git}")
depends=('gnome-shell>=3.18' 'gnome-shell-extensions' 'gnome-tweak-tool')
makedepends=('git')
install='gnome-shell-extension.install'
source=("git+https://github.com/LinxGem33/Arc-Menu")
sha256sums=('SKIP')

pkver() {
	cd $srcdir/Arc-Menu
	echo "$(git rev-list --count master).$(git rev-parse --short HEAD)"
}

build() {
	cd $srcdir/Arc-Menu
	make
}

package() {
	cd $srcdir/Arc-Menu
	make install DESTDIR="$pkgdir/" INSTALL=system
}

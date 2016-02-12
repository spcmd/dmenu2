# Maintainer: Sibren Vasse <arch at sibrenvasse dot nl>
# Maintainer: Michał Lemke <lemke.michal@gmail.com>
# Tab key modification by: spcmd (https://github.com/spcmd)

pkgname=dmenu2
pkgver=0.2
pkgrel=2
pkgdesc="Fork of dmenu with many useful patches applied and additional options like screen select, dim or opacity change"
url="https://bitbucket.org/melek/dmenu2"
arch=('i686' 'x86_64')
license=('MIT')
license=('GPL')
depends=('libxinerama' 'libxft')
provides=(dmenu)
conflicts=(dmenu)

source=(dmenu2-$pkgver.tar.gz)
md5sums=('ce0314b558b4e8692f6a5034af97f8ca')

build() {
	cd "$srcdir/$pkgname-$pkgver"
	make
}

package() {
	cd "$srcdir/$pkgname-$pkgver"
	make DESTDIR="$pkgdir" PREFIX=/usr install
	install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

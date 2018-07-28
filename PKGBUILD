# Maintainer: Christian Heses <mail@eworm.de>
# Contributor: Marti Raudsepp <marti@juffo.org>

pkgname=ssss
pkgver=v0.5.6
pkgrel=1
pkgdesc="Simple command-line implementation of Shamir's Secret Sharing Scheme"
arch=('i686' 'x86_64')
license=('GPL')
url="http://point-at-infinity.org/ssss/"
depends=('gmp')
makedepends=('xmltoman')
source=("ssss::git+https://github.com/alkis05/ssss.git#tag=releases/v${pkgver}")
md5sums=('SKIP')

build() {
	cd ${srcdir}/${pkgname}
	make
}

package() {
	cd ${srcdir}/${pkgname}

	install -D -m0755 ssss-combine ${pkgdir}/usr/bin/ssss-combine
	install -D -m0755 ssss-split ${pkgdir}/usr/bin/ssss-split

	install -D -m0644 ssss.1 ${pkgdir}/usr/share/man/man1/ssss.1

	install -D -m0755 doc.html ${pkgdir}/usr/share/doc/${pkgname}/doc.html
	install -D -m0755 ssss.1.html ${pkgdir}/usr/share/doc/${pkgname}/ssss.1.html
}

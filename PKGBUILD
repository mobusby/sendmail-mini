# Maintainer: Mark Busby <mark .at. BusbyCreations .dot. com>
pkgname=sendmail-mini
pkgver=0.0.2
pkgrel=1
pkgdesc="A very simple shell script to replace sendmail on single-user systems when only local mail is needed (i.e. for crond reports, etc.)."
arch=('any')
url=""
license=('GPL')
groups=()
depends=()
makedepends=()
optdepends=('heirloom-mailx: To read mail')
provides=()
conflicts=(postfix)
replaces=()
backup=()
options=()
install=
changelog=
source=($pkgname-$pkgver.tar.gz)
noextract=()
md5sums=() #generate with 'makepkg -g'

build() {
  cd "$srcdir/$pkgname-$pkgver"

  ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"

  make DESTDIR="$pkgdir/" install
}

install -D -m644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"

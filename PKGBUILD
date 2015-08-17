# Author: Miroslav Rajcic <miroslav.rajcic@inet.hr>
# Maintainer: Douglas McFadzean <mcfadzean.org.uk ta linux>

pkgname=notecase-pro-bin
pkgver=3.8.7
pkgrel=2
pkgdesc='Advanced hierarchical notes manager'
arch=('i686' 'x86_64')
url='http://www.notecasepro.com'
license=('custom:notecase-pro')
depends=('openssl' 'gtksourceview2' 'desktop-file-utils' 'gstreamer0.10-base' 'libunique')
optdepends=('aspell: spell check support')
conflicts=('notecase' 'notecase-pro')
provides=('notecase' 'notecase-pro')
install="$pkgname.install"
source=("${url}/get.php?ub13.10/notecase-pro_${pkgver}_i386.deb")
md5sums=('9e65a52bf648306b06582e7a2f8a5759')

[ "$CARCH" = "x86_64" ] && source=("${url}/get.php?ub13.10/notecase-pro_${pkgver}_amd64.deb")
[ "$CARCH" = "x86_64" ] && md5sums=('cf67e9b526b696be8926dddda204729c')


package() {
  if [ "$CARCH" = "x86_64" ]; then
    ar x notecase-pro_${pkgver}_amd64.deb
  else
    ar x notecase-pro_${pkgver}_i386.deb
  fi
  tar xzf data.tar.gz -C "${pkgdir}/"
}

# Maintainer: pauld <dufresnep@gmail.com>
# Contributor: boenki <boenki at gmx dot de>
# Contributor: Bartek Piotrowski <barthalion@gmail.com>
# Contributor: Arkham <arkham at archlinux dot us> 
# Contributor: Artyom Smirnov <smirnoffjr@gmail.com>

pkgname=flush
pkgver=0.9.12
pkgrel=3
pkgdesc="GTK+ based BitTorrent client"
arch=('i686' 'x86_64')
url="http://sourceforge.net/projects/flush/"
license=('GPL')
#depends=('libconfig' 'libtorrent-rasterbar' 'libglademm' 'libnotify' 'hicolor-icon-theme' 'desktop-file-utils')
depends=(libtorrent-rasterbar libconfig libglademm desktop-file-utils libnotify) #as namecap see them
makedepends=('boost')
install=${pkgname}.install
source=(http://downloads.sourceforge.net/${pkgname}/${pkgname}-${pkgver}.tar.bz2)
md5sums=('6a9a9a218b3f060be899688dc29549ec')

build() {
  cd ${pkgname}-${pkgver}
  ./configure --prefix=/usr
  make
}

package() {
  cd ${pkgname}-${pkgver}
  make DESTDIR=${pkgdir} install
}
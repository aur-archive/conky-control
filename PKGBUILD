# Contributer: giacomogiorgianni@gmail.com 

pkgname=conky-control
pkgver=1.0.0
pkgrel=2
pkgdesc="control panel for conky"
arch=('any')
url="http://bbs.archbang.org/viewtopic.php?id=3017"
license=('GPL')
categories=()
depends=('conky-lua')
makedepends=()
options=(!emptydirs)
source=("Conky_voyager.tar.gz::http://ompldr.org/vZWoxMA" "conky_voyager.tar.gz::http://ompldr.org/vZWoxYg" "conky-control.install")
md5sums=('6930f45eb5dd402953d306ebe8ff14da'
         'e63ba795800ec20df912e620b423688e'
         '0217a6bee07fb918b0c2050548103d43')
install=$pkgname.install

build() {
  mkdir -p $pkgdir/usr/bin
  mkdir -p $pkgdir/usr/share/applications
  mkdir -p $pkgdir/etc/skel/.config
  cp $startdir/conky-controlRC.desktop $pkgdir/etc/skel/.config/
  cp $startdir/conky-control.desktop $pkgdir/usr/share/applications/
    
  install -m 0775 -do $LOGNAME $pkgdir/etc/skel/.scripts
  tar xzf Conky_voyager.tar.gz -C $pkgdir/etc/skel/.scripts
  tar xzf conky_voyager.tar.gz -C $pkgdir/etc/skel//
  ln -s  $pkgdir/etc/skel/.scripts/Conky/conky $pkgdir/usr/bin/conky-control
  }
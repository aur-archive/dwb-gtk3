# Contributor: portix <portix at gmx.net>

pkgname=dwb-gtk3
_pkgrealname=dwb
pkgver=2014.03.07
pkgrel=1
pkgdesc="A webkit web browser with vi-like keyboard shortcuts, stable snapshot" 
url="http://portix.bitbucket.org/dwb/"
arch=('i686' 'x86_64')
license=('GPL')
depends=('webkitgtk' 'desktop-file-utils')
provides=(dwb)
install=dwb.install
conflicts=('dwb-hg' 'dwb-gtk3-hg' 'dwb')
source=(https://bitbucket.org/portix/dwb/downloads/${_pkgrealname}-${pkgver}.tar.gz)
md5sums=('270f17a3b926cae48dff475aa786df22')

build() {
  cd ${srcdir}/${_pkgrealname}-${pkgver}
  make GTK=3
}
package() {
  cd ${srcdir}/${_pkgrealname}-${pkgver}
  make DESTDIR=${pkgdir} install \
    BASHCOMPLETION=/usr/share/bash-completion/completions

}

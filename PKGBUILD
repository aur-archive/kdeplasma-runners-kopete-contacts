# Maintainer: Dan Vratil <dan@progdan.cz>

pkgname=kdeplasma-runners-kopete-contacts
_srcname=krunner-kopete-contacts
pkgver=0.4
pkgrel=2
pkgdesc="A KRunner plugin that allows you to open chat with Kopete contact just by typing it's name"
arch=('i686' 'x86_64')
depends=('kdebase-workspace>=4.3' 'qt4' 'kdenetwork-kopete')
makedepends=('cmake' 'automoc4')
url="http://kde-apps.org/content/show.php?content=105263"
license=('GPL')
source=(http://kde-apps.org/CONTENT/content-files/105263-${_srcname}-${pkgver}.tar.gz)

build()
{
  cd ${srcdir}/
  mkdir build
  cd build
  
  cmake -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix`\
  	-DCMAKE_BUILD_TYPE=Release \
  	 ../${_srcname}-${pkgver}
  make
}

package()
{
  cd ${srcdir}/build
  make DESTDIR=${pkgdir} install
}

md5sums=('cccbf5906ff7e2755233456cfa31091a')

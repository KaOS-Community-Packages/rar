pkgname=rar
pkgver=5.1.1
pkgrel=1
pkgdesc="A command-line port of the rar compression utility"
arch=('x86_64')
url="http://www.rarlab.com"
license=('custom')
depends=('gcc-libs')
backup=('etc/rarfiles.lst')
source=("http://www.rarlab.com/rar/rarlinux-x64-$pkgver.tar.gz")
md5sums=('529000f404e123c790f3a516f06ba6d1')
 
package() {
cd ${srcdir}/rar
install -Dm755 rar ${pkgdir}/usr/bin/rar
install -Dm755 rar_static ${pkgdir}/usr/bin/rar_static
install -Dm755 default.sfx ${pkgdir}/usr/lib/default.sfx
install -Dm644 rarfiles.lst ${pkgdir}/etc/rarfiles.lst
install -Dm644 license.txt ${pkgdir}/usr/share/licenses/${pkgname}/LICENSE
}

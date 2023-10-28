pkgname=rar
pkgver=6.24
_pkgver=624
pkgrel=1
pkgdesc="A command-line port of the rar compression utility"
arch=('x86_64')
url="http://www.rarlab.com"
license=('custom')
depends=('gcc-libs')
backup=('etc/rarfiles.lst')
source=("https://www.rarlab.com/rar/rarlinux-x64-${_pkgver}.tar.gz")
sha256sums=('SKIP')

package() {
    cd ${srcdir}/${pkgname}
    install -dm755 ${pkgdir}/opt/${pkgname}
    install -dm755 ${pkgdir}/usr/bin
    install -dm755 ${pkgdir}/etc
    install -dm755 ${pkgdir}/usr/lib
    install -dm755 ${pkgdir}/usr/share/doc
    install -dm755 ${pkgdir}/usr/share/licenses/${pkgname}
    install -dm755 ${pkgdir}
    install -Dm755 rar -t ${pkgdir}/usr/bin
    install -Dm755 default.sfx -t ${pkgdir}/usr/lib
    install -Dm644 rarfiles.lst -t ${pkgdir}/etc
    install -Dm644 readme.txt ${pkgdir}/usr/share/doc/${pkgname}/README
    install -Dm644 whatsnew.txt ${pkgdir}/usr/share/doc/${pkgname}/ChangeLog
    install -Dm644 rar.txt ${pkgdir}/usr/share/doc/${pkgname}/rar.txt
    install -Dm644 license.txt ${pkgdir}/usr/share/licenses/${pkgname}/LICENSE
    cp -a ${srcdir}/${pkgname}/. ${pkgdir}/opt/${pkgname}
}

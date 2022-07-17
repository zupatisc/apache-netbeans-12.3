# Maintainer: Jonty Newman <jonty.newman at gmail dot com>
# Maintainer: Cleber Matheus <clebermatheus at outlook dot com>
# Contributor: Martynas Janu <martynas.janu at googlemail dot com>
# Contributor: Benjamin Asbach <archlinux-aur.pkgname at impl dot it>
pkgname=apache-netbeans
pkgver=12.3
pkgrel=1
pkgdesc="Apache Netbeans IDE development platform"
arch=('i686' 'x86_64')
url="https://netbeans.apache.org"
license=('Apache')
options=('!strip')
depends=('java-runtime>=8' 'ttf-font')
provides=('apache-netbeans')
conflicts=('apache-netbeans' 'netbeans')
source=("https://archive.apache.org/dist/netbeans/netbeans/${pkgver}/netbeans-${pkgver}-bin.zip"
        "apache-netbeans.desktop")
sha512sums=('d38abd8312010837cffbe9b1c721a1e14a33735b766c09a0b640adf1360c439b3d68df032f420afb6af060e054c92dc07436fb50d33823b8fed996cbd824e39d'
            'e8160bb80c333a6b478766f176092caa8d87394202c923df22a8f4e3a336a72b0c3ee7f724743b13bfdc785fca32c1b984c2f719b0b153f943a9beaa9d877909')

package() {
    mkdir -p $pkgdir/usr/share/apache-netbeans
    mv $srcdir/netbeans $srcdir/apache-netbeans
    cp -R $srcdir/apache-netbeans $pkgdir/usr/share
    chmod -R 0755 $pkgdir/usr/share/apache-netbeans
    chmod +x $pkgdir/usr/share/apache-netbeans/bin/netbeans
    rm -f $pkgdir/usr/share/apache-netbeans/bin/netbeans.exe
    rm -f $pkgdir/usr/share/apache-netbeans/bin/netbeans64.exe
    install -Dm755 apache-netbeans.desktop "${pkgdir}/usr/share/applications/apache-netbeans.desktop"
}

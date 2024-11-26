# Maintainer: elementh <hello@lucasmarino.me>                                     
pkgname=anytype-bin
pkgver=0.43.8
pkgrel=1
pkgdesc="Operating environment for the new internet. Anytype is a next generation software that breaks down barriers between applications, gives back privacy and data ownership to users."
arch=('x86_64')
url="https://anytype.io/"
license=('custom')
depends=('fuse')
options=(!strip !debug)
optdepends=('org.freedesktop.secrets: for not having to sign in each time')
provides=('anytype')
conflicts=('anytype'
           'anytype-legacy')
_appimage="Anytype-${pkgver}.AppImage"
source=(
    "Anytype-${pkgver}.AppImage::https://anytype-release.fra1.cdn.digitaloceanspaces.com/Anytype-${pkgver}.AppImage"
    "anytype.desktop"
    "anytype.png"
    )
noextract=("${_appimage}")
sha256sums=('8a7a89bf1e4afe4f7b5f9d04d05625cc90caaab563014e9928855d0961ebf0d2'
            'fe5e13adc759f7d93382733ba942b2a49f0ec4817a1be95e1ac6e7d1495002db'
            '7967ea7a9c6237f7a3d32a6d352d1ac7b18fc29b329e662141bc21bf89d32939')

package() {
    install -Dm755 $_appimage "$pkgdir"/usr/bin/anytype
    chmod +x "${pkgdir}/usr/bin/anytype"

    install -Dm644 "anytype.desktop"                    "${pkgdir}/usr/share/applications/anytype.desktop"
    install -Dm644 "anytype.png"                        "${pkgdir}/usr/share/icons/hicolor/128x128/apps/anytype.png"
}

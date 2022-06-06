# Maintainer: Jesse Frey <jesse.m.frey@gmail.com>
pkgname=wifi-ap-sw
pkgver=0.1
pkgrel=1
epoch=
pkgdesc="units and scripts to switch between wifi access point and joining a network"
arch=('any')
url=""
license=('GPL')
groups=()
depends=('libgpiod' 'iproute2' 'hostapd' 'netctl')
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=(startup unit)
noextract=()
validpgpkeys=()
sha256sums=('be74f5afb769c9219e7fb6b72ac75d6323550ce888284f138386ea90ae12fe39'
            'b4f6c2f3b6e53a395322b8f9372f541cb44076c1c35b426def3f3503f207bc02')

package() {
    install -dvm 755 ${pkgdir}/usr/lib/systemd/system/ ${pkgdir}/usr/share/${pkgname}/
    #install unit file into system directory
    install -vm 644 unit ${pkgdir}/usr/lib/systemd/system/${pkgname}.service
    #install script into /usr/share
    install -vm 755 startup ${pkgdir}/usr/share/${pkgname}/startup
}

# Maintainer: Caleb Bredekamp
pkgname=csb-zsh-conf-git
_pkgname=csb-zsh-conf
pkgver=v0.0.2.r1.gf991196
pkgrel=1
_destname1="/etc/skel/"
_destname2="/etc/skel/.zsh/"
pkgdesc="Caleb's zsh configuration"
arch=('any')
url="https://github.com/caleb-sb/${_pkgname}.git"
license=('MIT')
depends=('zsh')
makedepends=('git')
replaces=("arcolinux-zsh-git")
provides=("${pkgname}")
conflicts=()
options=(!strip !emptydirs)
source=(${_pkgname}::"git+${url}")
sha256sums=('SKIP')
package() {
	install -dm 755 ${pkgdir}${_destname1}
	install -dm 755 ${pkgdir}${_destname2}
	cp -r ${srcdir}/${_pkgname}/.zsh* ${pkgdir}${_destname1}
	cp -r ${srcdir}/${_pkgname}/zsh-autosuggestions ${pkgdir}${_destname2}
}
pkgver() {
	cd "$_pkgname"
	git describe --long | sed 's/\([^-]*-g\)/r\1/;s/-/./g'
}

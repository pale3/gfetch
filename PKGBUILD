#$Id: PKGBUILD 87389 2013-03-30 14:49:30Z dwallace $ 
# Maintainer: Daniel Wallace <danielwallace at gtmanfred dot com>
# Contributor: portix <portix at gmx.net>

pkgname=gfetch-git
_gitname=gfetch
pkgver=2015.03.07.gdad0c87
pkgrel=1
pkgdesc="Gmail fetcher used for tiling wm" 
url="http://github.com/pale3/gfetch"
arch=('i686' 'x86_64')
provides=('gfetch')
license=('GPL')
depends=('wget')
optdepends=("alsa-utils: play sound on new mail")
source=("git+https://github.com/pale3/gfetch.git")
md5sums=('SKIP')

pkgver() {
  cd "$srcdir"/${_gitname}
  git log -1 --format="%cd.g%h" --date=short | sed 's/-/./g'
}

package() {
	
	cd "${srcdir}"/"${_gitname}"

	mkdir -p "$pkgdir/usr/share/$_gitname"
	mkdir -p "$pkgdir/usr/bin"
  
  cp "$srcdir/${_gitname}/usr/bin/gfetch" "$pkgdir/usr/bin/"
  cp "$srcdir/${_gitname}/usr/share/gfetch/ding.wav" "$pkgdir/usr/share/$_gitname/"
  cp "$srcdir/${_gitname}/usr/share/gfetch/gfetchrc" "$pkgdir/usr/share/$_gitname/"
  
  #mv "$pkgdir/usr/share/$_gitname" "$pkgdir/usr/bin"
	

}

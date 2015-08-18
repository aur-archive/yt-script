# Maintainer: dimigon <stateless@archlinux.us>

pkgname=yt-script
pkgver=0.2
pkgrel=0
pkgdesc="The YouTerm script to record/playback tty sessions with various patches."
url="http://www.youterm.com"
arch=('x86_64' 'i686')
license=('BSD')
makedepends=('git')

build() {
	cd ${srcdir}

	git clone git://github.com/quantumdream/yt-script.git
	cd ${pkgname}
	make || return 1

	mkdir -p ${startdir}/pkg/usr/bin
	install -m 755 yt-script ${startdir}/pkg/usr/bin
	install -m 755 yt-termcast ${startdir}/pkg/usr/bin
}

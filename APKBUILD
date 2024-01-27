# Maintainer: Patrick Uven <patrick@uven.dev>
pkgname=blockyd
pkgver=1
pkgrel=0
pkgdesc="Daemon configuration for blocky"
url="https://github.com/0xERR0R/blocky"
arch="all"
license="Apache-2.0"
install="$pkgname.pre-install
	$pkgname.pre-upgrade
	$pkgname.post-install
	$pkgname.post-upgrade"
#depends="blocky libcap"
source="blockyd.initd
	blockyd.confd
	config.yml
	"

package() {
	install -Dm755 "$srcdir"/blockyd.initd "$pkgdir"/etc/init.d/blockyd
	install -Dm644 "$srcdir"/blockyd.confd "$pkgdir"/etc/conf.d/blockyd
	install -Dm644 "$srcdir"/config.yml "$pkgdir"/etc/blocky/config.yml
}

sha512sums="
5f69299179747fafa3b790cc6a47ffbf916a9befe2e4cedc32b7e55875584d96f98207288a1a8b714031ad59aa356550d5ef292f1d9ef32aa99a20fc55331d0d  blockyd.confd
0c567f3eb642c9e097d6a1b2f601c23e33a652439ccb0b66d5f75a30715e7e8fd563251f70219b86de31a77548190934da6bc18462894305cf66aacbf19722d3  blockyd.initd
9ede8a4b26aae73e947221f59edc94062c0020d58ef53678d479ed09aef7ab4636a48bdf921eb0c822e72b179885315f227cdc3a32767d147908828f06804692  config.yml
"

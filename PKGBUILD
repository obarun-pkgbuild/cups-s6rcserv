# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=cups-s6rcserv
pkgver=0.1
pkgrel=2
pkgdesc="cups service for"
arch=(x86_64)
license=('beerware')
depends=('cups' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('cups.longrun.dependencies'
		'cups.longrun.pipeline-name'
		'cups.longrun.producer-for'
		'cups.longrun.run'	
		'cups.longrun.type'	
		
		'cups.log.consumer-for'
		'cups.log.dependencies'
		'cups.log.run'
		'cups.log.type'
		
		'bundle.cups.contents'
		'bundle.cups.type'
		'cups.logd'
		'LICENSE')
md5sums=('68b329da9893e34099c7d8ad5cb9c940'
         '6bb549f5f80e3215d3f2ab578e167712'
         'a1c6dc3b75335fe4606709b047d076e1'
         'a33004385c9cad42f7697c63943d6633'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'cd48c6d75cb03ddd8ec5fdc13d1c5abf'
         '68b329da9893e34099c7d8ad5cb9c940'
         '9d8280c019a168ff643e1e18425fc8a7'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '9f85d89e113d644e9acee6c3a3dc49fb'
         '71abe97e2554d37f1d12c5bf4945297f'
         '47826be117555474fe289d721f07c8dc'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# bundle , trouble here user-cups need a maj at cups e.g user-Base
	install -Dm 0644 "$srcdir/bundle.cups.contents" "$pkgdir/etc/s6-serv/available/rc/bundle-Cups/contents"
	install -Dm 0644 "$srcdir/bundle.cups.type" "$pkgdir/etc/s6-serv/available/rc/bundle-Cups/type"
	
	# longrun
	install -Dm 0644 "$srcdir/cups.longrun.dependencies" "$pkgdir/etc/s6-serv/available/rc/cups-longrun/dependencies"
	install -Dm 0644 "$srcdir/cups.longrun.pipeline-name" "$pkgdir/etc/s6-serv/available/rc/cups-longrun/pipeline-name"
	install -Dm 0644 "$srcdir/cups.longrun.producer-for" "$pkgdir/etc/s6-serv/available/rc/cups-longrun/producer-for"
	install -Dm 0644 "$srcdir/cups.longrun.run" "$pkgdir/etc/s6-serv/available/rc/cups-longrun/run"
	install -Dm 0644 "$srcdir/cups.longrun.type" "$pkgdir/etc/s6-serv/available/rc/cups-longrun/type"
	
	# log
	install -Dm 0644 "$srcdir/cups.log.consumer-for" "$pkgdir/etc/s6-serv/available/rc/cups-log/consumer-for"
	install -Dm 0644 "$srcdir/cups.log.dependencies" "$pkgdir/etc/s6-serv/available/rc/cups-log/dependencies"
	install -Dm 0644 "$srcdir/cups.log.run" "$pkgdir/etc/s6-serv/available/rc/cups-log/run"
	install -Dm 0644 "$srcdir/cups.log.type" "$pkgdir/etc/s6-serv/available/rc/cups-log/type"
	
	# hook
	install -Dm 0644 "$srcdir/cups.logd" "$pkgdir/etc/s6-serv/log.d/cups-rc"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/cups-s6rcserv/LICENSE"
}

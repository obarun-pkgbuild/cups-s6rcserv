# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=cups-s6rcserv
pkgver=0.1
pkgrel=1
pkgdesc="cups service for s6"
arch=(x86_64)
license=('beerware')
depends=('cups' 's6' 's6-rc' 's6-boot')
conflicts=()
install=cups-s6rcserv.install
source=('cups.daemon.dependencies.s6'
		'cups.daemon.pipeline-name.s6'
		'cups.daemon.producer-for.s6'
		'cups.daemon.run.s6'	
		'cups.daemon.type.s6'	
		
		'cups.log.consumer-for.s6'
		'cups.log.dependencies.s6'
		'cups.log.run.s6'
		'cups.log.type.s6'
		
		'bundle.cups.contents.s6'
		'bundle.cups.type.s6'
		'LICENSE')
md5sums=('68b329da9893e34099c7d8ad5cb9c940'
         '6bb549f5f80e3215d3f2ab578e167712'
         'a1c6dc3b75335fe4606709b047d076e1'
         'a33004385c9cad42f7697c63943d6633'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '68a103d8546bf62ee68e4cd35085d9a7'
         '68b329da9893e34099c7d8ad5cb9c940'
         '9d8280c019a168ff643e1e18425fc8a7'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'aa3893850e6419fd6878ac8ca118d12f'
         '71abe97e2554d37f1d12c5bf4945297f'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# bundle , trouble here user-cups need a maj at cups e.g user-Base
	install -Dm 0644 "$srcdir/bundle.cups.contents.s6" "$pkgdir/etc/s6-serv/available/rc/bundle-Cups/contents"
	install -Dm 0644 "$srcdir/bundle.cups.type.s6" "$pkgdir/etc/s6-serv/available/rc/bundle-Cups/type"
	
	# daemon
	install -Dm 0644 "$srcdir/cups.daemon.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/cups-daemon/dependencies"
	install -Dm 0644 "$srcdir/cups.daemon.pipeline-name.s6" "$pkgdir/etc/s6-serv/available/rc/cups-daemon/pipeline-name"
	install -Dm 0644 "$srcdir/cups.daemon.producer-for.s6" "$pkgdir/etc/s6-serv/available/rc/cups-daemon/producer-for"
	install -Dm 0644 "$srcdir/cups.daemon.run.s6" "$pkgdir/etc/s6-serv/available/rc/cups-daemon/run"
	install -Dm 0644 "$srcdir/cups.daemon.type.s6" "$pkgdir/etc/s6-serv/available/rc/cups-daemon/type"
	
	# log
	install -Dm 0644 "$srcdir/cups.log.consumer-for.s6" "$pkgdir/etc/s6-serv/available/rc/cups-log/consumer-for"
	install -Dm 0644 "$srcdir/cups.log.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/cups-log/dependencies"
	install -Dm 0644 "$srcdir/cups.log.run.s6" "$pkgdir/etc/s6-serv/available/rc/cups-log/run"
	install -Dm 0644 "$srcdir/cups.log.type.s6" "$pkgdir/etc/s6-serv/available/rc/cups-log/type"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/cups-s6rcserv/LICENSE"
}

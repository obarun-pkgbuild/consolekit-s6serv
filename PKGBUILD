# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=consolekit-s6serv
pkgver=0.1
pkgrel=3
pkgdesc="consolekit service for s6"
arch=(x86_64)
license=('beerware')
depends=('consolekit' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('consolekit.daemon.run.s6'
		'consolekit.log.run.s6'
		'consolekit.logd'
		'LICENSE')
md5sums=('980cd5f58222719ee025fe43149113e0'
         'bc1599e4ebe09d76e5589e01e9e63f21'
         '8223c11360fec4068fe7c3b36ed25cc0'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/consolekit.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/consolekit/run"

	# log
	install -Dm 0755 "$srcdir/consolekit.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/consolekit/log/run"
	install -Dm 0644 "$srcdir/consolekit.logd" "$pkgdir/etc/s6-serv/log.d/consolekit"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/consolekit-s6serv/LICENSE"
}

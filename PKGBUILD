# Maintainer: Alexander Grothe <seahawk1986[at]hotmail.com>
pkgname=lifeguard-ng
pkgver=0.0.1
pkgrel=1
pkgdesc="check for active services via dbus"
arch=('x86_64')
url="https://github.com/seahawk1986/lifeguard-ng"
license=('GPL')
depends=('python-gobject' 'python-dbus' 'python-psutil')
optdepends=('samba: detect active Samba shares'
            'nfs-utils: detect active NFS shares')
provides=('$pkgname')
backup=("etc/lifeguard.conf")
source=(git://github.com/seahawk1986/lifeguard-ng.git)
md5sums=('SKIP')


package() {
  cd $srcdir/$pkgname
  install -Dm755 lifeguard.py "$pkgdir/usr/bin/lifeguard"
  install -Dm755 check-lifeguard "$pkgdir/usr/bin/check-lifeguard"
  install -Dm644 lifeguard.conf  "$pkgdir/etc/lifeguard.conf"
  install -Dm644 lifeguard.service "${pkgdir}"/usr/lib/systemd/system/lifeguard.service
}

# vim:set ts=2 sw=2 et:

# Maintainer: DarkXero <info@techxero.com>

pkgname=grub-tools
pkgdesc="Fixes, additions and enhancements to grub and os-prober."
pkgver=1.6.6
pkgrel=2
arch=('any')
license=('GPL')
depends=(grub lsb-release)
optdepends=(os-prober-btrfs)

url=https://github.com/xerolinux/$pkgname
_url="https://raw.githubusercontent.com/xerolinux/main/$pkgname"

source=(
  $_url/grub-install.hook
  $_url/grub-kernel.hook
  $_url/grub-microcode.hook
  $_url/grub-mkconfig.hook
  $_url/initrd-generation-fix
  $_url/initrd-generation-fix.hook
)
sha512sums=('95d0a13e73c7471f4a631b2ba2100e678a2e004368716bc9ba72abadd46791c6ceeeff8977c1c776d8a4c176d3aab6dc3468392f59e6c729ce42b255058b3165'
            '5af5448f27680afe12ba91ba834edffab4fa1cd0d779d0b08cb41da13549b9f245d4c591683690f5c00d6baa77f8e13d03d0d004ba167e2258391a24c42e5a8b'
            'eca3b46a7e6281ebcf4f9227500feda5bac0f64c21823c866023ede4470b0a818c8ff259975ea98c2c69c67150129f9d277f0c0da290782281ebae3deecebb7b')

package() {
  cd $srcdir

  install -d $pkgdir/usr/share/libalpm/hooks
  install -Dm644 grub-install.hook   $pkgdir/usr/share/libalpm/hooks/grub-install.hook
  install -Dm644 grub-kernel.hook   $pkgdir/usr/share/libalpm/hooks/grub-kernel.hook
  install -Dm644 grub-microcode.hook   $pkgdir/usr/share/libalpm/hooks/grub-microcode.hook
  install -Dm644 grub-mkconfig.hook   $pkgdir/usr/share/libalpm/hooks/grub-mkconfig.hook
  install -Dm644 initrd-generation-fix.hook $pkgdir/usr/share/libalpm/hooks/initrd-generation-fix.hook

  install -d $pkgdir/usr/bin
  install -Dm755 initrd-generation-fix      $pkgdir/usr/bin/initrd-generation-fix
}

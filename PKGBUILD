# Maintainer: Victor Häggqvist <aur@snilius.com>
# Any Co-Maintainers are walcome

pkgname=fahclient
pkgver=7.4.4
pkgrel=1
pkgdesc='The (back-end) client software managed by FAHControl (Folding@Home)'
url="http://folding.stanford.edu/English/HomePage"
arch=('x86_64')
license=('GPL3')
optdepends=('fahcontrol: GUI for Folding@Home')
source=(https://fah.stanford.edu/file-releases/public/release/fahclient/debian-testing-64bit/v7.4/fahclient_7.4.4_amd64.deb)
sha1sums=('06d001110dd05d3c2e55c77c3ec52befb1e92d0e')

# Moronic server
DLAGENTS=("https::/usr/bin/curl -k -o %o %u")

package() {
  cd ${srcdir}
  tar -xf data.tar.gz
  install -D -m0755 ${srcdir}/usr/bin/FAHClient ${pkgdir}/usr/bin/FAHClient
  install -D -m0755 ${srcdir}/usr/bin/FAHCoreWrapper ${pkgdir}/usr/bin/FAHCoreWrapper
  install -D -m0644 ${srcdir}/usr/share/pixmaps/FAHClient.png ${pkgdir}/usr/share/pixmaps/FAHClient.png
  install -D -m0644 ${srcdir}/usr/share/applications/FAHWebControl.desktop ${pkgdir}/usr/share/applications/FAHWebControl.desktop
}

# vim:set ts=2 sw=2 et:

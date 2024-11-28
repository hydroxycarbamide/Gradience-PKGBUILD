# Maintainer: D3vil0p3r <vozaanthony[at]gmail[dot]com>

pkgname=gradience
_pkgname=Gradience
pkgver=0.8.0_beta4
pkgrel=1
pkgdesc="Change the look of Adwaita, with ease"
arch=('x86_64')
url="https://github.com/hydroxycarbamide/Gradience"
license=('GPL3')
depends=('libadwaita' 'libsoup3' 'python-gobject' 'python-anyascii' 'python-libsass' 'python-lxml' 'python-pillow' 'python-pluggy' 'python-svglib' 'libportal-gtk4' 'python-jinja')
makedepends=('meson' 'blueprint-compiler' 'gobject-introspection' 'sassc')
checkdepends=('appstream-glib')
optdepends=('adw-gtk-theme: LibAdwaita Theme for all GTK3 and GTK4 Apps.')
install='xdg-config.install'
source=("git+$url.git#tag=${pkgver//_/-}")
sha512sums=('SKIP')

prepare() {
  cd "$srcdir/$_pkgname"
  git submodule update --init --recursive
}

build() {
  arch-meson "$srcdir/$_pkgname" build --wipe
  meson compile -C build
}

check() {
  meson test -C build --print-errorlogs || :
}

package() {
  meson install -C build --destdir "$pkgdir"
}

# Contributor: Matt Harrison <matt at mistbyte dot com>
# Contributor: Danny Navarro <j@dannynavarro.net>
# Contributor: Joris Steyn <jorissteyn@gmail.com>

pkgname=ruby-chunky_png
_gemname=${pkgname#ruby-}
pkgver=1.3.0
pkgrel=1
pkgdesc="Pure Ruby library to read and write PNG images"
arch=('any')
url="http://github.com/wvanbergen/chunky_png"
license=('MIT')
groups=()
depends=('ruby')
makedepends=('rubygems')
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
source=("http://gems.rubyforge.org/gems/${_gemname}-${pkgver}.gem")
noextract=("${_gemname}-${pkgver}.gem")
md5sums=('345800b348b3e56b902e0baceba5720c')


package() {
  local _gemdir="$(ruby -rubygems -e'puts Gem.default_dir')"
  gem install --no-user-install --ignore-dependencies -i "$pkgdir$_gemdir" \
              -n "$pkgdir/usr/bin" ${_gemname}-$pkgver.gem
  install -D "$pkgdir$_gemdir/gems/${_gemname}-$pkgver/LICENSE" \
             "$pkgdir/usr/share/licenses/${pkgname}/LICENSE"
}

# vim:set ts=2 sw=2 et:


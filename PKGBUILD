# Maintainer: maman
pkgname=nix-bash-completions-git
pkgver=r243.e6db308
pkgrel=1
pkgdesc="Bash completion for the Nix and NixOS command line tools."
arch=(any)
url="https://github.com/maman/nix-bash-completions"
license=('MIT')
depends=('nix' 'bash' 'bash-completion')
makedepends=('git')
source=('nix-bash-completions::git+https://github.com/maman/nix-bash-completions.git')
md5sums=('SKIP')

pkgver() {
  cd "nix-bash-completions"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  mkdir -p mkdir -p $pkgdir/usr/share/licenses/nix-bash-completions/
  mkdir -p $pkgdir/etc/bash_completion.d/
  cd nix-bash-completions
  cp LICENSE $pkgdir/usr/share/licenses/nix-bash-completions/LICENSE
  cp _nix $pkgdir/etc/bash_completion.d/_nix
}
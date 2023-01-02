# Maintainer: Mateus Felipe Gonçalves (mateusfg7) <mateusfelipefg77@gmail.com>
# Contributor: Bachitter Chahal <bachitterch@pm.me>

pkgname=pscale
_pkgname=pscale
pkgver=0.126.0
pkgrel=5
pkgdesc='PlanetScale CLI client package for Arch'
arch=('x86_64')
url='https://github.com/planetscale/cli'
license=('Apache')
provides=('pscale')
conflicts=('pscale' 'pscale-git' 'pscale-bin' 'pscale-cli')
source=("https://github.com/planetscale/cli/releases/download/v${pkgver}/${_pkgname}_${pkgver}_linux_amd64.tar.gz")
sha256sums=('657cac6a64a5e03eb035f5b906bbe767883a7253632e66f13fcaa3979d5c8179')

package() {
  install -Dm755 pscale ${pkgdir}/usr/bin/pscale
  
  if [ -d "/usr/share/fish/vendor_completions.d/" ]; then
    install -Dm644 completions/pscale.fish ${pkgdir}/usr/share/fish/vendor_completions.d/pscale.fish
  fi

  if [ -d "/usr/share/bash-completion/completions/" ]; then
    install -Dm644 completions/pscale.bash ${pkgdir}/usr/share/bash-completion/completions/_pscale
  fi
  
  if [ -d "/usr/share/zsh/site-functions/" ]; then
   install -Dm644 completions/pscale.zsh ${pkgdir}/usr/share/zsh/site-functions/_pscale
  fi
}

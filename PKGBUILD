pkgname=keep-kernel-modules-hook
pkgver=0.1
pkgrel=1
pkgdesc="Keeps using kernel after kernel upgrade"
arch=('any')
url="https://github.com/hosxy/keep-kernel-modules-hook"
license=('UNLICENSE')
depends=('base')

source=("keep-kernel-modules"
		"99-keep-kernel-modules-pre.hook"
		"99-keep-kernel-modules-post.hook"
		)
sha256sums=('SKIP' 'SKIP' 'SKIP')

package() {
	install -Dm755 'keep-kernel-modules' "${pkgdir}/usr/share/libalpm/scripts/keep-kernel-modules"
	install -Dm644 '99-keep-kernel-modules-pre.hook' "${pkgdir}/usr/share/libalpm/hooks/99-keep-kernel-modules-pre.hook"
	install -Dm644 '99-keep-kernel-modules-post.hook' "${pkgdir}/usr/share/libalpm/hooks/99-keep-kernel-modules-post.hook"
}

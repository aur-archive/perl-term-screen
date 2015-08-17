# Maintainer: uberushaximus <uberushaximus AT gmail DOT com>

pkgname=perl-term-screen
pkgver=1.03
pkgrel=2
pkgdesc='A Simple all perl Term::Cap based screen positioning module'
_dist=Term-Screen
arch=('any')
url="https://metacpan.org/release/$_dist"
license=('GPL' 'PerlArtistic')
depends=(perl)
options=('!emptydirs' purge)
source=("http://cpan.metacpan.org/authors/id/J/JS/JSTOWE/$_dist-$pkgver.tar.gz")
md5sums=('1a57d3aa267d613a8897933a99f7110e')

build() (
  cd "$srcdir/$_dist-$pkgver"
  unset PERL5LIB PERL_MM_OPT PERL_LOCAL_LIB_ROOT
  export PERL_MM_USE_DEFAULT=1 PERL_AUTOINSTALL=--skipdeps
  /usr/bin/perl Makefile.PL
  make
)

check() (
  cd "$srcdir/$_dist-$pkgver"
  unset PERL5LIB PERL_MM_OPT PERL_LOCAL_LIB_ROOT
  export PERL_MM_USE_DEFAULT=1
  make test
)

package() (
  cd "$srcdir/$_dist-$pkgver"
  unset PERL5LIB PERL_MM_OPT PERL_LOCAL_LIB_ROOT
  make install INSTALLDIRS=vendor DESTDIR="$pkgdir"
)


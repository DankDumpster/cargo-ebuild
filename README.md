# cargo-ebuild

[![Build Status](https://travis-ci.org/cardoe/cargo-ebuild.svg?branch=master)](https://travis-ci.org/cardoe/cargo-ebuild) [![Latest Version](https://img.shields.io/crates/v/cargo-ebuild.svg)](https://crates.io/crates/cargo-ebuild)

`cargo ebuild` is a Cargo subcommand that generates an
[ebuild](https://wiki.gentoo.org/wiki/Ebuild) recipe that uses
[cargo.eclass](https://gitweb.gentoo.org/repo/gentoo.git/tree/eclass/cargo.eclass)
to build a Cargo based project for [Gentoo](https://gentoo.org/)

Install it with Cargo:

```
$ cargo install cargo-ebuild
```

In its default mode, `cargo ebuild` will write the recipe for the
local crate:

```
# Auto-Generated by cargo-ebuild 0.1.0

EAPI=6

CRATES="
gdi32-sys-0.2.0
rand-0.3.14
rustache-0.0.3
libz-sys-1.0.4
url-0.2.38
toml-0.1.30
utf8-ranges-0.1.3
aho-corasick-0.5.2
cargo-ebuild-0.1.0
gcc-0.3.28
curl-0.2.19
openssl-sys-0.7.14
thread-id-2.0.0
log-0.3.6
regex-syntax-0.3.4
tempdir-0.3.4
memstream-0.0.1
unicode-bidi-0.2.3
libgit2-sys-0.4.3
env_logger-0.3.3
user32-sys-0.2.0
cargo-0.10.0
docopt-0.6.81
miniz-sys-0.1.7
curl-sys-0.1.34
tar-0.4.6
term-0.4.4
pkg-config-0.3.8
glob-0.2.11
unicode-normalization-0.1.2
advapi32-sys-0.1.2
semver-0.2.3
cmake-0.1.17
regex-0.1.73
crates-io-0.2.0
memchr-0.1.11
libressl-pnacl-sys-2.1.6
matches-0.1.2
winapi-0.2.7
libssh2-sys-0.1.37
uuid-0.1.18
flate2-0.2.14
thread_local-0.2.6
nom-1.2.3
fs2-0.2.5
idna-0.1.0
pnacl-build-helper-1.4.10
bitflags-0.1.1
url-1.1.1
git2-0.4.3
winapi-build-0.1.1
kernel32-sys-0.2.2
num_cpus-0.2.13
filetime-0.1.10
crossbeam-0.2.9
time-0.1.35
git2-curl-0.4.1
strsim-0.3.0
libc-0.2.13
rustc-serialize-0.3.19
"

inherit cargo

DESCRIPTION="Generates an ebuild for a package using the in-tree eclasses."
HOMEPAGE="https://github.com/cardoe/cargo-ebuild"
SRC_URI="$(cargo_crate_uris ${CRATES})"
RESTRICT="mirror"
LICENSE=""
SLOT="0"
KEYWORDS="~amd64"
IUSE=""

DEPEND=""
RDEPEND=""
```
# ignis-xbps-src
xbps-src template for [ignis widgets framework](https://github.com/linkfrg/ignis)

# EN - English
To install this template:
```
$ git clone https://github.com/void-linux/void-packages.git
```
The Void Linux package repository is quite large, so be prepared to wait depending on your internet connection.

Next:
```
$ cd void-packages/
$ ./xbps-src --binary-bootstrap
```
Then:
```
$ mkdir -p srcpkgs/ignis
```
Download the template directly from this repository and place it in your srcpkgs/ignis directory.
The location depends on where you cloned the repository. In my case it's ~/.local/pkgs/void-packages/srcpkgs/ignis
But you'll need to check where you cloned it.

Alternatively, you can simply create the template with the following content:
```
pkgname=ignis
version=0.5
revision=2
wrksrc="${pkgname}-${version}"
build_style=meson
makedepends="
glib-devel
gtk4-layer-shell-devel
pulseaudio-devel
meson
ninja
pkg-config
python3
gobject-introspection
git"
depends="python3 python3-gobject python3-loguru gobject-introspection"
short_desc="A widget framework for building desktop shells, written and configurable in Python."
maintainer="binarylinuxx <aar58384@gmail.com>"
license="LGPL-2.1-or-later"
homepage="https://github.com/linkfrg/ignis"
distfiles="https://github.com/linkfrg/ignis/archive/refs/tags/v${version}.tar.gz"
checksum=52c1be35de4ac3cdf952cdd6b21592b6076245720001db7f2e5aef2489f70768
configure_args="--wrap-mode=forcefallback"

post_install() {
    vlicense LICENSE
}
```
Once the template is ready:
```
$ ./xbps-src pkg ignis
```
Wait for the build to complete, and when it's done:
```
$ sudo xbps-install -R hostdir/binpkgs ignis
```
# RU - русский
чтобы установить даный шаблон
```
$ git clone https://github.com/void-linux/void-packages.git
```
репозиторий пакетов у воида достатачно большой так что будь готов подождать зависит от интернета

далее
```
$ cd void-packages/
$ ./xbps-src --binary-bootstrap
```

дальше
```
$ mkdir -p srcpkgs/ignis
```
скачайте шаблон прямо из этого репозитория и вставте туда где у вас srcpkgs/ignis
зависит от того куда склонировали репозиторий в моем случае ~/.local/pkgs/void-packages/srcpkgs/ignis
ну а ты сам смотри где ты склонировал
так же можно просто прописать данный шаблон:
```
pkgname=ignis
version=0.5
revision=2
wrksrc="${pkgname}-${version}"
build_style=meson
makedepends="
glib-devel
gtk4-layer-shell-devel
pulseaudio-devel
meson
ninja
pkg-config
python3
gobject-introspection
git"
depends="python3 python3-gobject python3-loguru gobject-introspection"
short_desc="A widget framework for building desktop shells, written and configurable in Python."
maintainer="binarylinuxx <aar58384@gmail.com>"
license="LGPL-2.1-or-later"
homepage="https://github.com/linkfrg/ignis"
distfiles="https://github.com/linkfrg/ignis/archive/refs/tags/v${version}.tar.gz"
checksum=52c1be35de4ac3cdf952cdd6b21592b6076245720001db7f2e5aef2489f70768
configure_args="--wrap-mode=forcefallback"

post_install() {
    vlicense LICENSE
}
```
потом когда шаблон есть и все готово
```
$ ./xbps-src pkg ignis
```
ожидайте конца сборки
и как готово
```
$ sudo xbps-install -R hostdir/binpkgs ignis
```

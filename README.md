# ignis-xbps-src
xbps-src template for [ignis widgets framework](https://github.com/linkfrg/ignis)

# EN - English
> **Note**  
> This repo provides only stable version of ignis. If you want the latest version,
> go to → [ignis-install-page](https://linkfrg.github.io/ignis/stable/user/installation.html)

To install this template:
```bash
$ git clone https://github.com/void-linux/void-packages.git
```
The Void Linux package repository is quite large, so be prepared to wait depending on your internet connection.

Next:
```bash
$ cd void-packages/
$ ./xbps-src --binary-bootstrap
```
Then:
```bash
$ mkdir -p srcpkgs/ignis
```
Download the template directly from this repository and place it in your srcpkgs/ignis directory.
The location depends on where you cloned the repository. In my case it's ~/.local/pkgs/void-packages/srcpkgs/ignis
But you'll need to check where you cloned it.

Alternatively, you can simply create the template with the following content:
```bash
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
```bash
$ ./xbps-src pkg ignis
```
Wait for the build to complete, and when it's done:
```bash
$ sudo xbps-install -R hostdir/binpkgs ignis
```

# RU - Русский
> **Примечание**  
> Этот пакет предоставляет только стабильную версию ignis. Если хотите самую новую версию,
> то вам тута → [установка-игниса](https://linkfrg.github.io/ignis/stable/user/installation.html)

Чтобы установить данный шаблон:
```bash
$ git clone https://github.com/void-linux/void-packages.git
```
Репозиторий пакетов у Void достаточно большой, так что будь готов подождать (зависит от интернета).

Далее:
```bash
$ cd void-packages/
$ ./xbps-src --binary-bootstrap
```

Дальше:
```bash
$ mkdir -p srcpkgs/ignis
```
Скачайте шаблон прямо из этого репозитория и вставьте туда, где у вас srcpkgs/ignis.
Зависит от того, куда склонировали репозиторий. В моем случае ~/.local/pkgs/void-packages/srcpkgs/ignis
Ну а ты сам смотри, где ты склонировал.

Также можно просто прописать данный шаблон:
```bash
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
depends="python3 python3-gobject python3-click python3-cairo python3-loguru gobject-introspection"
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
Потом, когда шаблон есть и все готово:
```bash
$ ./xbps-src pkg ignis
```
Ожидайте конца сборки, и как готово:
```bash
$ sudo xbps-install -R hostdir/b
```

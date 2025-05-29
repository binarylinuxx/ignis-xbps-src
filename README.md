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

Потом, когда шаблон есть и все готово:
```bash
$ ./xbps-src pkg ignis
```
Ожидайте конца сборки, и как готово:
```bash
$ sudo xbps-install -R hostdir/binpkgs ignis
```

# Lokálna inštalácia D

Najnovšiu verziu referenčného kompilátora **DMD** (Digital Mars D)
je možné [stiahnuť](http://dlang.org/download.html) a nainštalovať
z oficiálnej stránky jazyka D [dlang.org](https://dlang.org):

### Linux / FreeBSD / macOS

Pre rýchlu inštaláciu `dmd` do vášho domovského priečinka, spustite v termináli príkaz:
`curl -fsS https://dlang.org/install.sh | bash -s dmd`

Pre viaceré distribúcie sú k dispozícii priamo inštalačné balíky:

* [ArchLinux](https://wiki.archlinux.org/index.php/D_(programming_language))
* [Debian/Ubuntu](http://d-apt.sourceforge.net).
* [Fedora/CentOS](http://dlang.org/download.html#dmd)
* [Gentoo](https://wiki.gentoo.org/wiki/Dlang)
* [OpenSuse](http://dlang.org/download.html#dmd)

### Windows

* [Inštalátor](http://downloads.dlang.org/releases/2.x/{{latest-release}}/dmd-{{latest-release}}.exe)
* alebo [archív](http://downloads.dlang.org/releases/2.x/{{latest-release}}/dmd.{{latest-release}}.windows.7z)
* alternatívne prostredníctvom [chocolatey](https://chocolatey.org/packages/dmd): `choco install dmd`

### macOS

* `.dmg` [balík](http://downloads.dlang.org/releases/2.x/{{latest-release}}/dmd.{{latest-release}}.dmg)
* alebo [archív](http://downloads.dlang.org/releases/2.x/{{latest-release}}/dmd.{{latest-release}}.osx.tar.xz)
* prípadne pomocou [Homebrew](http://brew.sh): `brew install dmd`

### Alternatívne kompilátory

Popri referenčnom kompilátore, ktorý používa svoj vlastný bekend,
sú k dispozícii i ďalšie dva kompilátory, ktoré možno získať v sekcii Na stiahnutie na
[dlang.org](https://dlang.org):

* [**GDC**](http://gdcproject.org/downloads), ktorý využíva bekend GNU Compiler Collection
* [**LDC**](https://github.com/ldc-developers/ldc#installation), ktorý je založený na bekende LLVM

Oba kompilátory GDC a LDC obvykle zaostávajú za verziou frontendu referenčného kompilátora DMD,
dosahujú však lepšie úrovne optimalizácie a rovnako tiež umožňujú podporu ďalších platforiem
ako napríklad ARM.

Viac informácií ku kompilátorom nájdete aj na [wiki jazyka D](https://wiki.dlang.org/Compilers)


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

## Alternatívne kompilátory

Popri referenčnom kompilátore, ktorý používa svoj vlastný bekend,
sú k dispozícii i ďalšie dva kompilátory, ktoré možno získať v sekcii Na stiahnutie (Download) na
[dlang.org](https://dlang.org):

* [**GDC**](http://gdcproject.org/downloads), ktorý využíva bekend GNU Compiler Collection
* [**LDC**](https://github.com/ldc-developers/ldc#installation), ktorý je založený na bekende LLVM

Oba kompilátory GDC a LDC obvykle zaostávajú za verziou frontendu referenčného kompilátora DMD,
dosahujú však lepšie úrovne optimalizácie a rovnako tiež umožňujú podporu ďalších platforiem
ako napríklad ARM.

Viac informácií ku kompilátorom nájdete aj na [wiki jazyka D](https://wiki.dlang.org/Compilers)

## Nastavte si váš textový editor

Krásou jazyka D je to, že nepotrebujete vyčačkané vývojové prostredie, keďže generovať opakujúci sa a mierne poupravovaný kód (tzv. boilerplate) je potrebné veľmi výnimočne.
Používanie jazyka D je však príjemnejšie, ak máte možnosť pohybovať sa v známom prostredí vášho obľúbeného textového editora.
Podpora jazyka D (zabezpečená zásuvnými modulmi) je aktuálne k dispozícii minimálne pre nasledujúce editory:

- [Atom](https://github.com/Pure-D/atomize-d)
- [Eclipse](http://ddt-ide.github.io)
- [Emacs](https://github.com/Emacs-D-Mode-Maintainers/Emacs-D-Mode)
- [IntelliJ](https://github.com/intellij-dlanguage/intellij-dlanguage)
- [Sublime Text](https://github.com/yazd/DKit)
- [Vim](https://wiki.dlang.org/D_in_Vim)
- [VS Code](https://marketplace.visualstudio.com/items/webfreak.code-d)
- [Visual Studio](http://rainers.github.io/visuald/visuald/StartPage.html)

K dispozícii sú tiež tieto integrované vývojové prostredia (IDE) venované jazyku D:

- [Coedit](https://github.com/BBasile/Coedit)
- [Dlang IDE](https://github.com/buggins/dlangide)

V oficiálnej dokumentácii jazyka D je k dispozícii podrobnejší prehľad dostupných [editorov](https://wiki.dlang.org/Editors) a [IDE](https://wiki.dlang.org/IDEs).
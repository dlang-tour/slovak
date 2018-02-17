# Lokálna inštalácia D

Referenčný kompilátor jazyka D sa nazýva **DMD** (Digital Mars D).
Tiež je k dispozícii kompilátor [LDC](https://github.com/ldc-developers/ldc)
(založený na [LLVM](http://llvm.org) bekende)
a kompilátor [GDC](https://gdcproject.org) (založený na [GCC](https://gcc.gnu.org/) bekende).
Viac informácií ku kompilátorom nájdete aj na [wiki jazyka D](https://wiki.dlang.org/Compilers),
avšak ak ste v jazyku D nováčik a neviete sa rozhodnúť, ktorý kompilátor nainštalovať,
nainštalujte si DMD.

## Stiahnutie a inštalácia

Sekcia [Na stiahnutie](https://dlang.org/download.html) oficiálnej stránky jazyka D
poskytuje prehľad rôznych implementácií a obsahuje odkazy na predpripravené
balíky DMD kompilátora podľa operačného systému nachystané na stiahnutie a inštaláciu.

Alternatívu ku balíkom pre jednotlivé operačné systémy predstavuje
[inštalačný skript](https://dlang.org/install.html) použiteľný na akomkoľvek
Posix-ovom systéme (Linux, FreeBSD, MacOS), ktorý umožní nainštalovať rôzne implementácie
kompilátorov (včítane podpory inštalácie viacerých verzií súčasne) lokálne bez
potreby administrátorského prístupu.
Prejdite si [dokumentáciu inštalačného skriptu](https://dlang.org/install.html) pre
viac podrobností

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
- [__Visual Studio__](http://rainers.github.io/visuald/visuald/StartPage.html)

K dispozícii sú tiež tieto integrované vývojové prostredia (IDE) venované jazyku D:

- [Coedit](https://github.com/BBasile/Coedit)
- [Dlang IDE](https://github.com/buggins/dlangide)

V oficiálnej dokumentácii jazyka D je k dispozícii podrobnejší prehľad dostupných [editorov](https://wiki.dlang.org/Editors) a [IDE](https://wiki.dlang.org/IDEs).
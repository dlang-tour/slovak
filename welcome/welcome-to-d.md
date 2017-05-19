# Vitajte vo svete jazyka D

Vitajte v interaktívnej prehliadke *programovacieho jazyka D*.

{{#dmanmobile}}

Táto prehliadka prináša prehľad __silného__ a __expresívneho__ jazyka D
kompilovaného priamo do __efektívneho__ __natívneho__ strojového kódu.

{{/dmanmobile}}

### Čo je jazyk D?

Jazyk D ako zúročený výsledok _desaťročí skúseností získaných pri implementácii kompilátorov_
pre mnoho rozličných jazykov má jedinečnú množinu vlastností:

{{#dmandesktop}}

- _vysokoúrovňové_ jazykové konštrukcie pre vynikajúce možnosti modelovania
- _vysoký výkon_, kompilovaný jazyk
- statické typovanie
- priame napojenie na aplikačné programové rozhranie (API) operačného systému a priamy prístup k hardvéru
- bleskovo rýchle časy kompilácie
- vymedzenú množinu vlastností garantujúcu pamäťovú bezpečnosť (SafeD)
- _spravovateľný_, _ľahko porozumiteľný_ zdrojový kód
- postupnú krivku učenia (syntax skupiny jazykov C, podobná Jave a iným jazykom)
- kompatibilitu s aplikačným binárnym rozhraním (ABI) jazyka C
- ohraničenú kompatibilitu s aplikačným binárnym rozhraním (ABI) jazyka C++
- viac-paradigmový prístup k programovaniu (imperatívne, štruktúrované, objektovo-orientované, generické, funkcionálne, i dokonca assembler)
- zabudovanú detekciu chýb (kontrakty, unit testy)

... a veľa ďalších [vlastností](http://dlang.org/overview.html).

{{/dmandesktop}}

### O prehliadke

Každá sekcia obsahuje príklad so zdrojovým kódom, ktorý je možné upravovať a používať
na experimentovanie s možnosťami a vlastnosťami jazyka D.
Pre kompiláciu a následné spustenie kódu stlačte tlačidlo 'Spustiť' (alebo klávesovú skratku `Ctrl-enter`).

### Prispievanie

Táto prehliadka má [otvorený zdrojový kód](https://github.com/dlang-tour)
a vítame žiadosti o zapracovanie zmien (pull request), ktoré ju spravia ešte lepšou.

## {SourceCode}

```d
import std.stdio;
import std.algorithm;
import std.range;

void main()
{
    // Poďme na to!
    writeln("Ahoj svet!");

    // Príklad pre skúsených programátorov:
    // Vezmite tri polia a bez alokovania
    // ďalšej pamäte v nich preusporiadajte
    // ich prvky
    int[] arr1 = [4, 9, 7];
    int[] arr2 = [5, 2, 1, 10];
    int[] arr3 = [6, 8, 3];
    sort(chain(arr1, arr2, arr3));
    writefln("%s\n%s\n%s\n", arr1, arr2, arr3);
    // Viac podrobností k tomuto príkladu
    // nájdete na stránke "Rozsahové algoritmy"
    // v sekcii "Klenoty"
}
```

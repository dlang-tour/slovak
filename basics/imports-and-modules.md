# Moduly a importovanie

I v jednoduchom programe (typu 'Ahoj svet') je zväčša potrebné v jazyku D použiť `import` klauzulu.
`import` klauzula sprístupní všetky verejné funkcie a deklarované typy z daného **modulu**.

Štandardná knižnica, nazývaná [Phobos](https://dlang.org/phobos/),
je umiestnená v **balíku** `std`, pričom jej jednotlivé moduly sa sprístupňujú cez konštrukciu `import std.MODUL`.

Klauzulou `import` je možné tiež selektívne vymedziť rozsah sprístupnených symbolov:

    import std.stdio : writeln, writefln;

Selektívne importy možno využívať na zvýšenie čitateľnosti
ozrejmením toho, odkiaľ symbol pochádza a taktiež ako prevenciu
nejednoznačnosti symbolov s rovnakým názvom, ak sa nachádzajú v rozličných moduloch.

`import` klauzuly netreba uvádzať na začiatku zdrojového súboru.
Je možné ich použiť i lokálne vo funkciách alebo všeobecne v inom rozsahu platnosti.

## {SourceCode}

```d
void main()
{
    import std.stdio;
    // tiež možno použiť:
    // import std.stdio : writeln;
    writeln("Ahoj svet!");
}
```

# Moduly a importovanie

{{#img-right}}turtle.svg{{/img-right}}

One of D's core design decision was to be consistent and avoid corner cases
in the language.
This is called [_turtles all the way down_](https://en.wikipedia.org/wiki/Turtles_all_the_way_down).
One good example for this consistency are `import`s.

## Imports

I v jednoduchom programe (typu 'Ahoj svet') je zväčša potrebné v jazyku D použiť `import` klauzulu.
`import` klauzula sprístupní všetky verejné funkcie a deklarované typy z daného **modulu**.

### The turtles start falling down

`import` klauzuly netreba uvádzať na začiatku zdrojového súboru.
Je možné ich použiť i lokálne vo funkciách alebo všeobecne v inom rozsahu platnosti.
In the following chapters you will see that this applies to almost all concepts in D. The language doesn't expose arbitrary restrictions on you.

### Selective imports

Štandardná knižnica, nazývaná [Phobos](https://dlang.org/phobos/),
je umiestnená v **balíku** `std`, pričom jej jednotlivé moduly sa sprístupňujú cez konštrukciu `import std.MODUL`.

Klauzulou `import` je možné tiež selektívne vymedziť rozsah sprístupnených symbolov:

    import std.stdio : writeln, writefln;

Selektívne importy možno využívať na zvýšenie čitateľnosti
ozrejmením toho, odkiaľ symbol pochádza a taktiež ako prevenciu
nejednoznačnosti symbolov s rovnakým názvom, ak sa nachádzajú v rozličných moduloch.

### Imports match directories and files

D's module system — in contrast to other systems — is entirely based on files.
For example, `my.cat` always refers to a file `cat.d` in the folder `my/`.
The folder `my` needs to be in the current working directory or
in one of the explicitly specified directory imports (`-I`).
Lastly, to ease splitting big modules up into multiple smaller files,
instead of `cat.d`, a folder `cat/` could be used as well.
The D compiler would then try to load `my/cat/package.d` instead of `my/cat.d`.

The convention (but not a hard rule) for `package.d` files is to publicly import
all other modules in the same folder.

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

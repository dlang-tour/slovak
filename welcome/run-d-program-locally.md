# Spustenie programu v jazyku D lokálne

Po nainštalovaní jazyka D sú k dispozícii kompilátor `dmd`, podporný nástroj `rdmd` umožňujúci písať skripty v jazyku D a
manažér balíkov `dub`.

### Kompilátor DMD

Kompilátor *DMD* kompiluje zdrojové súbory jazyka D a vytvára spustiteľný súbor.
Na príkazovom riadku je možné spustiť *DMD* s názvom súboru:

    dmd ahoj.d

Existuje veľa možností, ktoré vám umožnia upraviť správanie kompilátora.
Preštudujte si [online dokumentáciu](https://dlang.org/dmd.html#switches) alebo použite príkaz `dmd --help` pre zobrazenie prehľadu dostupných prepínačov.

### Kompilácia za behu pomocou `rdmd`

Pomocný nástroj `rdmd` distribuovaný spoločne s kompilátorom DMD
zabezpečí kompiláciu všetkých závislostí a automaticky spustí výslednú aplikáciu:

    rdmd ahoj.d

Na systémoch typu UNIX je možné vložiť ako prvý riadok spustiteľného D súboru tzv. *shebang* riadok
(prvý riadok skriptu definujúci jeho interpreter) v tvare `#!/usr/bin/env rdmd`.
To umožní priame použitie zdrojového súboru D jazyka ako spustiteľného skriptu.

Preštudujte si [online dokumentáciu](https://dlang.org/rdmd.html) alebo použite príkaz `rdmd --help` pre zobrazenie prehľadu dostupných prepínačov.

### Manažer balíkov `dub`

Štandardný manažér balíkov jazyka D sa nazýva [`dub`](http://code.dlang.org). Keď je `dub` dostupný ako lokálne nainštalovaná aplikácia,
je možné vytvoriť nový projekt s názvom `ahoj` pomocou nasledujúceho príkazu:

    dub init ahoj

Spustenie príkazu `dub` vo vytvorenom priečinku ahoj následne posťahuje všetky závislosti, skompiluje aplikáciu a napokon ju spustí.
Príkaz `dub build` len skompiluje projekt bez spustenia aplikácie.

Preštudujte si [online dokumentáciu](https://code.dlang.org/docs/commandline) alebo použite príkaz `dub help` pre zobrazenie prehľadu dostupných povelov a možností.

Všetky dostupné dub balíky je možné prehliadať prostredníctvom verejného [webového rozhrania](https://code.dlang.org) manažéra balíkov.

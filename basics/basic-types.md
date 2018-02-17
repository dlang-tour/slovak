# Základné typy

D provides a number of basic types which always have the same
size **regardless** of the platform - the only exception
is the `real` type which provides the highest possible floating point
precision. There is no difference
between the size of an integer regardless of whether the application
is compiled for 32-bit or 64-bit systems.

| typ                           | veľkosť
|-------------------------------|------------
|`bool`                         | 8 bitov
|`byte`, `ubyte`, `char`        | 8 bitov
|`short`, `ushort`, `wchar`     | 16 bitov
|`int`, `uint`, `dchar`         | 32 bitov
|`long`, `ulong`                | 64 bitov

#### Typy s plávajúcou desatinnou čiarkou:

| typ     | veľkosť
|---------|--------------------------------------------------
|`float`  | 32 bitov
|`double` | 64 bitov
|`real`   | >= 64 bitov (všeobecne 64 bitov, avšak 80 bitov na 32-bitovej architektúre Intel x86)

The prefix `u` denotes *unsigned* types. `char` translates to
UTF-8 characters, `wchar` is used in UTF-16 strings and `dchar`
in UTF-32 strings.

A conversion between variables of different types is only
allowed by the compiler if no precision is lost. However,
a conversion between floating point types
(e.g `double` to `float`) is allowed.

A conversion to another type may be forced by using the
`cast(TYPE) myVar` expression. It needs to be used with great care though,
as the `cast` expression is allowed to break the type system.

The special keyword `auto` creates a variable and infers its
type from the right hand side of the expression. `auto myVar = 7`
will deduce the type `int` for `myVar`. Note that the type is still
set at compile-time and can't be changed - just like with any other
variable with an explicitly given type.

### Vlastnosti údajového typu

All data types have a property `.init` to which they are initialized.
For all integers this is `0` and for floating points it is `nan` (*not a number*).

Integral and floating point types have a `.max` property for the highest value
they can represent. Integral types also have a `.min` property for the lowest value
they can represent, whereas floating point types have a `.min_normal` property
which is defined to the smallest representable normalized value that's not 0.

Floating point types also have properties `.nan` (NaN-value), `.infinity`
(infinity value), `.dig` (number of decimal digits of precisions), `.mant_dig`
(number of bits in mantissa) and more.

Every type also has a `.stringof` property which yields its name as a string.

### Indexy v jazyku D

In D, indexes usually have the alias type `size_t`, as it is a type that
is large enough to represent an offset into all addressable memory - this is
`uint` for 32-bit and `ulong` for 64-bit architectures.

### Výraz `assert`

`assert` is an expression which verifies conditions in debug mode and aborts
with an `AssertionError` if it fails.
`assert(0)` is thus used to mark unreachable code.

### Podrobnejšie

#### Základné odkazy

- [Priradenie](http://ddili.org/ders/d.en/assignment.html)
- [Premenné](http://ddili.org/ders/d.en/variables.html)
- [Aritmetika](http://ddili.org/ders/d.en/arithmetic.html)
- [Plávajúca čiarka](http://ddili.org/ders/d.en/floating_point.html)
- [Základné typy vysvetlené v publikácii _Programming in D_](http://ddili.org/ders/d.en/types.html)

#### Pokročilé odkazy

- [Prehľad všetkých základných údajových typoch v jazyku D](https://dlang.org/spec/type.html)
- [`auto` a `typeof` vysvetlené v publikácii _Programming in D_](http://ddili.org/ders/d.en/auto_and_typeof.html)
- [Vlastnosti typov](https://dlang.org/spec/property.html)
- [Výraz `assert`](https://dlang.org/spec/expression.html#AssertExpression)

## {SourceCode}

```d
import std.stdio : writeln;

void main()
{
    // V zápise veľkých čísiel možno
    // pre zvýšenie čitateľnosti použiť
    // ako oddeľovač podčiarkovník "_".
    int b = 7_000_000;
    short c = cast(short) b; // pretypovanie
                             // nevyhnutné
    uint d = b; // v poriadku
    int g;
    assert(g == 0);

    auto f = 3.1415f; // f indukuje typ float

    // Výraz typeid(VAR) vracia informáciu
    // o type výrazu VAR.
    writeln("type of f is ", typeid(f));
    double pi = f; // v poriadku
    // implicitné pretypovanie na typ s nižšou
    // presnosťou je povolené pre údajové typy
    // s plávajúcou desatinnou čiarkou
    float demoted = pi;

    // pristupovanie k vlastnostiam
    // údajového typu
    assert(int.init == 0);
    assert(int.sizeof == 4);
    assert(bool.max == 1);
    writeln(int.min, " ", int.max);
    writeln(int.stringof); // int
}
```

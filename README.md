# SeqEqLang
Torl but Lojiban and compiled 2 Sodigy

## Syntax

### constant as leteral.
### dataflow example as English

y
``` plain/text
div x a is b
add 1 y is x
```

y -(argument list as csv)-> example.sdg

### var system

c/a : const/argv

 - `cmd c/a var is c/a`
 - `cmd var c/a is c/a`
 - `cmd c/a c/a is var`
equation solving -> var as ...

solvement map rule

 - `add n var is m` or `add n c/a is m`
-> `var` = `m - n`
 - `add n m is var` -> `var` = `n + m`
 - `div a b is var` -> `var` = `a // b`
 - `div a var is b` -> `dosen't support error`
 - `div var a is b` -> `var` = `a * b`

### how2get div

**I don't sure.**

tempdiv.sdg
```sodigy
@mod(x, y) x % y
@sub(x, y) x - y
@div(x, y) x / y
let func(x, y) = div(sub(x, mod(x, y)), y)
```

is it works?

### how2works?

1. sscanf as `add` form first.
2. if success then compile as `add`, else, try `div`

hashmap that basically strhash->nullptr to save var.
by `hashmaper.h`'s `(char*) nullptrer`, `char* get(char*)`, `char* set(char*)`

at last : write value of filename-var (no var named as filename => ambiguous error)

## umm...

### \[deploymentation\]
python cffi + compiler, deployment as pypi

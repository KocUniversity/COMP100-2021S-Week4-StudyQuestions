## Plesder, do not forget to write a docstring for each function!

## Q1: Making Chocolate :)

We want to make a package of `target` kilos of chocolate. We have small bars (**1 kilo each**) and big bars (**5 kilos each**) and our goal is to sum a varying number of them to obtain `target` kilos.

Write a function `make_chocolate(small_bars, big_bars, target)` where

* `small_bars` is the number of small bars available,
* `big_bars` is the number of big bars available,
* `target` is the number of kilos of chocolate to make.

Return the number of small bars to use, assuming we always use big bars before small bars. Return `-1` if it cannot be done.

```
make_chocolate(4, 1, 9) → 4
make_chocolate(4, 1, 10) → -1
make_chocolate(4, 1, 7) → 2
```

## Q2: Count "Hi"s in a String

Write a function `count_hi(str)` to return the number of times that the string "hi" appears anywhere in the given string `str`.

```
count_hi('abc hi ho') → 1
count_hi('ABChi hi') → 2
count_hi('hihi') → 2
```

## Q3: Cats and Dogs

Write a function `cat_dog(str)` to return `True` if the strings `"cat"` and `"dog"` appear the same number of times in the given string `str`.

```
cat_dog('catdog') → True
cat_dog('catcat') → False
cat_dog('1cat1cadodog') → True
```
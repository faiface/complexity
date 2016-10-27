# Complexity

Time/space/anything complexity measurement utility.

## Foreword on asymptotic complexity

Asymptotic complexity is an incredibly important concept in computer
science. Algorithms are usually judged by their asymptotic complexity,
and though other factors are often important too, complexity tends to
be the most prevalent one.

To learn more about asymptotic complexity and big-O notation (used to
anotate it), visit:

<https://en.wikipedia.org/wiki/Big_O_notation>
<https://en.wikipedia.org/wiki/Computational_complexity_theory>

## What is this program for?

Ever written an algoritm that was slightly more complicated that a
single for-loop and wanted to know it's time or space complexity, but
wasn't quite sure how to calculate it?

Or have ever wanted to just quickly prototype different solutions to
an algorithmic problem and just quickly check their time or space
complexities?

This utility helps you in precisely these kinds of situations.

## What does this program do?

This utility calculates the time or space complexity of your for
you. All you have to do is to measure a simple table of this form:

|      N |         Time |
|:------:|-------------:|
|     10 |   0.04185679 |
|    100 |   0.24053579 |
|   1000 |   3.16843691 |
|  10000 |  41.85855881 |
| 100000 | 522.87088523 |


The `N` column represents the size of the input and the `Time` column
is the time (in whatever unit, e.g. seconds) your program ran for on
the specific input.

Put this data into a file, where each line contains exactly two
number, `N` and `Time`, like this:

```
10 0.04185679
100 0.24053579
1000 3.16843691
10000 41.85855881
100000 522.87088523
```

Now, run the program and see the result!

```
$ complexity < data.txt
O(n log n)
```

Seeeeee?

## How does it work?

This program uses various heurestic methods to search for the right
complexity and verifies the results. Of course, it's not always able
to find the right complexity, mainly if the running times of your
program are not very consistent. However, it works quite reliably in
many cases.

## Why are you talking like it's finished, when it's not?

Yaaa, it will be :) Sooooooon...

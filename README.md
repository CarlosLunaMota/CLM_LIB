# CLM_LIBS

`CLM_LIBS.h`is single header file with a set of code-generating macros for the C preprocessor. Each macro generates the code associated to one of the libraries listed and the end of this document.

<details><summary><strong>What does <em>"code-generating macros"</em> mean?</strong></summary><p></p></details>

<details><summary><strong>Code conventions</strong></summary><p></p></details>

<details><summary><strong>Tests and examples</strong></summary><p></p></details>

<details><summary><strong>Dependencies</strong></summary><p>

All the `CLM_LIBS` are mutually independent. That means that they don't rely on each other to work and that including one of them will never include the others. Moreover, functions inside a given `CLM_LIB` are mutually independent too (with the exception of the `CLM_STREE` library, where some of the functions do rely on the `stree_find`, `stree_min` and `stree_max` functions). In particular, there are no hidden auxiliary functions that do not appear in the lists provided below.

Regarding the C standar library, the `CLM_LIBS.h` header file automatically includes the following headers:

```c
#include <stdlib.h>
#include <string.h>
#include <assert.h>
#include <stdio.h>
#include <time.h>
```
</p></details>

<details><summary><strong>License</strong></summary><p></p></details>

## The CLM Libraries

<details><summary><strong>CLM_TIME</strong></summary><p>

The `IMPORT_CLM_TIME(prefix)` macro generates the following functions:

<details><summary><strong>elapsed</strong></summary><p>

Returns a double with the number of seconds elapsed since the last `start = clock();`.

```c
clock_t MyCrono = clock();
do_something();
printf("do_something takes %.3f seconds.\n", elapsed(MyCrono));
```
</p></details>

<details><summary><strong>get_timestamp</strong></summary><p>

*To Do*

</p></details>
</p></details>

<details><summary><strong>CLM_RANDOM</strong></summary><p></p></details>
<details><summary><strong>CLM_ARRAY</strong></summary><p></p></details>
<details><summary><strong>CLM_CLIST</strong></summary><p></p></details>
<details><summary><strong>CLM_STREE</strong></summary><p></p></details>
<details><summary><strong>CLM_ITERATORS</strong></summary><p></p></details>

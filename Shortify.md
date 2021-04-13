# Memory

Every data structure `T` can is mapped to some pattern *P* of consecutive words.
We write |`T`| for how many words *P* uses. Let variable `v:T` ('v' of type T) have location *X* in memory. Then a variable *Y* at the next avalible location will have memory adress *Y* = *X* + |`T`|

## Memory layout
The primitive types such as `boolen`, `char`, `integer` and `real` are mapped to their corresponding [memory layout](https://medium.com/@shoheiyokoyama/understanding-memory-layout-4ef452c2e709) *B*, *C*, *I*, *R*.
* `boolen` -> *B*
* `char` -> *C*
* `integer` -> *I*
* `real` -> *R*

The layout `A` for an array data structure `A = array[n] of T` is a sequence of *n* concecutive layouts *L*. The size of such an array is |`A`| = *n* ∗|*T*|, and its index range is *i* ∈ {0,1, . . . , *n*−1}. Let *X* be the starting address for an array `myarray:A` ('myarray' of type Array). Then the array index expression `myarray`[ *i* ] maps to the location `myarray`+*i*∗|`G`|. The array uses up memory locations v, . . . , v+n∗|T|−1(inclusive),so the next available location isv+*n*∗|T|.

## Record
Record is the Pascal equivalent of java's class. 

```Pascal
Rec = record x:Type1; y:Type2; z:Type3; end
```
This record contains three fields `x`, `y` and `z` of types `Type1`, `Type2` and `Type3` 

Its layout is the layout `Layout1` of `Type1` followed by the layout `Layout2` of `Type2` followed by `Layout3` of `Type3`

The size of the record is |`Rec`| = |`Type1`| + |`Type2`| + |`Type3`|
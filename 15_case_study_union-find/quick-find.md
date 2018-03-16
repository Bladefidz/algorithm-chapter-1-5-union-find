## Quick-Find {#quick-find}

For example, we want to connecting \(5, 9\) in given vertex below:

| p | q |  | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 5 | 9 |  | 1 | 1 | 1 | 8 | 8 | 0 | 1 | 1 | 8 | 8 |
| **FIND** |  |  |  |  |  |  |  | 0 |  |  |  | 8 |
| **UNION** |  |  | 8 | 8 | 8 | 8 | 8 | 8 | 8 | 8 | 8 | 8 |

To find each vertex, Quick-Find only need lookup its index directly that cost O\(1\) complexity. But, for one connectivity, Quick-Union need to update almost all rows. This algorithm does not aware may 5 is a root or child of 0, so this algorithm just traversing any vertex that connected to 5 and change all of them as child of 9. Because if this scheme, union\(\) take N operation for each connectivity or N^2 for all connectivity in worst case scenario.


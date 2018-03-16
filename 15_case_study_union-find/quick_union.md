## Quick Union {#quick-union}

To increase efficiency in union\(\) operation, we need to aware to construct proper tree representation by find root of each vertex. Take a look for table below:

| p | q |  | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 5 | 9 |  | 1 | 1 | 1 | 8 | 8 | 0 | 1 | 1 | 8 | 8 |
| **FIND** |  |  | - | 1 |  |  |  | - |  |  | 8 | - |
| **UNION** |  |  |  | 8 |  |  |  |  |  |  |  |  |

We need to find each parent of each vertex until found its root. Since height of each tree varies, than the find\(\) operation cost equal to tree height. The union\(\) operation cost only O\(1\) since we have already know each root of tree, then union\(\) only need to connecting root of tree in the left into tree in the right.


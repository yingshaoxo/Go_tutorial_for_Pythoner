#### Codes:
```
package main

import "fmt"

func main() {
    i := 1
    for i <= 10 {
        fmt.Println(i)
        i = i + 1
    }
}
```

#### Output:
```
1
2
3
4
5
6
7
8
9
10
```

#### Conclusion:
The `for` in there, is like Python's `while`.
In other words, is just like `if`, for example: `if i <= 10: do things`.

___

#### Codes:
```
func main() {
    for i := 1; i <= 10; i++ {
        fmt.Println(i)
    }
}
```

#### Conclusion:
This structure is picked up from C++.
You can understand it in this way: for `i == 1`, if `i <= 10`, running following part of codes, then `i = i + 1`.
(for == 对于、基于)
#### Codes:
```
package main

import "fmt"

func add1(x int, y int) int {
    return x + y
}

func add2(x, y int) int {
    return x + y
}

func main() {
    fmt.Println(add1(2, 3))
    fmt.Println(add1(3, 3))
}
```

#### Output:
```
5
6
```

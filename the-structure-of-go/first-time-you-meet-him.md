```
package main

import (
    "fmt"
)

func main() {
    var x string
    x = "Hello"

    y := "world"

    var sentence string = x + ", " + y + "!"

    fmt.Println(sentence)
    fmt.Printf("%s, %s!", y, x)
}
```

##### As you can see, Go is a kind of combination of Python, C++, JavaScript.

1. `package`~~, have no idea yet.~~

2. `func main() {}` is like C or C++ codes structure, which without `;` to determine if a statement was finished.

3. `var x string` is like the way of declaring a variable in JavaScript.

4. `y := "world"` is like Python, in there, the compiler will automatically figure out the variable type without  you to declare.  
    `fmt.Println()` is like Python's `print()`, and revealed the relationship of `Class` and `Function`.




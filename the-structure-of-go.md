```
package main

import "fmt"

func main() {
    var x string
    x = "Hello"
    
    y := "world"
    
    var sentence string = x + ", " + y + "!"
    
    fmt.Println(sentence)
}
```


##### As you can see, Go is a kind of combination of Python, C, JavaScript.

1. ~~`package` is like a further classification for python pakages.~~

2. `func main() {}` is like C or C++ codes part structure without `;` to determine if a statement is finished.

3. `var x string` is like JavaScript for assign a variable.

4. `y := "world"` is like Python, which compiler will know the variable type without you say.
    `fmt.Println()` is like Python's `print()`, and revealed the relationship of `Class` and `Function`.  
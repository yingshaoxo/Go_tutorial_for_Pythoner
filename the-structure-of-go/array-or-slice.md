#### The `Array or Slice`, exactly, is Python's list.
___

```
package main

import (
    "fmt"
    "strings"
)

var words = []string{}

func main() {
    sentence := "I love you guys!"
    
    words = strings.Split(sentence, " ")
    fmt.Printf("%#v\n", words)

    for index, word := range words {
    	fmt.Printf("%d. %s\n", index, word)
    }

    for _, word := range words {
    	fmt.Printf("%s ", word)
    }
}
```
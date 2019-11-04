# Break loop and enumerate

## Break a loop

```text
package main

import "fmt"

func main() {
    i := 0
    for true { //go to infinty
        fmt.Println(i)
        if i == 10 {
            break
        }
        i += 1
    }
}
```

## Enumerate

```text
package main

import (
    "fmt"
    "strings"
)

func traverse_an_array(sentences []string) {
    for index, sentence := range sentences {
        fmt.Printf("\n%d. %s.\n", index, strings.Trim(sentence, ". "))
    }
    // if you don't want to use index, use:
    // for _, sentence := range sentences
}

func main() {
    poem := `Welcome to part 12 of the Go programming tutorial series, where we're going to cover looping/iterating in Go. Leading up to this, we've been working on a project that aggregates news. We're at the point where we have a list of sitemaps that we want to iterate over in order to visit. In the Go language, there is only the "for" loop, there is no "while" statement, but we can still mimic what we might traditionally put in a while loop.`
    sentences := strings.Split(poem, ". ")
    traverse_an_array(sentences)
}
```


# Dict \(Map\)

## The map, exactly, is Python's dictionary.

### Golang version

```text
package main

import "fmt"

func iterate_map_A(A map[string]string) {
    for key, value := range A {
        fmt.Println(key, value)
    }
}

func iterate_map_B(A map[string]int) {
    for key, value := range A {
        fmt.Println(key, value)
    }
}

func main() {
    mapA := make(map[string]string)
    mapA["anyone"] = "lacks of patience" 
    mapA["that's"] = "bad" 
    iterate_map_A(mapA)

    fmt.Println("")

    mapB := map[string]int{"me": 100, "you": 0}
    iterate_map_B(mapB)
}
```

### Python version

```text
def iterate_dict(a_dict):
    for index, value in a_dict.items():
        print(index, value)

dict_A = dict({'anyone': 'lacks of patience', "that's": "bad"})
iterate_dict(dict_A)

print('\n')

dict_B = dict({"me": 100, "you": 0})
iterate_dict(dict_B)
```

## What if we want a type of `dict-list` combination?

```text
package main

import (
    "fmt"
)

var dict_list = make(map[int][]string)

func main() {
    dict_list[1] = []string{"Everyone", "one"}
    dict_list[2] = []string{"can", "be"}
    dict_list[3] = []string{"its", "own", "god."}

    fmt.Println(dict_list)

    for key, list := range dict_list {
        for _, word := range list {
            if key <= 3 {
                fmt.Printf("%s ", word)
            }
        }
    }
}
```


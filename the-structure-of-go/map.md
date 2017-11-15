#### The map, exactly, is Python's dictionary.
___

##### Golang version
```
package main

import "fmt"

func iterate_map_A(A map[string]string) {
    for idx, value := range A {
        fmt.Println(idx, value)
    }
}

func iterate_map_B(A map[string]int) {
    for idx, value := range A {
        fmt.Println(idx, value)
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


##### Python version
```
def iterate_dict(a_dict):
    for index, value in a_dict.items():
        print(index, value)

dict_A = dict({'anyone': 'lacks of patience', "that's": "bad"})
iterate_dict(dict_A)

print('\n')

dict_B = dict({"me": 100, "you": 0})
iterate_dict(dict_B)
```
Golang's struct is just like C++'s struct.

```
package main

import ("fmt"
        "reflect"
)

type box struct {
    length int16
    width int16
    hight int16
}

func main(){
    a_box := box{length: 3, width: 2, hight: 1}
    another_box := box{3, 2, 1} //if you got varible well_named, this way just fine

    fmt.Println(a_box.length)
    fmt.Println(another_box.width)
}
```
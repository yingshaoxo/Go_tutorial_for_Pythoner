I can't believe it when `sentdex` tell me that Golang doesn't have `class methods`.

But soon I know what's the big idea.
___

##### Python Version
```
package main

import "fmt"


type box struct {
    length int16
    width int16
    hight int16
}

func (b box) get_volume() int16 {
    return b.length * b.width * b.hight
}

func main(){
    box_a := box{length: 3, width: 2, hight: 1}
    box_b := box{length: 4, width: 2, hight: 2}

    fmt.Println("The volume of box_a is", box_a.get_volume())
    fmt.Println("The volume of box_b is", box_b.get_volume())
}
```

##### Golang Version
```
package main

import "fmt"


type box struct {
    length int16
    width int16
    hight int16
}

func (b box) get_volume() int16 {
    return b.length * b.width * b.hight
}

func main(){
    box_a := box{length: 3, width: 2, hight: 1}
    box_b := box{length: 4, width: 2, hight: 2}

    fmt.Println("The volume of box_a is", box_a.get_volume())
    fmt.Println("The volume of box_b is", box_b.get_volume())
}

```

This is the basic way for class method.

___

You can also pass pointer to class function:

```
package main

import "fmt"

type box struct {
    length int16
    width int16
    hight int16
}

func (b *box) get_volume() int16 {
    return b.length * b.width * b.hight
}

func main(){
    box_a := box{length: 3, width: 2, hight: 1}

    fmt.Println("The volume of box_a is", box_a.get_volume())
}
```

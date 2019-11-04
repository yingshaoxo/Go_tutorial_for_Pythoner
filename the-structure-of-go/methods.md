# Class \(Methods\)

I can't believe when `sentdex` tell me that Golang doesn't have `class methods`.

But soon I know what's the big idea under the mystery.

## Python Version

```text
class box():
    def __init__(self, length, width, hight):
        self.length = length
        self.width = width
        self.hight = hight

    def get_volume(self):
        return self.length * self.width * self.hight

box_a = box(3, 2, 1)
box_b = box(4, 2, 2)
print('The volume of box_a is', box_a.get_volume())
print('The volume of box_b is', box_b.get_volume())
```

## Golang Version

```text
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

You can also pass pointer to class function:

```text
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


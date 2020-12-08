# List \(Array or Slice\)

```go
package main

import (
	"fmt"
	"strings"
)

func main() {
	sentence := "I love you guys!"

	words := strings.Split(sentence, " ")
	fmt.Printf("%#v\n", words)

	for index, word := range words {
		fmt.Printf("%d. %s\n", index, word)
	}

	for _, word := range words {
		fmt.Printf("%s ", word)
	}
}
```

```go
package main

import (
	"fmt"
)

//var nums = make([]int, 0) //this is a slice, it's a dynamic array
var nums []int

func main() {
	fmt.Printf("%#v\n", nums)

	nums = append(nums, 1)
	nums = append(nums, 9)
	nums = append(nums, 9)
	nums = append(nums, 8)

	fmt.Printf("%#v\n", nums)

	nums[len(nums)-1] = 0
	nums = nums[:len(nums)-1]

	fmt.Printf("%#v\n", nums)
}
```


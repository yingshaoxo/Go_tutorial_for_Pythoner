# Go modules

## Make a folder

for example: `godream`

## Initiate go mod

```bash
go mod init github.com/yingshaoxo/godream
```

## Add a package

any package would be fine.

```bash
go get -u github.com/fogleman/gg
```

## Check your go.mod file

you shall see something new inside of it.

## Add your code

add a `main.go` file:

```go
package main

import (
	"log"

	"github.com/fogleman/gg"
)

func main() {
	var W = 500
	var H = 500
	dc := gg.NewContext(W, H)
	if err := dc.LoadFontFace("font.ttf", 42); err != nil {
		panic(err)
	}

	const line_space = 1.5

	const text = "yingshaoxo is the best person in this world! \n no one can default him!"

	w, h := dc.MeasureMultilineString(text, line_space)
	log.Printf("w%f, h%f\n", w, h)

	W = int(w / 2)
	H = int(h)

	dc = gg.NewContext(W, H)
	dc.SetRGB(1, 1, 1)
	dc.Clear()
	dc.SetRGB(0, 0, 0)

	dc.DrawStringWrapped(text, float64(W)/2, float64(H)/2, 0.5, 0.5, float64(W), line_space, gg.AlignCenter)

	dc.SavePNG("out.png")
}
```

## Build your module

```bash
go build
```

It will resolve all of your dependencies and build your module as a single binary for you.

## Use your program

```bash
./godream
```


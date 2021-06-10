# Packages

## Example

[https://yingshaoxo.blogspot.com/2021/06/how-to-create-package-with-golang.html](https://yingshaoxo.blogspot.com/2021/06/how-to-create-package-with-golang.html)

```bash
go env -w  GOPROXY=https://goproxy.io
```

Like `Python`, sometimes, you want to separate your codes to different files.

So it can be organized.

In Python, you use `import` to load function from `.py file`.

In Golang, you will also use `import` to load function from `.go file`.

But `Golang` file structure is different.

For example，a tree of a project may look like this:

```text
src
├── hi
│   └── a_go_file.go
└── main.go
```

```go
//a_go_file.go
package hi

import "fmt"

func init() {
    fmt.Println("You are runing init() function from hi package")
}

func Say_hello() {
    fmt.Println("You are runing Say_hello() function from hi package")
}
```

```go
//main.go
package main

import (
    "./hi"
    "fmt"
)

func main() {
    fmt.Println("You are runing main() function from main package.")
    hi.Say_hello()
}
```

If you run `main.go`，you'll get:

```text
You are runing init() function from hi package
You are runing main() function from main package.
You are runing Say_hello() function from hi package
```

That tells us some facts:

1. `golang` package was separated by `folder`. In that folder, all your `.go file` must declare the `package name` by `package *`
2. you can `import` your own packages from `main.go` with `./your_package_name`
3. before golang import any package, it will run the `init()` function first
4. if you want to export or use a function from a package, the first character of that `function name` must keep capitalizing.

Sometimes, people would like to put all their source codes to `~/go/src`

In that case you will import a package using `github.com/yourname/projectname`

It's good to do with if you don't want to handle the `folder-file structure` with `relative import`

And by doing so, vim `YouCompleteMe` could be able to work correctly

> By the way, in case you don't know: use \`go get ./...\` to install all missing packages for a Go project.


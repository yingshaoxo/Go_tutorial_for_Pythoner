```
package main

import ("fmt"
        "net/http")

func index_handler(w http.ResponseWriter, r *http.Request) {
    fmt.Fprintf(w, "Hello, yingshaoxo!")
}

func about_handler(w http.ResponseWriter, r *http.Request) {
    fmt.Fprintf(w, "This is based on Golang.")
}

func main() {
    http.HandleFunc("/", index_handler)
    http.HandleFunc("/about/", about_handler)

    fmt.Println("http://127.0.0.1:5000")
    http.ListenAndServe(":5000", nil)
}
```

It's much like python's flask package:

`/` for index of website.

`/about/` for about page.
___

There just one thing you should care about: `*`.

It reads value from a point address (`http.Request`).
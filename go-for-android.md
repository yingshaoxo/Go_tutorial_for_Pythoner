# Go for Android

> `Cython` could do the same thing by convert python to c, then c to binary.

## First, you should write a program at `~/go/github/yingshaoxo/hi/main.go`

```text
package greeting

func SayHi() string {
    return "Hi!"
}
```

> Capitalize the function name, so golang would treat that function as public.

## Then, compile it to binary file

```text
go get golang.org/x/mobile/cmd/gomobile
gomobile init
```

```text
gomobile bind -target=android
```

> If it ask for NDK, install it and make sure the Environmental-Variable was set right.

If everything was right, you'll get two files: `greeting.aar` and `greeting-sources.jar`

## Let's import it to Android Studio Project

1. Let's assume you have a project which was named `ABI_Test`
2. `mkdir ABI_Test/app/libs`
3. `mv greeting.aar ABI_Test/app/libs/` and `mv greeting-sources.jar ABI_Test/app/libs/`
4. add `implementation fileTree(dir: 'libs', include: ['*.jar', '*.aar'])` to `ABI_Test/app/build.gradle`
5. rebuild the project

## Let's use it with the following codes

```text
import greeting.Greeting

var words = Greeting.sayHi()
Toast.makeText(applicationContext, words, Toast.LENGTH_LONG).show()
```

## The real codes

```text
import greeting.Greeting

class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        var words = Greeting.sayHi()
        Toast.makeText(applicationContext, words, Toast.LENGTH_LONG).show()
    }
}
```


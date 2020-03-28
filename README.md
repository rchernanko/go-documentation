#Go documentation

- Notes based on go-udemy course - https://github.com/rchernanko/go-udemy

##Introduction:

###`go doc` command:
- command to read documentation at the command line 
    - `go doc fmt`

###`godoc` command:
- to run a local server showing documentation (e.g. if you're offline)

##go doc command:

- `go doc` prints the documentation for a package, const, func, type, var, or method
    - go doc accepts zero, one, or two arguments.
        - zero
            - prints package documentation for the package in the current directory
                - `go doc`
        - one
            - `go doc Foo`, `go doc encoding/json`, `go doc json.Number`
        - two
            - first argument must be a full package path
                - `go doc pkg text/template new` (show doc for text/template's New function)

- `go help doc` for more info

##godoc command:

- `godoc -http=:8080`
- Then I can launch a web browser on that port, and view all the documentation - `http://localhost:8080/`

##Writing documentation
- Works via comments you add to your code - see `01/hello/world/main.go`  and the comments above package and exportable function declarations
- If you have lots and lots of comments above your package declaration - create a `doc.go` file e.g. https://golang.org/src/fmt/doc.go
- If the code is in your go workspace (mine currently isn't), you can launch the local web server and you should see the docs for your source code in the package documentation
- More info - https://blog.golang.org/godoc
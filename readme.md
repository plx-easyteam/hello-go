# _Intro_ to Go

## Init:

> Create a module in which you can manage dependencies.

Run the go mod init command, giving it the path of the module your code will be in.

```sh
go mod init <module-path>
```

The go mod init command’s argument is your module’s module path. If possible, the module path should be the repository location of your source code.

See: <a href="https://go.dev/doc/modules/managing-dependencies#naming_module">naming module</a>

> Create `main.go` file

Add package declaration

```go
package main
```

> Follow tutorial...

Import the packages you’ll need to support the code

```go
import (
    "net/http"

    "github.com/gin-gonic/gin"
)
```

> Begin tracking the Gin module as a dependency.

At the command line, use go get to add the github.com/gin-gonic/gin module as a dependency for your module. Use a dot argument to mean “get dependencies for code in the current directory.”

```sh
go get .
```

Go resolved and downloaded this dependency to satisfy the import declaration you added

> From the command line in the directory containing main.go, run the code. Use a dot argument to mean “run code in the current directory.”

```sh
go run .
```

---

Tutorial Source:
<a href="https://go.dev/doc/tutorial/web-service-gin">Developing a RESTful API with Go and Gin</a>

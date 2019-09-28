## Snippets for Visual Studio Code

These are some of the [custom snippets](https://code.visualstudio.com/docs/editor/userdefinedsnippets) I'm using for [Visual Studio Code](https://code.visualstudio.com).

### How to install

Just place the desired Go file in:

- macOS: ~/Library/Application Support/Code/User/snippets
- Windows: 

### Go Snippets

For [Go](https://golang.org), I have two snippets defined:

#### `tcimp`

You can use the `tcimp` snippet to quickly add the basic imports needed for writing a test.

It uses the [`testing`](https://golang.org/pkg/testing/) and [`assert`](https://github.com/stretchr/testify#assert-package) libaries.

Just type `tcimp` and you'll get the following snippet:

```go
import (
	"testing"

	"github.com/stretchr/testify/assert"

	"github.com/<package>"
)
```

#### `tc`

Typing `tc` sets up the basic structure for an empty test and results in:

```go
func Test_<name>(t *testing.T) {

	type test struct {
		name string
	}

	var tests = []test{}

	for _, tc := range tests {
		t.Run(tc.name, func(t *testing.T) {
		})
	}

}
```
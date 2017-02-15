# SizeStruct
Recommended test use only.<br> 
Can't nest pointer.<br> 

###For example：

```go
package main

import (
	"github.com/Re-volution/sizestruct"
)

type test struct {
	a int
	b string
	c map[string]int
}

func main() {
	var data = new(test)
	sizestruct.SizeStruct(data)
}
```

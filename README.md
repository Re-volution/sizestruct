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
	a int32
	b string
	c map[string]int
	d int64 `ss:"-"`
}

func main() {
	var data = new(test)
	sizestruct.SizeStruct(data)
}
```
This example will not be calculated the size of the "d".

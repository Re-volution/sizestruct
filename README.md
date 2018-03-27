# SizeStruct
Recommended test use only.<br> 
目前只是测试阶段使用.<br> 
Can't nest pointer.<br> 
不可以有重复的指针.<br> 

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
This example will not be calculated the size of the "d".<br> 
这个例子中不会计算字段 'd' 的大小.<br> 

没有计算结构体字段名字的长度大小。<br> 

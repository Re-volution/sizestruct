# SizeStruct
At present, it is only used in the test phase. There may be some problems.<br> 
目前只是测试阶段使用.可能会有些问题<br> 
Can have nest pointer.<br> 
可以有重复的指针.<br> 
There is no statistics on the size of chan and func.<br>
对chan、func的大小没有统计.<br> 

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
	sizestruct.SizeOf(data)
	sizestruct.SizeTOf(data)//Including type size 包括type的大小
}
```
This example will not be calculated the size of the "d".<br> 
这个例子中不会计算字段 'd' 的大小.<br> 

可以计算结构体字段名字的长度大小。<br> 

修改了函数名<br> 

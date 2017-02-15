# SizeStruct
Recommended test use only.
Can't nest pointer.

For example：

package main

import (
  "sizestruct"
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

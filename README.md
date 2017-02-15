# SizeStruct
Recommended test use only.<br> 
Can't nest pointer.<br> 

###For example：

package main<br> 

import (<br> 
	"sizestruct"<br> 
)<br> 

type test struct {<br> 
	a int<br> 
	b string<br> 
	c map[string]int<br> 
}<br> 

func main() {<br> 
	var data = new(test)<br> 
	sizestruct.SizeStruct(data)<br> 
}

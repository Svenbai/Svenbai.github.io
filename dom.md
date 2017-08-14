# DOM 
***
#### 按照层级的形式划分:父节点、子节点、兄弟节点#### 按照节点类型划分: 1元素节点、2属性节点、3文本节点、8注释节点、9document节点	nodeType 返回节点的类型	nodeName 返回节点名称	nodeValue 返回节点的值## 获取子节点：
#### 1.children/childNodes 获取指定元素的第一层子节点
` 区别：`

	children 在标准浏览器和IE9下，不会造成空白文本解析，获取到的是真实的子节点，不支持IE6、7、8  
	childNodes 会解析空白文本节点 
#### 2.firstChild/firstElementChild  获取指定元素的最后一个子节点
` 区别：`		firstChild 在标准和ie9下会获取到空白文本节点	firstElementChild 标准下获取第一个子元素节点，ie6/7/8不支持。`
#### 3.	lastChild/lastElementChild 获取指定元素的最后一个子节点` 区别：`
	lastChild : 最后一个子节点 在标准和ie9下会获取到空白文本节点。    lastElementChild : 标准下获取最后一个子元素节点，ie6/7/8不支持。#### 4.	previousSibling/previousElementSibling 获取指定元素的上一个兄弟节点#### 5.	nextSibling/nextElementSibling 获取指定元素的下一个兄弟节点
***## 获取父节点：#### 1.parentNode 获取指定元素的父节点
#### 2.offsetParent 获取离指定元素最近的具有定位属性的祖先节点
` 以上两个属性都是把获取到的元素结构整体返回，不仅仅只是返回一个标签`
#### 3.offsetWidth  width + border + padding
#### 4.clientWidth  width + padding
***## 获取元素属性：
#### 1.元素.属性名  获取不到非标准属性
注：如果获取的是元素的class的话，在写的时候必须是className
#### 2.["属性名"] 同上
#### 3.getAttribute("属性名")  获取元素属性 可以获取到元素的自定义属性 可以直接写class不用写className
 ` setAttribute("属性名","属性值")  设置元素属性`
`  removeAttribute("属性名")  移除元素属性`
#### 4.attributes能访问到元素上所有属性，返回的是一个类数组，可以通过下标的形式拿到每一个属性***
## 增删改查：#### 1.创建节点 document.createElement("标签名")
#### 2.appendChild() 给指定元素追加子节点
#### 3.插入元素 insertBefore(插入的元素，参照元素)
#### 4.removeChild() 移除子节点
#### 5.replaceChild(替换元素，被替换元素) 替换子节点
#### 6.cloneNode() 克隆节点  接受一个布尔值作为节点
` 当参数为true时，会克隆元素的innerHTML，false不会,默认是false`#### 7.hasChildNodes()  判断指定元素是否拥有子节点，返回布尔值true或false
#### 8.childNodes 获取元素所有的子节点，包括空白文本节点
#### 9.children 获取元素所有子节点，不包括空白文本节点***
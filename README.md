# drag_demo
拖拽功能-html demo 


1. event = event || window.event // 处理浏览器 event 兼容性问题
2. 浏览器默认行为. 可以通过  return false  来取消默认行为


3. 想要拖动元素, 需要设置元素为absolute 绝对定位, 否则拖不动(重要)

拖拽元素
1. 鼠标在被拖拽元素上按下时, 开始拖拽 onmousedown
2. 当鼠标移动时, 被拖拽元素跟随鼠标移动 onmousemove
3. 当鼠标松开时, 被拖拽元素固定在当前位置 onmouseup

ie8问题
* setCapture()
* - 只有IE 支持, 但是在火狐中调用时不会报错
*   而如果使用chrome调用,会报错

* releaseCapture()
* - 只有IE 支持, 但是在火狐中调用时不会报错
*   而如果使用chrome调用,会报错

判断浏览器有无该事件在去使用
object.setCapture&& object.setCapture() 
object.releaseCapture&& object.releaseCapture() 

取消事件绑定  = null
- * 取消document的onmousemove事件
  document.onmousemove = null        
- * 取消document的onmouseup事件
  document.onmouseup = null
- 鼠标的水平偏移量      
var left = event.clientX
- 鼠标的垂直偏移量
var top = event.clientY

- * div 偏移量   鼠标.clientX - 元素 . offsetLeft
- * div 偏移量   鼠标.clientY - 元素 . offsetTop
- var ol = event.clientX - box1.offsetLeft // offsetLeft
- var ot = event.clientY - box1.offsetTop // offsetTop
   

05.拖拽(提取函数).html
![](https://github.com/dL-hx/PicgoData/blob/master/drag_demo/%E6%8B%96%E6%8B%BD.png?raw=true)

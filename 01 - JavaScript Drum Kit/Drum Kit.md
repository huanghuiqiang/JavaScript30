# 思路

1. 敲击键盘，获取对应的 DOM 元素
2. 播放音频
3. 改变样式

# 难点

## 如何将键盘按键和页面按钮相互关联？

使用事件委托，监听<code>keydown</code>事件，能够通过<code>keyCode</code> 获得对应的键盘值。<br>
使用<code>document.querySelector</code>获取页面上对应的元素。<br>

注：<br>
<code>keydown</code>和<code>keyup</code>分别表示键盘按下、弹起来，触发的事件。<br>
<code>keypress</code>表示的则是能够生成字符的才会触发事件。比如：<code>shift</code><code>ctrl</code>就不会触发<code>keypress</code>事件<br>

## 如何播放音频？

使用 <code>play()</code> 方法

## 如何解决无法连续敲击的问题？

添加<code>currentTime</code>属性,设置为<code>0</code><br>
表示将播放时间戳改为初始位置。

## 如何解决样式无法恢复的问题？

<code>transitionend</code> 事件会在 <code>CSS transition</code> 结束后触发。
在触发该事件后，利用<code>propertyName</code>属性找到对应的元素，取消高亮样式。

# 思路

1. 通过监听<code>change</code>事件和<code>mousemouve</code>事件，获得变化后的元素
2. 将获得的元素，给到图片上
3. 这里能够通过<code>：root</code>设置全局 CSS 变量, 这样就只用修改一处了

# 难点

# 如何获得变量值

可以用点击事件的参数<code>Event</code>。
但这里用<code>this</code>对象会更好
这里通过 this 对象

# 如何处理不同 CSS 属性单位的问题？

自定义数据<code>data-</code>,里面包含了之前设定的值。
能沟通通过<code>dataset </code>访问得到。这样就能够获得不同的单位

## 如何用 JavaScript 改变属性值

<code>:root</code>是匹配根目录<code>HTML</code>,所以要用
<code>document.documentElement</code> 来获取全局 DOM。
<code> document.documentElement.style.setProperty('--blur', '0px')</code>

# 知识点

CSS 变量、伪类、自定义数据类型

## 什么是伪类？

伪类只能够根据元素的状态选择，而不能够根据 DOM 对象选择。<br>
<code>:first-child, :last-child</code>
行为类<code>:hover</code>

## 什么是伪元素？

通过状态来表示的元素
<code>::after, ::before, ::first-line, ::first-letter, ::selection</code>

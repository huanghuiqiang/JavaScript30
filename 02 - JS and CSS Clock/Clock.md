# 思路

1. 获取当前时间，计算出旋转角度
2. 给三个指针添加旋转样式
3. 设置定时器，定时旋转

# 难点

如何使用 JS 设置 CSS 样式？
使用<code>style</code>设置属性<br>
<code>element.style.height = '100px'</code><br>
使用<code>setAttribute</code>设置属性<br>
<code>setAttribute('style', 'padding: 100px; background: red')</code>

如何使指针围绕中心旋转？
使用 <code>transform: rotate(45deg)</code>设置元素旋转

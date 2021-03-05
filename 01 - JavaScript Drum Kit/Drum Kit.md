# 重点知识

## getAttribute

## 键盘元素 <kbp>

## audio

## 事件委托

# 难点

如何将元素和音频相互关联

在<code>div</code>元素上绑定点击事件，<code>keydown</code> 未生效。
解决思路：绑定事件委托事件。

e.keyCode 获得键盘元素的按键

如何触发音频的自动播放？
解决思路：使用<code>autoplay</code> <code>play()</code>

如何获取音频列表中对应的元素

如何解决无法连续敲击的问题？
解决方式：添加<code>currentTime</code>属性
<code>currentTime</code>

作用：todo

js 插入样式 playing

如何在点击之后，删除样式

propertyName

```
问题：无法连续敲击键盘，也没有高亮样式

  window.addEventListener('keydown', function(e) {
    const keyCode = e.keyCode + '' || '';
    let audioList = document.getElementsByTagName('audio');
    for (let i = 0; i < audioList.length; i++) {
      const audioNum = audioList[i].getAttribute('data-key');
      if (keyCode === audioNum) {
        audioList[i].play()
      }
    }
  })
```

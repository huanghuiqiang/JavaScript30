# 数组去重的方法

<code></code>

## <code>Array.from(new Set([1,1,2,2]))</code>

## reduce

```
[1,1,1,2,2].reduce((acc, cur) => {
  if (acc.indexOf(cur) === -!) {
    acc.push(cur)
  }
  return acc
}, [])
```

## 排序 + 双指针

# 实现`Array.prototype.some`

## 代码
```javascript
// write code here
Array.prototype.some = function(fun) {
  let flag = false
  if(typeof(fun) === 'function') {
    for(var i = 0; i < this.length; i++) {
      flag = fun(this[i])
      if (flag) {
        flag = true
        break
      }
    }
    return flag
  }
}

```
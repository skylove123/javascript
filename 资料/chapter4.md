字符串的使用

```javascript
let bigmouth = 'I \'ve got no right to take my place...';
console.log(bigmouth)  // \转义字符

let one = 'Hello, ';
let two = 'how are you?';
let joined = one + two;
let j = `${one}${two}` //连接两个字符, 叫literal
console.log(joined)
console.log(j)
```

```javascript
var a = 'I am good'
var b = 12
console.log(a + b) // 编译器自动把字符串连起来
console.log(b + a)

var c = "13"
var k = "18"
console.log(c + k) // 如果不转换，直接当成字符串连接起来
console.log(Number(c) + Number(k))  //Number（） 把字符串转换成数字

```

```javascript
let browserType = 'mozilla';
console.log(browserType.length) //打印字符串的长度
console.log(browserType[0]) // 打印第一个字符
console.log(browserType.indexOf('zilla')) // 打印够小的字符串从哪里开始，返回开始位置, 返回2
console.log(browserType.indexOf('vanilla')) // 如果没找到就返回-1， -1是没找到里面存在这个字符串
console.log(browserType.slice(0, 3)) // 截取字符串，从0开始，但不包挂3, 返回moz
console.log(browserType.toLowerCase()) // 转换成小写
console.log(browserType.toUpperCase()) // 转换成大写
console.log(browserType.charAt(6)) // 返回位置第6的字符， char是字符的意思，at是在哪里
console.log(browserType.substring(1)) // 截取从1位置开始，包挂1位置
console.log(browserType.substring(0, 3)) // 截取从0开始，但不包挂3的位置， 和slice(0, 3)一样效果
console.log(browserType.replace("mo", "to")) // 替代字符串
console.log(browserType.repeat(2)) //重复打印2次
console.log(browserType.includes("zilla1")) // 检查这个字符串是否存在， 如果存在返回true，如果不包挂返回false, 和indexOf有点区别
```


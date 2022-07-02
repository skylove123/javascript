javascript 变量（variable）



## [1. 声明变量](https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First_steps/Variables#声明变量)

要想使用变量，你需要做的第一步就是创建它 -- 更准确的说，是声明一个变量。声明一个变量的语法是在 `var` 或 `let` 关键字之后加上这个变量的名字：

```javascript
let myName;
var myAge;
```

## 2. [初始化变量](https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First_steps/Variables#初始化变量)

一旦你定义了一个变量，你就能够初始化它。方法如下，在变量名之后跟上一个“=”，然后是数值：

```
var myName = 'Chris';
let myAge = 37;
```

## [3. var 与 let 的区别](https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First_steps/Variables#var_与_let_的区别)

1.  **作用域不同**(scope)

   ```javascript
   for(var i = 0; i < 2; i++){}
   console.log(i)  // print 2
   for(let j = 0; j < 2; j++){}
   console.log(j) // print undefined
   
   ```

   

2.  Let 不能再定义, var 可以

   ```javascript
   let a = 100
   console.log(a)
   let a = 200  // 出错，不能重新定义
   console.log(a)
   ```

   ```javascript
   var a = 100
   console.log(a)
   var a = 200  // 不出错，但不建议这么做， 直接a=200就行
   console.log(a)
   ```

   

   3. let 不能在定义前访问变量， 但var 可以， 显示undefined

   ```javascript
   console.log(a)
   a = 200
   var a   // undefined
   ```

   ```javascript
   console.log(a)
   a = 200
   let a  // ReferenceError: Cannot access 'a' before initialization
   ```

   

3. 变量提升(hoisting), var可以变量提升，但let不可以

   ```javascript
   function do_something() {
     console.log(bar); // undefined
     var bar = 111;
     console.log(bar); // 111
   }
   
   // 可以隐式地将以上代码理解为：
   
   function do_something() {
     var bar;
     console.log(bar); // undefined
     bar = 111;
     console.log(bar); // 111
   }
   ```

   

   5. 变量的类型

      ### [Number](https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First_steps/Variables#number)

      你可以在变量中存储数字，不论这些数字是像 30（也叫整数）这样，或者像 2.456 这样的小数（也叫做浮点数）。与其他编程语言不同，在 JavaScript 中你不需要声明一个变量的类型。当你给一个变量数字赋值时，不需要用引号括起来。 

      ```
      let myAge = 17;
      ```

      Copy to Clipboard

      ### [String](https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First_steps/Variables#string)

      字符串是文本的一部分。当你给一个变量赋值为字符串时，你需要用单引号或者双引号把值给包起来，否则 JavaScript 将会把这个字符串值理解成别的变量名。

      ```
      let dolphinGoodbye = 'So long and thanks for all the fish';
      ```

      Copy to Clipboard

      ### [Boolean](https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First_steps/Variables#boolean)

      Boolean 的值有 2 种：true 或 false。它们通常被用于在适当的代码之后，测试条件是否成立。举个例子，一个简单的示例如下： 

      ```
      let iAmAlive = true;
      ```

      Copy to Clipboard

      然而实际上通常是以下用法：

      ```
      let test = 6 < 3;
      ```

      Copy to Clipboard

      这是使用“小于”操作符（<）来测试 6 小于 3。正如你所料的，将会返回`false`，因为 6 并不小于 3！在这个课程中，以后你将会学到许多有关操作符的知识。

      ### [Array](https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First_steps/Variables#array)

      数组是一个单个对象，其中包含很多值，方括号括起来，并用逗号分隔。尝试在您的控制台输入以下行：

      ```
      let myNameArray = ['Chris', 'Bob', 'Jim'];
      let myNumberArray = [10,15,40];
      ```

      Copy to Clipboard

      当数组被定义后，您可以使用如下所示的语法来访问各自的值，例如下行：

      ```
      myNameArray[0]; // should return 'Chris'
      myNumberArray[2]; // should return 40
      ```

      Copy to Clipboard

      此处的方括号包含一个索引值，该值指定要返回的值的位置。您可能已经注意到，计算机从 0 开始计数，而不是像我们人类那样的 1。

      在以后的文章，你将更多地了解数组。

      ### [Object](https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First_steps/Variables#object)

      在编程中，对象是现实生活中的模型的一种代码结构。您可以有一个简单的对象，代表一个停车场，并包含有关其宽度和长度的信息，或者您可以有一个代表一个人的对象，并包含有关他们的名字，身高，体重，他们说什么语言，如何说 你好，他们，等等。

      尝试在您的控制台输入以下行：

      ```
      let dog = { name : 'Spot', breed : 'Dalmatian' };
      ```

      Copy to Clipboard

      要检索存储在对象中的信息，可以使用以下语法：

      ```
      dog.name
      ```

      Copy to Clipboard

      我们现在不会看对象了 - 您可以在将来的模块中了解更多关于这些对象的信息。

      ## [动态类型](https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First_steps/Variables#动态类型)

      JavaScript 是一种“动态类型语言”，这意味着不同于其他一些语言 (译者注：如 C、JAVA)，您不需要指定变量将包含什么数据类型（例如 number 或 string）

      例如，如果你声明一个变量并给它一个带引号的值，浏览器就会知道它是一个字符串：

      ```
      let myString = 'Hello';
      ```

      Copy to Clipboard

      尝试依次将上述代码输入您的控制台，看看结果是什么（无须输入//之后的注释）。我们使用了一个名为`typeof`的特殊的操作符 ——它会返回所传递给它的变量的数据类型。第一次在上面的代码中调用它，它应该返回 string，因为此时 myNumber 变量包含一个字符串'500'。看看它第二次将返回什么。

      ```javascript
       let n = 100
       let m  = true
       console.log(typeof(n))
       console.log(typeof(m))
      ```

      

      ```javascript
       var n = 16  // number
       var s = "are you ok?"  //string
       var b = true  // boolean true/false
       console.log("n is " + n + "," + "s is " + s + "," + "b is " + b) // 不推荐使用
       console.log(`n is ${n} , s is ${s}, b is ${b}`) // 推荐使用
       let myNameArray = ['Chris', 'Bob', 'Jim']; // array,数组类型, index is from 0
       console.log(myNameArray[0])
       console.log(myNameArray.length)  // 打印数组长度
       let dog = { name : 'Spot', breed : 'Dalmatian' };  // key: value  , example: name is key, spot is value, json格式
       console.log(dog.name + "," + dog.breed)  // 这种简单一点
       console.log(dog['name'] + "," + dog['breed']) // 这种也可以
          
      ```

​             

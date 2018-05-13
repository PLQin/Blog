# 变量
## 这就是javaScript中的变量
ECMA-262的表述是javascript变量与其他编程语言的变量有着很大的区别，javascript的变量是
松散的，这个本质也就决定变量他只是在特定时间存放特定值的名称而已。由于他不会向其他语言
受变量必须要保存何种数据类型的值的约束。所以它的变量可以在脚本的生命周期更改变量值以及
变量的类型。
```js
var num = 1; //Number
console.log(typeof num);
num = '2'; // String
console.log(typeof num);
num = true; // 布尔值
console.log(typeof num); 

//代码一 变量本质
```
上述代码可以说明了javascript变量本质。会发现在变量名的前面不需要像C、C++一样要在前面就
要确定变量的数据类型，而且它会在生命周期中更改变量的数据类型。这就是一个松散的javascript
变量。

## 基本类型(原始值)和引用类型
在ECMAscript中包含了两种不同的数据类型：基本类型与引用类型

基本类型：保存在变量对象中（作用域会说明），能够操作保存在变量中实际的值，包括了5种基本数据类型String,Number,Boolean,Undefined,Null(ES6中新加的Sybmol).,它们是按值进行访问的。

引用类型：是保存在内存中(堆内存)的对象。由于javaScript不能够直接访问内存中的位置，也就是说不能直接操作对象的内存空间。也就说我们在操作对象的时候，实际上操作的不是对象本身而是指向对象内存空间的一个地址引用。

动态创建属性适用于基本类型与引用类型。只不过对于基本类型来说创建属性的过程就相当于销毁这个属性。
```js
var name = 'xuhh';
name.age = 22;  // 22  不过在这里这个属性会被立即销毁掉
console.log(name.age);  // undefined

// 代码二  基本类型创建属性
```

而引用类型创建属性时会将这个属性保存到这个变量中，只要这个变量或是这个属性不被销毁他就会一直保存下去。
```js
var obj = {};  // 创建一个空对象
obj.name = 'xuhh'; //添加一个name属性
console.log(obj.name);  // 'xuhh'  说明属性保存下来了

// 代码三  引用类型创建属性
```
## 关于变量复制与参数的传递
在介绍变量复制之前，需要补充一些东西：基本类型(原始值)是不可变的，引用类型是可变的。（用一个例子来进行解释吧，详细的可以去参照javascript权威指南上的解释）
```js
// 原始值
var name = 'xuhh';  // 创建一个变量，值为原始值
name.toLocaleUpperCase(); // 改变变量的值  值改成大写的
console.log(name);  // 'xuhh'  值没有发生改变

// 对象引用
var obj = {
	name: 'xuhh'
}  // 创建一个变量，值为引用类型
obj.name = 'stone'; //改变变量值
console.log(obj.name);  // 'stone'  发生了改变

// 代码四 基本类型(原始值)是不可变的，引用类型是可变的
```
### 变量复制
基本类型：
### 参数传递
## 检测类型


注解：javascript是一门动态的弱类型编程语言。


## JavaScript 类(class)

**类是用于创建对象的模版.**

我们使用 class 关键字来创建一个类,类体在一对大括号 {} 中,我们可以在大括号 {} 中定义类成员的位置,如方法或改造函数.

每个类中包含了一个特殊的方法 **constructor()**,它是类的构造函数,这种方法用于创建和初始化一个由 **class** 创建的对象.

创建一个类的语法格式如下:

```
class ClassName {
  constructor() { ... }
}
```

```
class Runoob {
  constructor(name, url) {
    this.name = name;
    this.url = url;
  }
}
```

以上实例创建了一个类,名为 "Runoob".

类中初始化了两个属性: "name" 和 "url".

### 使用类

定义好类后,我们可以使用 **new** 关键字来创建对象:

```
class Runoob {
  constructor(name, url) {
    this.name = name;
    this.url = url;
  }
}
 
let site = new Runoob("菜鸟教程",  "https://www.runoob.com");
```

创建对象时会自动调用构造函数的方法 **constructor()**.

**类表达式**

类表达式是定义类的另一种方法.类表达式可以命名或不命名.命名类表达式的名称是该类体的局部名称.

```
// 未命名/匿名类
let Runoob = class {
  constructor(name, url) {
    this.name = name;
    this.url = url;
  }
};
console.log(Runoob.name);
// output: "Runoob"
 
// 命名类
let Runoob = class Runoob2 {
  constructor(name, url) {
    this.name = name;
    this.url = url;
  }
};
console.log(Runoob.name);
// 输出: "Runoob2"
```

构造方法

构造方法是一种特殊的方法:

- 构造方法名为 constructor()

- 构造方法在创建新对象时会自动执行.

- 构造方法用于初始化对象属性.

- 如果不定义构造方法, JavaScript 会自动添加一个空的构造方法.

### 类的方法














































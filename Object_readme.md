# Object

https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/Object

# 构造函数

## Object()

```js
Object(); // 创建一个新的 Object 对象。该对象将会包裹（wrapper）传入的参数

new Object(42);
// Number {42}
//     [[Prototype]]: Number
//     [[PrimitiveValue]]: 42

new Object("42");
// String {'42'}
//     0: "4"
//     1: "2"
//     length: 2
//     [[Prototype]]: String
//     [[PrimitiveValue]]: "42"
```

# 属性

## Object.prototype.constructor

// Object.prototype.**proto**

# 方法

// Object.prototype.**defineGetter**()
// Object.prototype.**defineSetter**()
// Object.prototype.**lookupGetter**()
// Object.prototype.**lookupSetter**()

## Object.assign()

## Object.create()

```js
Object.create(proto，[propertiesObject])

const person = {
    isHuman: false,
    printIntroduction: function () {
        console.log(`My name is ${this.name}. Am I human? ${this.isHuman}`);
    },
};

const me = Object.create(person, {
    name: {
        value: "Matthew",
    },
    isHuman: {
        value: true,
    },
});

me.printIntroduction();
// "My name is Matthew. Am I human? true"

```
## // Object.hasOwn()
## // Object.prototype.toSource()

## Object.defineProperties()

## Object.defineProperty()


## Object.freeze()


## Object.getOwnPropertyDescriptor()
## Object.getOwnPropertyDescriptors()

## Object.getOwnPropertyNames()
## Object.getOwnPropertySymbols()

## Object.getPrototypeOf()
## Object.is()
## Object.isExtensible()
## Object.isFrozen()
## Object.isSealed()
## Object.preventExtensions()
## Object.seal()
## Object.setPrototypeOf()

## Object.keys()
## Object.values()
## Object.entries()
## Object.fromEntries()


## Object.prototype.hasOwnProperty()
## Object.prototype.isPrototypeOf()
## Object.prototype.propertyIsEnumerable()
## Object.prototype.toLocaleString()
## Object.prototype.toString()
## Object.prototype.valueOf()


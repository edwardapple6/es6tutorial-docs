# Set

```js
// 去重规则
NaN 等于自身
两个对象总是不相等的

// 键名和键值是同一个值

new Set().add(1);         // Set(1) {1}
new Set([1, 2, 3, 4, 4])  // Set(4) {1, 2, 3, 4}

// 扩展运算符将一个数组转为用逗号分隔的 参数序列
...[1, 2, 3, 4]                // Uncaught SyntaxError: Unexpected token '...'
[...[1, 2, 3, 4]]              // [1, 2, 3, 4]
... new Set([1, 2, 3, 4, 4])   // Uncaught SyntaxError: Unexpected token 'new'
[...new Set([1, 2, 3, 4, 4])]  // [1, 2, 3, 4]

...{1, 2, 3, 4}      // Uncaught SyntaxError: Unexpected number
[...{1, 2, 3, 4}]    // Uncaught SyntaxError: Unexpected number
[...Set{1, 2, 3, 4}] // Uncaught SyntaxError: Unexpected token '{'
[...Set]             // Uncaught TypeError: Set is not iterable

// 属性
Set.prototype.constructor;
Set.prototype.size;

// 操作方法
Set.prototype.add(value);    // set
Set.prototype.delete(value); // boolean
Set.prototype.has(value);    // boolean
Set.prototype.clear();       // undefined

// 遍历方法
Set.prototype.keys()    // SetIterator 返回键名的遍历器
Set.prototype.values()  // SetIterator 返回键值的遍历器
Set.prototype.entries() // SetIterator 返回键值对的遍历器
Set.prototype.forEach() // undefined   使用回调函数遍历每个成员

// Set 结构的实例 默认可遍历，它的 默认遍历器生成函数 就是它的 values 方法
Set.prototype[Symbol.iterator] === Set.prottype.values // true

// 示例
new Set([1, 2, 3, 4, 4]).__proto__[Symbol.iterator] // ƒ values() { [native code] }
Set.prototype[Symbol.iterator]                      // ƒ values() { [native code] }

// 示例
new Set([1, 2, 3, 4, 4])
// Set(4) {1, 2, 3, 4}
// [[Entries]]
// 0: 1
// 1: 2
// 2: 3
// 3: 4
// size: 4
// [[Prototype]]: Set
// add: ƒ add()
// clear: ƒ clear()
// constructor: ƒ Set()
// delete: ƒ delete()
// entries: ƒ entries()
// forEach: ƒ forEach()
// has: ƒ has()
// keys: ƒ values()
// size: (...)
// values: ƒ values()
// Symbol(Symbol.iterator): ƒ values()
// Symbol(Symbol.toStringTag): "Set"
// get size: ƒ size()
// [[Prototype]]: Object
```

# WeakSet

WeakSet 的成员只能是对象，而不能是其他类型的值。
WeakSet 没有 size 属性，没有办法遍历它的成员。
成员都是弱引用，随时可能消失。

```js
WeakSet.prototype.add(value); // 向 WeakSet 实例添加一个新成员。
WeakSet.prototype.delete(value); // 清除 WeakSet 实例的指定成员。
WeakSet.prototype.has(value); // 返回一个布尔值，表示某个值是否在 WeakSet 实例之中。
```

# Map

```js
// 属性
Map.prototype.constructor;
Map.prototype.size; // number

// 操作方法
Map.prototype.set(key, value) // 返回整个 Map 结构，可以采用链式写法。
Map.prototype.get(key)        // 键值 | undefined
Map.prototype.has(key)        // boolean
Map.prototype.delete(key)     // boolean
Map.prototype.clear()         // undefined

// 遍历方法
Map.prototype.keys()    // 返回键名的遍历器。
Map.prototype.values()  // 返回键值的遍历器。
Map.prototype.entries() // 返回所有成员的遍历器。
Map.prototype.forEach((value, key, map) => {}) // 遍历 Map 的所有成员。

// Map 结构的默认遍历器接口（`Symbol.iterator`属性），就是`entries`方法
map[Symbol.iterator] === map.entries
```

# WeakMap

`WeakMap`只接受对象作为键名（`null`除外），不接受其他类型的值作为键名。
`WeakMap`的键名所指向的对象，不计入垃圾回收机制。
WeakMap 弱引用的只是键名，而不是键值。键值依然是正常引用。

```js
WeakMap.prototype.get()
WeakMap.prototype.set()
WeakMap.prototype.has()
WeakMap.prototype.delete()
```
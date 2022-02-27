XII
https://github.com/ruanyf/es6tutorial
http://www.broadview.com.cn/32475 // 博文视点

# 电子书
https://es6.ruanyifeng.com/
注：注释部分书中没有 20210915

#README               前言
#docs/
    intro           ECMAScript 6简介
    let             let 和 const 命令
    destructuring   变量的解构赋值 // 2021-12-22 L108
    string          字符串的扩展
    <!-- string-methods  字符串的新增方法 -->
    regex           正则的扩展
    number          数值的扩展
    function        函数的扩展
    array           数组的扩展
    object          对象的扩展
    <!-- object-methods  对象的新增方法 -->
    <!-- operator        运算符的扩展 -->
    symbol          Symbol
    set-map         Set 和 Map 数据结构
    proxy           Proxy
    reflect         Reflect
    promise         Promise 对象
    iterator        Iterator 和 for...of 循环
    generator       Generator 函数的语法 // 2021-12-22 L123  2021-12-23 L317
    generator-async Generator 函数的异步应用
    async           async 函数
    class           Class 的基本语法
    class-extends   Class 的继承
    module          Module 的语法
    module-loader   Module 的加载实现
    style           编程风格
    spec            读懂规格
    <!-- async-iterator  异步遍历器 -->
    arraybuffer     ArrayBuffer
    <!-- proposals       最新提案 -->
    <!-- decorator       Decorator -->
    <!-- reference       参考链接 -->

#docs  acknowledgment  无
#docs  fp              无
#docs  mixin           无
#docs  simd            无

    https://github.com/ruanyf/es6tutorial/                 // 源码
    https://github.com/ruanyf/es6tutorial/commits/gh-pages // 修订历史
    https://github.com/ruanyf/es6tutorial/issues           // 反馈意见


node --v8-options | findstr harmony
  --es-staging (enable test-worthy harmony features (for internal use only))
  --harmony (enable all completed harmony features)
  --harmony-shipping (enable all shipped harmony features)
  --harmony-regexp-sequence (enable "RegExp Unicode sequence properties" (in progress))
  --harmony-weak-refs-with-cleanup-some (enable "harmony weak references with FinalizationRegistry.prototype.cleanupSome" (in progress))
  --harmony-regexp-match-indices (enable "harmony regexp match indices" (in progress))
  --harmony-intl-displaynames-date-types (enable "Intl.DisplayNames date types" (in progress))
  --harmony-string-replaceall (enable "harmony String.prototype.replaceAll")
  --harmony-logical-assignment (enable "harmony logical assignment")
  --harmony-promise-any (enable "harmony Promise.any")
  --harmony-top-level-await (enable "harmony top level await")
  --harmony-intl-dateformat-day-period (enable "Add dayPeriod option to DateTimeFormat")
  --harmony-intl-segmenter (enable "Intl.Segmenter")
  --harmony-namespace-exports (enable "harmony namespace exports (export * as foo from 'bar')")
  --harmony-sharedarraybuffer (enable "harmony sharedarraybuffer")
  --harmony-import-meta (enable "harmony import.meta property")
  --harmony-dynamic-import (enable "harmony dynamic import")
  --harmony-promise-all-settled (enable "harmony Promise.allSettled")
  --harmony-private-methods (enable "harmony private methods in class literals")
  --harmony-weak-refs (enable "harmony weak references")
  --harmony-intl-dateformat-fractional-second-digits (enable "Add fractionalSecondDigits option to DateTimeFormat")



# 目录

第1章 ECMAScript 6简介 1
    1 ECMAScript和JavaScript的关系 1
    2 ES6与ECMAScript 2015的关系 1
    3 语法提案的批准流程 2
    4 ECMAScript的历史 3
    5 部署进度 4
    6 Babel 转码器 4
        1 配置文件.babelrc 5
        2 命令行转码babel-cli 6
        3 babel-node 7
        4 babel-register 8
        5 babel-core 8
        6 babel-polyfill 9
        7 浏览器环境 10
        8 在线转换 10
        9 与其他工具的配合 11
    7 Traceur转码器 11
        1 直接插入网页 12
        2 在线转换 13
        3 命令行转换 14
        4 Node环境的用法 15
第2章 let和const命令 17
    1 let 命令 17
        1 基本用法 17
        2 不存在变量提升 19
        3 暂时性死区 19
        4 不允许重复声明 21
    2 块级作用域 22
        1 为什么需要块级作用域 22
        2 ES6的块级作用域 23
        3 块级作用域与函数声明 24
        4 do表达式 27
    3 const命令 28
        1 基本用法 28
        2 本质 29
        3 ES6声明变量的6种方法 30
    4 顶层对象的属性 30
    5 global对象 31
第3章 变量的解构赋值 33
    1 数组的解构赋值 33
        1 基本用法 33
        2 默认值 35
    2 对象的解构赋值 37
    3 字符串的解构赋值 41
    4 数值和布尔值的解构赋值 41
    5 函数参数的解构赋值 42
    6 圆括号问题 43
        1 不能使用圆括号的情况 43
        2 可以使用圆括号的情况 44
    7 用途 44
第4章 字符串的扩展 49
    1  字符的Unicode表示法 49
    2  codePointAt() 50
    3  String.fromCodePoint() 52
    4  字符串的遍历器接口 52
    5  at() 53
    6  normalize() 53
    7  includes()、startsWith()、endsWith() 54
    8  repeat() 55
    9  padStart()、padEnd() 56
    10 模板字符串 57
    11 实例：模板编译 60
    12 标签模板 62
    13 String.raw() 67
    14 模板字符串的限制 68
第5章 正则的扩展 71
    1  RegExp构造函数 71
    2  字符串的正则方法 72
    3  u修饰符 72
    4  y修饰符 74
    5  sticky属性 77
    6  flags属性 77
    7  s修饰符：dotAll模式 78
    8  后行断言 79
    9  Unicode属性类 80
    10 具名组匹配 81
        1 简介 81
        2 解构赋值和替换 82
        3 引用 83
第6章 数值的扩展 85
    1  二进制和八进制表示法 85
    2  Number.isFinite()、Number.isNaN() 86
    3  Number.parseInt()、Number.parseFloat() 87
    4  Number.isInteger() 88
    5  Number.EPSILON 88
    6  安全整数和Number.isSafeInteger() 89
    7  Math对象的扩展 92
        1 Math.trunc() 92
        2 Math.sign() 92
        3 Math.cbrt() 93
        4 Math.clz32() 94
        5 Math.imul() 95
        6 Math.fround() 95
        7 Math.hypot() 96
        8 对数方法 96
        9 双曲函数方法 98
    8  Math.signbit() 98
    9  指数运算符 99
    10 Integer数据类型 99
        1 简介 99
        2 运算 100
第7章 函数的扩展 103
    1 函数参数的默认值 103
        1 基本用法 103
        2 与解构赋值默认值结合使用 105
        3 参数默认值的位置 107
        4 函数的length属性 108
        5 作用域 108
        6 应用 111
    2 rest参数 112
    3 严格模式 113
    4 name属性 115
    5 箭头函数 116
        1 基本用法 116
        2 注意事项 118
        3 嵌套的箭头函数 121
    6 绑定this 123
    7 尾调用优化 124
        1 什么是尾调用 124
        2 尾调用优化 125
        3 尾递归 126
        4 递归函数的改写 128
        5 严格模式 129
        6 尾递归优化的实现 129
    8 函数参数的尾逗号 132
第8章 数组的扩展 133
    1 扩展运算符 133
        1 含义 133
        2 替代数组的apply方法 134
        3 扩展运算符的应用 136
    2 Array.from() 139
    3 Array.of() 142
    4 数组实例的copyWithin() 143
    5 数组实例的find()和findIndex() 144
    6 数组实例的fill() 145
    7 数组实例的entries()、keys()和values() 145
    8 数组实例的includes() 146
    9 数组的空位 147
第9章 对象的扩展 151
    1 属性的简洁表示法 151
    2 属性名表达式 154
    3 方法的name属性 156
    4 Object.is() 157
    5 Object.assign() 158
        1 基本用法 158
        2 注意点 160
        3 常见用途 161
    6 属性的可枚举性 163
    7 属性的遍历 165
    8 __proto__ 属性、Object.setPrototypeOf()、Object.getPrototypeOf() 166
        1 __proto__ 属性 166
        2 Object.setPrototypeOf() 167
        3 Object.getPrototypeOf() 168
    9 Object.keys()、Object.values()、Object.entries() 169
        1 Object.keys() 169
        2 Object.values() 170
        3 Object.entries 171
    10 对象的扩展运算符 173
    11 Object.getOwnPropertyDescriptors() 177
    12 Null传导运算符 181
第10章 Symbol 183
    1 概述 183
    2 作为属性名的Symbol 185
    3 实例：消除魔术字符串 188
    4 属性名的遍历 189
    5 Symbol.for()、Symbol.keyFor() 191
    6 实例：模块的Singleton模式 192
    7 内置的Symbol值 194
        1  Symbol.hasInstance        194
        2  Symbol.isConcatSpreadable 195
        3  Symbol.species            196
        4  Symbol.match              197
        5  Symbol.replace            197
        6  Symbol.search             198
        7  Symbol.split              198
        8  Symbol.iterator           199
        9  Symbol.toPrimitive        200
        10 Symbol.toStringTag        201
        11 Symbol.unscopables        202
第11章 Set和Map数据结构 205
    1 Set 205
        1 基本用法 205
        2 Set实例的属性和方法 207
        3 遍历操作 208
    2 WeakSet 212
        1 含义 212
        2 语法 212
    3 Map 214
        1 含义和基本用法 214
        2 实例的属性和操作方法 218
        3 遍历方法 220
        4 与其他数据结构的互相转换 222
    4 WeakMap 225
        1 含义 225
        2 WeakMap的语法 227
        3 WeakMap示例 228
        4 WeakMap的用途 229
第12章 Proxy 233
    1 概述 233
    2 Proxy实例的方法 237
        1  get()                      237
        2  set()                      241
        3  apply()                    243
        4  has()                      244
        5  construct()                246
        6  deleteProperty()           247
        7  defineProperty()           248
        8  getOwnPropertyDescriptor() 248
        9  getPrototypeOf()           249
        10 isExtensible()             249
        11 ownKeys()                  250
        12 preventExtensions()        254
        13 setPrototypeOf()           255
    3 Proxy.revocable() 255
    4 this问题 256
    5 实例：Web服务的客户端 258
第13章 Reflect 259
    1 概述 259
    2 静态方法 261
        1  Reflect.get(target, name, receiver) 262
        2  Reflect.set(target, name, value, receiver) 263
        3  Reflect.has(obj, name) 264
        4  Reflect.deleteProperty(obj, name) 265
        5  Reflect.construct(target, args) 265
        6  Reflect.getPrototypeOf(obj) 265
        7  Reflect.setPrototypeOf(obj, newProto) 266
        8  Reflect.apply(func, thisArg, args) 267
        9  Reflect.defineProperty(target, propertyKey, attributes) 267
        10 Reflect.getOwnPropertyDescriptor (target, propertyKey) 268
        11 Reflect.isExtensible (target) 268
        12 Reflect.preventExtensions(target) 269
        13 Reflect.ownKeys (target) 269
    3 实例：使用Proxy实现观察者模式 270
第14章 Promise对象 273
    1 Promise的含义 273
    2 基本用法 274
    3 Promise.prototype.then() 278
    4 Promise.prototype.catch() 279
    5 Promise.all() 285
    6 Promise.race() 287
    7 Promise.resolve() 288
    8 Promise.reject() 290
    9 两个有用的附加方法 291
        1 done() 291
        2 finally() 292
    10 应用 292
        1 加载图片 292
        2 Generator函数与Promise的结合 293
    11 Promise.try() 294
第15章 Iterator和for...of循环 297
    1 Iterator（遍历器）的概念 297
    2 默认Iterator接口 300
    3 调用Iterator接口的场合 305
    4 字符串的Iterator接口 307
    5 Iterator接口与Generator函数 308
    6 遍历器对象的return()、throw() 309
    7 for...of循环 310
        1 数组 310
        2 Set和Map结构 311
        3 计算生成的数据结构 312
        4 类似数组的对象 313
        5 对象 314
        6 与其他遍历语法的比较 315
第16章 Generator函数的语法 317
    1 简介 317
        1 基本概念 317
        2 yield表达式 319
        3 与Iterator接口的关系 322
    2 next方法的参数 323
    3 for...of循环 325
    4 Generator.prototype.throw() 328
    5 Generator.prototype.return() 334
    6 yield*表达式 335
    7 作为对象属性的Generator函数 342
    8 Generator函数this 342
    9 含义 345
        1 Generator与状态机 345
        2 Generator与协程 346
    10 应用 347
        1 异步操作的同步化表达 347
        2 控制流管理 348
        3 部署Iterator接口 351
        4 作为数据结构 352
第17章 Generator函数的异步应用 355
    1 传统方法 355
    2 基本概念 355
        1 异步 355
        2 回调函数 356
        3 Promise 356
    3 Generator函数 357
        1 协程 357
        2 协程的Generator函数实现 358
        3 Generator函数的数据交换和错误处理 359
        4 异步任务的封装 360
    4 Thunk函数 361
        1 参数的求值策略 361
        2 Thunk函数的含义 362
        3 JavaScript语言的Thunk函数 362
        4 Thunkify模块 364
        5 Generator函数的流程管理 365
        6 Thunk函数的自动流程管理 367
    5 co模块 368
        1 基本用法 368
        2 co模块的原理 369
        3 基于Promise对象的自动执行 369
        4 co模块的源码 371
        5 处理并发的异步操作 372
    6 实例：处理 Stream 373
第18章 async函数 375
    1 含义 375
    2 用法 377
    3 语法 379
        1 返回Promise对象 379
        2 Promise对象的状态变化 379
        3 await命令 380
        4 错误处理 382
        5 使用注意点 383
    4 async函数的实现原理 386
    5 其他异步处理方法的比较 387
    6 实例：按顺序完成异步操作 388
    7 异步遍历器 390
        1 异步遍历的接口 390
        2 for await...of 392
        3 异步Generator函数 393
        4 yield*语句 398
第19章 Class的基本语法 399
    1 简介 399
    2 严格模式 403
    3 constructor方法 403
    4 类的实例对象 404
    5 Class表达式 406
    6 不存在变量提升 407
    7 私有方法 408
    8 私有属性 409
    9 this的指向 410
    10 name属性 412
    11 Class的取值函数（getter）和存值函数（setter） 412
    12 Class的Generator方法 413
    13 Class的静态方法 414
    14 Class的静态属性和实例属性 415
        1 Class的实例属性 416
        2 Class的静态属性 417
    15 new.target属性 418
第20章 Class的继承 421
    1 简介 421
    2 Object.getPrototypeOf() 423
    3 super关键字 423
    4 类的prototype属性和 __proto__ 属性 429
        1 extends的继承目标 430
        2 实例的 __proto__ 属性 432
    5 原生构造函数的继承 432
    6 Mixin模式的实现 436
第21章 修饰器 439
    1 类的修饰 439
    2 方法的修饰 442
    3 为什么修饰器不能用于函数 444
    4 core-decorators.js 446
    5 使用修饰器实现自动发布事件 449
    6 Mixin 450
    7 Trait 453
    8 Babel转码器的支持 456
第22章 Module的语法 457
    1 概述 457
    2 严格模式 458
    3 export命令 459
    4 import命令 462
    5 模块的整体加载 464
    6 export default命令 465
    7 export与import的复合写法 468
    8 模块的继承 469
    9 跨模块常量 470
    10 import() 471
        1 简介 471
        2 适用场合 472
        3 注意点 473
第23章 Module的加载实现 475
    1 浏览器加载 475
        1 传统方法 475
        2 加载规则 476
    2 ES6模块与CommonJS模块的差异 477
    3 Node加载 481
        1 概述 481
        2 import命令加载CommonJS模块 482
        3 require命令加载ES6模块 484
    4 循环加载 485
        1 CommonJS模块的加载原理 485
        2 CommonJS模块的循环加载 486
        3 ES6模块的循环加载 488
    5 ES6模块的转码 492
        1 ES6 module transpiler 492
        2 SystemJS 492
第24章 编程风格 495
    1 块级作用域 495
        1 let取代var 495
        2 全局常量和线程安全 496
    2 字符串 497
    3 解构赋值 497
    4 对象 498
    5 数组 500
    6 函数 501
    7 Map结构 503
    8 Class 503
    9 模块 504
    10 ESLint的使用 506
第25章 读懂ECMAScript规格 509
    1 概述 509
    2 相等运算符 510
    3 数组的空位 511
    4 数组的map方法 513
第26章 ArrayBuffer 517
    1 ArrayBuffer对象 518
        1 概述 518
        2 ArrayBuffer.prototype.byteLength 520
        3 ArrayBuffer.prototype.slice() 520
        4 ArrayBuffer.isView() 520
    2 TypedArray视图 521
        1  概述 521
        2  构造函数 522
        3  数组方法 524
        4  字节序 526
        5  BYTES_PER_ELEMENT属性 528
        6  ArrayBuffer与字符串的互相转换 528
        7  溢出 529
        8  TypedArray.prototype.buffer 531
        9  TypedArray.prototype.byteLength、
           TypedArray.prototype.byteOffset 531
        10 TypedArray.prototype.length 531
        11 TypedArray.prototype.set() 532
        12 TypedArray.prototype.subarray() 532
        13 TypedArray.prototype.slice() 532
        14 TypedArray.of() 533
        15 TypedArray.from() 533
    3 复合视图 534
    4 DataView视图 535
    5 二进制数组的应用 537
        1 AJAX 537
        2 Canvas 538
        3 WebSocket 539
        4 Fetch API 539
        5 File API 539
    6 SharedArrayBuffer 541
    7 Atomics对象 543
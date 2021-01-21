---
title: JS-Q&A
date: 2021-01-19T10:14:09+08:00
tags: [JavaScript]
# CC BY-NC 4.0
license: CC BY-NC 4.0
---

记录一些 js 相关的问题。

<!-- more -->

Q: 以下两段代码的区别

片段一

```js
const EMPTY_ARR = Object.freeze([]);

const a = EMPTY_ARR;
const b = EMPTY_ARR;
```

片段二

```js
const a = Object.freeze([]);
const b = Object.freeze([]);
```

A: 片段一消耗的内存更少

---

Q: 以下两段代码的区别

片段一

```js
function test(params) {
  const { type, data } = params;
  console.log(type, data);
}

test({
  type: 1,
  data: 2,
});
```

片段二

```js
function test(type, data) {
  console.log(type, data);
}
test(1, 2);
```

A: 第一种易于代码参数扩展，第二种方式益于压缩代码。

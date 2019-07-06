
> 一些常用的代码片段


将数字四舍五入到指定的小数位数
```javascript
const round = (n, decimals = 0) => Number(`${Math.round(`${n}e${decimals}`)}e-${decimals}`);
round(1.005, 2);    // 1.01
```


返回两个或两个以上数字/数字数组中元素之和。
```javascript
const sum = (...arr) => [].concat(...arr).reduce((acc, val) => acc + val, 0);
sum([1, 2, 3, 4]);  // 10
```

延迟异步函数的执行，返回一个pormise。
```javascript
const sleep = ms => new Promise(resolve => setTimeout(resolve, ms));
async function sleepyWork() {
    console.log("---------");
    await sleep(1000);
    console.log('我是1s后才开始输出的');
}
sleepyWork();
```

计算一个数组中某个值出现的次数
用```Array.prototype.reduce()```方法计算数组内的值进行递增
```javascript
const countOccurrences = (arr, val) => arr.reduce((a, v) => (v === val ? a + 1 : a), 0);
countOccurrences([1, 1, 2, 1, 2, 3], 1); // 3
```
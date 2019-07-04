
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

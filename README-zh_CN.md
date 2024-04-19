<a href="https://github.com/chutao-zhang/alibs-utils/tree/master#readme" target="_blank">Englist</a> | 中文

<p>
<img alt="npm" src="https://img.shields.io/npm/v/@alibs/utils?logo=npm&color=%234ac41c">
<img alt="npm" src="https://img.shields.io/npm/dm/@alibs/utils?logo=npm&color=%234ac41c">
<img alt="GitHub forks" src="https://img.shields.io/github/forks/chutao-zhang/alibs-utils">
<img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/chutao-zhang/alibs-utils">
</p>

### 安装

```js
npm install @alibs/utils
```

### 使用

```js
import { xxx } from "@alibs/utils";
```

### API

##### 1. debounce

`debounce(func: Function, delay: number): Function`

eg.

```js
const debounceFunc = debounce(() => {
  console.log("防抖测试");
}, 1 * 1000); // delay 毫秒(ms)
```

##### 2. throttle

`throttle(func: Function, delay: number): Function`

eg.

```js
const throttleFunc = throttle(() => {
  console.log("节流测试");
}, 1 * 1000); // delay 毫秒(ms)
```

##### 3. bytesFormat

`bytesFormat(bytes: number, decimals?: number): string`

eg.

```js
// decimals 小数点位数(默认:2)
console.log(bytesFormat(1024, 2)); // => 1 KB
console.log(bytesFormat(1024 * 1024, 2)); // => 1 MB
```

> 注意: 如果 `bytes` 和 `decimals` 是负数或着是非数字, 将会返回`0 KB`。

##### 4. stringFormat

`stringFormat(fmt: string, ...args: StringFormatArgs[]): string`

eg.

```js
console.log(stringFormat("今天是{0}年{1}月{2}号", 2023, 5, 1)); // => 今天是2023年5月1号
console.log(stringFormat("今天是{0}年{1}月{2}号", [2023, 5, 1])); // => 今天是2023年5月1号
console.log(
  stringFormat("今天是{year}年{month}月{date}号", {
    year: 2023,
    month: 5,
    date: 1,
  })
); // => 今天是2023年5月1号
```

##### 5. isPC

`isPC(): boolean` 检查当前是否在 PC 端

##### 6. isWechat

`isWechat(): boolean` 检查当前是否为微信环境

##### 7. cookieHandler

```js
cookieHandler.get(): object;
cookieHandler.get(name: string): string;
cookieHandler.get(names: string[]): object;
cookieHandler.set(name: string, value: string, options?: ICookieOptions): void;
cookieHandler.set(props: ICookieProps | ICookieProps[]): void;
cookieHandler.remove(name: string, options?: IRemoveCookieOptions): void;
cookieHandler.remove(items: Array<string | IRemoveCookieProps>): void;
cookieHandler.clear(): void;
```

##### 8. localStorageHandler

```js
localStorageHandler.get():object;
localStorageHandler.get(key: string): any;
localStorageHandler.get(keys: string[]): object;
localStorageHandler.set(key: string, value: any): void;
localStorageHandler.set(obj: object): void;
localStorageHandler.remove(key: string): void;
localStorageHandler.remove(keys: string[]): void;
localStorageHandler.clear(): void;
```

##### 9. sessionStorageHandler

```js
// 与localStorageHandler用法相似
```

Englist | <a href="https://github.com/chutaozh/mangolibs-utils/blob/master/README-zh_CN.md" target="_blank">中文</a>

<p>
<img alt="npm" src="https://img.shields.io/npm/v/@mangolibs/utils?logo=npm&color=%234ac41c">
<img alt="npm" src="https://img.shields.io/npm/dm/@mangolibs/utils?logo=npm&color=%234ac41c">
<img alt="GitHub forks" src="https://img.shields.io/github/forks/chutaozh/mangolibs-utils">
<img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/chutaozh/mangolibs-utils">
</p>

### Installation

```js
npm install @mangolibs/utils
```

### Usage

```js
import { xxx } from "@mangolibs/utils";
```

### API

##### 1. debounce

`debounce(func: Function, delay: number): Function`

eg.

```js
const debounceFunc = debounce(() => {
  console.log("debounce test.");
}, 1 * 1000); // delay (ms)
```

##### 2. throttle

`throttle(func: Function, delay: number): Function`

eg.

```js
const throttleFunc = throttle(() => {
  console.log("throttle test.");
}, 1 * 1000); // delay (ms)
```

##### 3. bytesFormat

`bytesFormat(bytes: number, decimals?: number): string`

eg.

```js
// decimals (default:2)
console.log(bytesFormat(1024, 2)); // => 1 KB
console.log(bytesFormat(1024 * 1024, 2)); // => 1 MB
```

> Note: If `bytes` and `decimals` are not numbers or negative, `0 KB` is returned.

##### 4. stringFormat

`stringFormat(fmt: string, ...args: StringFormatArgs[]): string`

eg.

```js
console.log(stringFormat("Today is {0}/{1}/{2}", 1, 5, 2023)); // => Today is 1/5/2023
console.log(stringFormat("Today is {0}/{1}/{2}", [1, 5, 2023])); // => Today is 1/5/2023
console.log(
  stringFormat("Today is {date}/{month}/{year}", {
    year: 2023,
    month: 5,
    date: 1,
  })
); // => Today is 1/5/2023
```

##### 5. isPC

`isPC(): boolean`

##### 6. isWechat

`isWechat(): boolean`

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
// Same as localStorageHandler
```

## 集合的概念

**特点：**
- 无序且元素唯一的数据结构
- 常用操作：去重、判断某元素是否在集合中，求交集

去重：
```javascript
let arr = [1,2,2,1,2,2]
new Set(arr) // Set {1, 2}
let arr2 = [...new Set(arr)] // 1,2
```

判断元素是否在集合中：
```javascript
let set = new Set(arr)
let has = set.has(2) // true
let has = set.has(3) // false
```

求交集：
```javascript
let set2 = new Set([2,3])
let set3 = new Set([...set].filter(item) => set2.has(item)))
```

ES6 set方法：
- new
```javascript
let set = new Set()
```
- add
```javascript
set.add(1)  // 1
set.add(5) // 1、5
set.add(5)  // 1、5
```
- has
```javascript
let has = set.has(1) // true
```
- delete
```javascript
set.delete(5) // true
set // Set {1}
```
- size
```javascript
set.size // 1
```
- 遍历
```javascript
for(let item of set){
    consoel.log(item)
}
```
**set 中的元素，key和value是相同的**

- set 和 array 互转
```javascript
const arr = [...set] // set转换为array
```
```javascript
const arr = Array.from(set)// set转换为array
```
```javascript
const myset = new Set([1,2,3,4,5]) // 数组转换为aray
```
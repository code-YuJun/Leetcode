## 字典的概念
**特点：与集合类似，也是存储唯一值的数据结构，但是是以键值对的形式来存储。**
ES6字典是 Map
- 实例化
```javascript
const m = new Map()
```
- 添加
```javascript
m.set('a','aaa')
m.set('b','bbb')
```
- 获取
```javascript
m.get('a') // 'aaa'
```
- 删除
```javascript
m.delete('a')
// 删除所有的键
m.clear()
```
- 修改
```javascript
m.set('a','aa')
```
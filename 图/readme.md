## 图的表示法

- 邻接矩阵

![img](https://img-blog.csdnimg.cn/e7aa26d78a064d6a92cdef59c0ce2304.png)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

- 邻接表

![img](https://img-blog.csdnimg.cn/2baa1e98592f4d61a2a6e48d68639e85.png)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

## 图的常用操作

**深度优先遍历**

1. 访问根节点
2. 对根节点的 **没访问过的相邻节点** 挨个进行深度优先遍历

![img](https://img-blog.csdnimg.cn/03ac94f7ed914989a136449755e0bfe3.png)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

从 2 开始，访问 0 ，然后找 0  的相邻节点2、1，因为 2 访问过了，所以访问 1。访问3，然后找3的相邻节点，还是3，但是已经访问过了，所以删除 3-> 3

```javascript
// 邻接表表示法
const graph = {
    0: [1, 2],
    1: [2],
    2: [0, 3],
    3: [3]
}
// 深度遍历
const visited = new Set()
const dfs = (n) => {
    console.log(n)
    visited.add(n)
    graph[n].forEach((c) => {
        if(!visited.has(c)){
            dfs(c)
        }
    })
}
console.log(dfs(2)) // 2、0、1、3
```

**广度优先遍历**

1. 新建一个队列，根节点入队
2. 队头出队并访问
3. 把队头的没有访问过的相邻节点入队
4. 重复2、3，直到队列为空

![img](https://img-blog.csdnimg.cn/27e845e6f5904625add319960f89572c.png)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



分析：2 入队，2出队。0、3入队，0出队，1入队。3出队，1出队

```javascript
const visited = new Set()
visited.add(2);
const q = [2]
while(q.length){
    const n = q.shift()
    console.log(n)
    graph[n].forEach((c) => {
        if(!visited.has(c)){
            q.push(c)
            visited.add(c)
        }
    })
}
```
























## 空间复杂度

**算法在运行过程中临时占用存储空间大小的度量。**

O(1)

```javascript
let i = 0
i+1
```

O(n)

```javascript
const list = []
for(let i = 0;i < n;i++){
    list.push(i)
}
```

O(![img](https://img-blog.csdnimg.cn/img_convert/5a442df34c6b4286acbdb3f128289c53.png))

```javascript
let arr = []
for(let i = 0;i <= n;i++){
    arr.push([])
    for(let j = 1;j <= n;j++){
        arr[i][j] = i*j            //    相当于是二维数组
    }
}
```

## 时间复杂度

```javascript
for(let i = 1;i <= n;i++){
    for(let j = 1;j <= n;j++){
        c[i][j] = 0;
        for(let k = 1;k <= n;k++){
            c[i][j] = c[i][j] + a[i][k] * b[k][j]
        }
    }
}
```

![img](https://img-blog.csdnimg.cn/img_convert/0b40563eb71f440caa28695f4e86ce03.png)

```javascript
for(let i = 1;i <= n;i++){
    for(let j = 1;j <= i;j++){
        for(let k = 1;k <= j;k++){
            x = x + 1
        }
    }    
}
```

![img](https://img-blog.csdnimg.cn/img_convert/1438dcf994bc4ea89dd559f7c5433dbf.png)

```javascript
i = 1;
while(i <= n)
    i = i* 2
```

循环1次： i = 1 * 2 = 2

循环2次： i = 2 * 2 = 4

循环3次： i = 4 * 2 = 8

循环X次： i = 2^x

i <= n

2^x <= n

x <= ![img](https://img-blog.csdnimg.cn/img_convert/148dcf0548d64244b2f98715e384bafa.png)

f(n) <= ![img](https://img-blog.csdnimg.cn/img_convert/148dcf0548d64244b2f98715e384bafa.png)

最大值：f(n) = ![img](https://img-blog.csdnimg.cn/img_convert/148dcf0548d64244b2f98715e384bafa.png)

![img](https://img-blog.csdnimg.cn/img_convert/8dfe3798987a4dd49fa36ca9bd29229f.png)
## 栈的概念

栈的特点为 **先进后出，后进先出**（LIFO：last in first out）

![img](https://github.com/code-YuJun/Leetcode/blob/master/图片/42dba16fc8a44da382a5b1121b54c45e.png)

**栈常见的操作：**

- push（element）：添加一个新元素到栈顶位置；

- pop（）：移除栈顶的元素，同时返回被移除的元素；

- stack[stack.length - 1]:获取栈顶元素；

**栈在前端中的使用：**

函数调用栈：A（B（C（D（））））：即A函数中调用B，B调用C，C调用D；在A执行的过程中会将A压入栈，随后B执行时B也被压入栈，函数C和D执行时也会被压入栈。所以当前栈的顺序为：A->B->C->D（栈顶）；函数D执行完之后，会弹出栈被释放，弹出栈的顺序为D->C->B->A;

递归：为什么没有停止条件的递归会造成栈溢出？比如函数A为递归函数，不断地调用自己（因为函数还没有执行完，不会把函数弹出栈），不停地把相同的函数A压入栈，最后造成栈溢出（Stack Overfloat）

## 十进制转二进制











## 有效的括号

题目：https://leetcode.cn/problems/valid-parentheses/
















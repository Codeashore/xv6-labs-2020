# 项目笔记

#### 项目架构

* kernel 内核源码
* user：系统自带工具源码，shell、echo、cat等工具实现
* grade-lab-util：python实现的代码测试工具
* Makefile：make配置文件

### Lab1

    这个 lab 是为了熟悉 xv6 的使用，就是使用一些 xv6 的系统调用来实现几个函数，和使用 Linux 上的系统调用是完全一样的，唯一的区别就是**要用 exit(0) 来结束进程** 。另外注意要将相应的用户进程 **添加到顶层 Makefile 中的 UPROGS 中** 。

###### 1.sleep.c

思路：调用 系统调用sleep即可 [sleep.c](http://link.zhihu.com/?target=https%3A//github.com/zhengjiaw/MIT6.S081/blob/master/lab1_util/sleep.c)

##### 2.pingpong.c 用 pipe 在两个 进程间实现通信

思路：  **将管道当成一个先进先出的队列即可** 。管道的简单使用，实现交互即可 ：[pingpong.c](http://link.zhihu.com/?target=https%3A//github.com/zhengjiaw/MIT6.S081/blob/master/lab1_util/pingpong.c)

###### primes.c 用多进程的方式求解素数

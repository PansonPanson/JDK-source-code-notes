** 

+ [ ]  hash 算法和寻址算法优化
+ [ ]  hash 碰撞问题：当数量到达一定限度，无论怎么优化hash 算法，都会造成 hash 冲突，此时链表 && 红黑树 ：遍历一颗红黑树找一个元素，此时O(logn)
+ [ ]  扩容 rehash 优化，做到扩容之后，将数据分布均匀，减少冲突




参考：
+ https://mp.weixin.qq.com/s/UFeLHR4qtGYPODTiNJDmHQ
+ https://tech.meituan.com/2016/06/24/java-hashmap.html
+ 深入浅出ConcurrentHashMap1.8：https://www.jianshu.com/p/c0642afe03e0
+ 老生常谈，HashMap的死循环：https://www.jianshu.com/p/1e9cf0ac07f4
+ 深入分析ConcurrentHashMap1.8的扩容实现：https://www.jianshu.com/p/f6730d5784ad
+ ConcurrentHashMap的红黑树实现分析：https://www.jianshu.com/p/23b84ba9a498
+ 谈谈ConcurrentHashMap1.7和1.8的不同实现：https://www.jianshu.com/p/e694f1e868ec
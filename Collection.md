# Record
编程记录

# Collection体系 笔记

## Collection 是顶层接口 下面有List与Set两个重要实现  而List与Set又有不同的实现


### List
List 底层是数组 可重复有序集合

List实现无效扩容的原理是拿自身长度 加上长度 >> 1  创建以原长度的1.5倍的新集合 同时拷贝旧集合所有元素到新集合 由于List每个元素有序 并且有索引  所以查询效率低于Set

### Set
Set 是无序不可重复集合

Set集合通过hashcode对元素进行分组 提供比List更高的查询效率 

使用Set存放 ? extends Object 时 ，两个对象的equals方法必须返回true 必须重写hashcode方法  才能保证唯一性  

HashSet不保证元素插入顺序  LinkedHashSet可保证元素插入顺序

TreeSet是有序集合 传入一个非重复Set可自动转换为有序集合

### Map
Map 键值对集合 类似JavaScript中的非实例对象结构

Key不可重复 Value可重复  HashMap的Key不可重复性是由内部的Map实现的

HashMap扩容与List大同小异
 
因为线程安全问题 HashMap的底层在Java7以后 由链表换成了红黑树

TreeMap 是一个有序集合 使用方法与特性与TreeSet大同小异

使用二叉树作为底层的集合 查询效率快

二叉树原则 左小右大 使得查询次数比有序集合次数少

二叉树插入元素能保持原结构不变 新插入的元素继续向二叉树原则分叉



## 一、继承关系

+ ArrayList实现了List, RandomAccess, Cloneable, java.io.Serializable等接口。

+ ArrayList实现了List，提供了基础的添加、删除、遍历等操作。

+ ArrayList实现了RandomAccess，提供了随机访问的能力。

+ ArrayList实现了Cloneable，可以被克隆。

+ ArrayList实现了Serializable，可以被序列化。

## 二、属性

```java
    /**
     * Default initial capacity.
     * 默认容量为10，也就是通过new ArrayList()创建时的默认容量。
     */
    private static final int DEFAULT_CAPACITY = 10;

    /**
     * Shared empty array instance used for empty instances.
     * 空的数组，这种是通过new ArrayList(0)创建时用的是这个空数组。
     */
    private static final Object[] EMPTY_ELEMENTDATA = {};

    /**
     * Shared empty array instance used for default sized empty instances. We
     * distinguish this from EMPTY_ELEMENTDATA to know how much to inflate when
     * first element is added.
     * 也是空数组，这种是通过new ArrayList() 创建时用的是这个空数组，与 
     * EMPTY_ELEMENTDATA的区别是在添加第一个元素时使用这个空数组的会初始化
     * 为DEFAULT_CAPACITY（10）个元素。
     */
    private static final Object[] DEFAULTCAPACITY_EMPTY_ELEMENTDATA = {};

    /**
     * The array buffer into which the elements of the ArrayList are stored.
     * The capacity of the ArrayList is the length of this array buffer. Any
     * empty ArrayList with elementData == DEFAULTCAPACITY_EMPTY_ELEMENTDATA
     * will be expanded to DEFAULT_CAPACITY when the first element is added.
     * 真正存放元素的地方，使用transient是为了不序列化这个字段。
     */
    transient Object[] elementData; // non-private to simplify nested class access

    /**
     * The size of the ArrayList (the number of elements it contains).
     * 真正存储元素的个数，而不是elementData数组的长度。
     *
     * @serial
     */
    private int size;
    
    /**
     * The maximum size of array to allocate.
     * Some VMs reserve some header words in an array.
     * Attempts to allocate larger arrays may result in
     * OutOfMemoryError: Requested array size exceeds VM limit
     * 
     */
    private static final int MAX_ARRAY_SIZE = Integer.MAX_VALUE - 8;

```

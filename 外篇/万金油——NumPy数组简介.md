##  “万金油”NumPy的简单介绍

​		先说说为什么我把NumPy叫做"万金油"吧：因为在Python数据分析的世界，Numpy是一个实实在在的通用程序库，它不仅支持常用的数值数组，同时提供了用于高效处理这些数组的函数，而且很多其他的数据分析库(如Pandas)底层都有Numpy的支持，所以，称Numpy为"万金油"比较形象吧。

### NumPy数组对象

​       NumPy提供了一个名为ndarray的多维数组对象。NumPy数组是同质的，也就是说，Numpy数组只能存放同一种类型的对象。数组由两部分组成，分别是：存储在连续的内存块中的实际数据；描述实际数据的元数据。

   + arange()创建一维数组

     ```python
     import numpy as np
     def numpysum(n):
         a = np.arange(n) ** 2
         b = np.arange(n) ** 3
         c = a + b
         return c
     ```

     如上所示，我们经常使用numpy的arange()来建立一维数组，上述代码是将生成的0~n-1的一维数组的每个元素分别进行2次方和3次方，得到两个新数组a和b，然后对a、b两个数组对应位置上的每个元素进行相加，得到c数组，若调用上述函数numpy(sum)，最终得到的结果是：array([ 0,  2, 12], dtype=int32),这个结果的类型是numpy.ndarray.

+ 创建多维数组

  ```python
  import numpy as np
  m = np.array([
      np.arange(2),
      np.arange(2)
  ])
  m   
  m.shape
  ```

  上述m的结果是：

  ```python
  array([[0, 1],
         [0, 1]])
  ```

  m的shape属性值是：(2,2)，表示m是一个2x2的数组。

  这里有一个问题，那就是：如何选择NumPy数组中指定的元素呢？请看：

  ```python
  import numpy as np
  a = np.array([[1,2],[3,4]])
  a[0,0]  # 1
  a[0,1]  # 2
  a[1,0]  # 3
  a[1,1]  # 4
  ```

  怎么样？选择数组元素很简单吧？只要通过a[m,n]的形式，就能访问数组内的元素，其中m和n为数组元素的下标。

  




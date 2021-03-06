## 冒泡排序
### 比较步骤
1. 比较相邻的元素。如果第一个比第二个大，就交换他们两个。
2. 对每一对相邻元素作同样的工作，从头到尾，最后的元素应该会是最大的数。
3. 针对所有的元素重复以上的步骤，除了最后一个。
4. 持续每次对越来越少的元素重复上面的步骤，直到没有任何一对数字需要比较。 
### 编程思路
外循环控制需要比较的元素，比如第一次排序后，最后一个元素就不需要比较了，内循环则负责两两元素比较，将元素放到正确位置上。
### 实现
```js
function bubbleSort(arr) {
    for (let i = arr.length - 1; i > 0; i--) {
        for (let j = 0; j < i; j++) {
            // 当 prev > current ，交换位置
            if (arr[j] > arr[j + 1]) [arr[j], arr[j + 1]] = [arr[j + 1], arr[j]];
        }
    }
    return arr;
}


console.log(bubbleSort([1, 2, 3111, 0, 32, 21]));
```

#### 推荐阅读
- [十大经典排序算法（动图演示）](https://www.cnblogs.com/onepixel/p/7674659.html)
- [排序算法](https://zxpsuper.github.io/Demo/advanced_front_end/suanfa/sort.html#_1-%E5%86%92%E6%B3%A1%E6%8E%92%E5%BA%8F)

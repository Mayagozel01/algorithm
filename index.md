# Задачи LeetCode для алгоритмов из книги "Грокаем алгоритмы"

## 1. Бинарный поиск (Binary Search)

**Концепция из книги:** Поиск в отсортированном массиве за O(log n)

**Задачи LeetCode:**
- **704. Binary Search** (Easy) - классическая реализация
## bellik
# hokman sorted massiw bolmaly
```
var search = function(nums, target) {
        let left = 0;
    let right = nums.length - 1;

    while (left <= right) {
        const mid = Math.floor((left + right) / 2);

        if (nums[mid] === target) {
            return mid;
        }

        if (nums[mid] < target) {
            left = mid + 1;
        } else {
            right = mid - 1;
        }
    }

    return -1;
};
 ```
- **35. Search Insert Position** (Easy) - поиск позиции для вставки
```
# Intuition
<!-- Describe your first thoughts on how to solve this problem. -->

# Approach
<!-- Describe your approach to solving the problem. -->

# Complexity
- Time complexity:
<!-- Add your time complexity here, e.g. $$O(n)$$ -->

- Space complexity:
<!-- Add your space complexity here, e.g. $$O(n)$$ -->

# Code
```javascript []
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number}
 */
var searchInsert = function(nums, target) {
        let left = 0;
    let right = nums.length - 1;

    while (left <= right) {
        const mid = Math.floor((left + right) / 2);

        if (nums[mid] === target) {
            return mid;
        }

        if (nums[mid] < target) {
            left = mid + 1;
        } else {
            right = mid - 1;
        }
    }

    return right+1;
};
```
```
- **278. First Bad Version** (Easy) - применение бинарного поиска
- **33. Search in Rotated Sorted Array** (Medium) - усложненная версия
- **34. Find First and Last Position of Element** (Medium) - границы элемента
- **69. Sqrt(x)** (Easy) - вычисление квадратного корня
- **374. Guess Number Higher or Lower** (Easy) - игра с бинарным поиском

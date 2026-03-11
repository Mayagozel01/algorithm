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

## BinarySearch with recursion
### Intuition
<!-- Describe your first thoughts on how to solve this problem. -->

### Approach
<!-- Describe your approach to solving the problem. -->

### Complexity
- Time complexity:
<!-- Add your time complexity here, e.g. $$O(n)$$ -->

- Space complexity:
<!-- Add your space complexity here, e.g. $$O(n)$$ -->

### Code
```javascript []
/**
 * Definition for isBadVersion()
 * 
 * @param {integer} version number
 * @return {boolean} whether the version is bad
 * isBadVersion = function(version) {
 *     ...
 * };
 */

/**
 * @param {function} isBadVersion()
 * @return {function}
 */
var solution = function(isBadVersion) {
    /**
     * @param {integer} n Total versions
     * @return {integer} The first bad version
     */
    return function(n) {
            let left = 1;
            let right = n;
    while (left < right) {
        const mid = Math.floor((left + right) / 2);


        if (isBadVersion(mid)) {
            right = mid;
        } else {
            left = mid + 1;
        }
    }

    return right;
    };
};
```
- **33. Search in Rotated Sorted Array** (Medium) - усложненная версия
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
var search = function(nums, target) {
  let left = 0;
    let right = nums.length - 1;

    while (left <= right) {
        let mid = Math.floor((left + right) / 2);

        if (nums[mid] === target) {
            return mid;
        }

        // левая часть отсортирована
        if (nums[left] <= nums[mid]) {
            if (nums[left] <= target && target < nums[mid]) {
                right = mid - 1;
            } else {
                left = mid + 1;
            }
        } 
        // правая часть отсортирована
        else {
            if (nums[mid] < target && target <= nums[right]) {
                left = mid + 1;
            } else {
                right = mid - 1;
            }
        }
    }

    return -1;  
};
```
- **34. Find First and Last Position of Element** (Medium) - границы элемента
- **69. Sqrt(x)** (Easy) - вычисление квадратного корня
- **374. Guess Number Higher or Lower** (Easy) - игра с бинарным поиском

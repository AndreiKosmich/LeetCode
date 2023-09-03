# [88. Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/)

---

> Given two sorted integer arrays `nums1` and `nums2`, merge `nums2` into `nums1` as one sorted array.
>
> The number of elements initialized in `nums1` and `nums2` are `m` and `n` respectively.
> You may assume that `nums1` has enough space (size that is equal to `m + n`) to hold additional elements from `nums2`.
>
>
>
> ### Example 1:
> ```
> Input: nums1 = [1,2,3,0,0,0], m = 3, nums2 = [2,5,6], n = 3
> Output: [1,2,2,3,5,6]
> ```
>
> ### Example 2:
> ```
> Input: nums1 = [1], m = 1, nums2 = [], n = 0
> Output: [1]
> ```
>
> ### Constraints:
> * `0 <= n, m <= 200`
> * `1 <= n + m <= 200`
> * `nums1.length == m + n`
> * `nums2.length == n`
> * `-10^9 <= nums1[i], nums2[i] <= 10^9`

---


### Solution
* **mine**  `Your runtime beats 88.82% of ruby submissions.`
```
// O(n)time O(n)space

def merge(nums1, m, nums2, n)
   nums1.pop(n)
   nums1.concat(nums2).sort!
end
```
# [46. Permutations](https://leetcode.com/problems/permutations/)

---

> Given an array nums of distinct integers, return all the possible permutations. You can return the answer in any order.
>
> ### Example 1:
> ```
> Input: nums = [1,2,3]
> Output: [[1,2,3],[1,3,2],[2,1,3],[2,3,1],[3,1,2],[3,2,1]]
> ```
>
> ### Example 2:
> ```
> Input: nums = [0,1]
> Output: [[0,1],[1,0]]
> ```
>
> ### Example 3:
> ```
> Input: nums = [1]
> Output: [[1]]
> ```


---

### Solution
* **mine**  `Your runtime beats 92.9 % of ruby submissions.`
```
// O(n)time O(n)space

def permute(nums, temp = [], res = [])
  if nums.empty?
    res << temp
  else
    nums.each { |num| permute(nums - [num], temp + [num], res)}
  end

  res
end
```
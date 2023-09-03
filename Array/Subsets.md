# [78. Subsets](https://leetcode.com/problems/subsets/description/)


---

> Given a set of `distinct` integers, nums, return all possible subsets (the power set).
>
> ### Note:
> * The solution set must not contain duplicate subsets.
>
> ### Example 1:
> ```
> Input: nums = [1,2,3]
> Output: [[],[1],[2],[1,2],[3],[1,3],[2,3],[1,2,3]]
> ```
>
> ### Example 2:
> ```
> Input: nums = [0]
> Output: [[],[0]]
> ```

---

### Solution
* **mine**  `Your runtime beats 100% of ruby submissions.`
```
// O(n)time O(n)space

def subsets(nums)
  (0..nums.size).flat_map { |k| nums.combination(k).to_a }
end
```
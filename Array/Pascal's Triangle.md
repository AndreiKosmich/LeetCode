# [118. Pascal's Triangle](https://leetcode.com/problems/pascals-triangle/)

---

> Given a non-negative integer numRows, generate the first numRows of Pascal's triangle.
>
> ![1](https://upload.wikimedia.org/wikipedia/commons/0/0d/PascalTriangleAnimated2.gif)
>
> In Pascal's triangle, each number is the sum of the two numbers directly above it.
>
> ### Example:
> ```
>Input: 5
>Output:
>[
>     [1],
>    [1,1],
>   [1,2,1],
>  [1,3,3,1],
> [1,4,6,4,1]
>]
> ```

---


### Solution
* **mine**  `Your runtime beats 88.82% of ruby submissions.`
```
// O(n2)time O(n)space

def generate(num_rows)
  result = [[1]]

  (1..num_rows - 1).each do
    temp = [0] + result.last + [0]
    row = []

    (0..temp.length - 2).each do |i|
      row << temp[i] + temp[i + 1]
    end

    result << row
  end

  result

end
```
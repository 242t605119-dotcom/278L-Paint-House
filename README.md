# Paint House

LeetCode 256

## Problem Statement

There are `n` houses in a row, and each house can be painted with one of three colors: red, blue, or green.

The cost of painting each house with each color is given in a 2D array `costs`.

No two adjacent houses can have the same color.

Return the minimum cost to paint all the houses.

## Solution

This solution uses Dynamic Programming.

For each house, we calculate the minimum cost of painting it with each color. When choosing a color for the current house, the previous house must have a different color.

The cost values are updated directly in the `costs` array, and the minimum value for the last house gives the final answer.

## Example

### Input

```text
costs = [[17,2,17],
         [16,16,5],
         [14,3,19]]
```

### Output

```text
10
```

### Explanation

One minimum-cost coloring is:

```text
House 1 → Blue = 2
House 2 → Green = 5
House 3 → Blue = 3
```

Total cost:

```text
2 + 5 + 3 = 10
```

Therefore, the minimum cost is `10`.

## Approach

1. Consider each house one by one.
2. For each color of the current house, choose the minimum cost from the two different colors of the previous house.
3. Add that minimum previous cost to the current painting cost.
4. Continue until all houses are processed.
5. Return the minimum cost among the three colors for the last house.

## Algorithm

1. If there are no houses, return `0`.
2. Start from the second house.
3. Calculate the minimum cost for painting it red, blue, and green.
4. Repeat the same process for every remaining house.
5. Take the minimum of the three costs for the last house.
6. Return that value.

## Complexity

* Time Complexity: O(n)
* Space Complexity: O(1)

## Author

T. Nandhini


#gfg #array

## Problem
Given an array `arr[]` of non-negative integers, return the second largest **distinct** element. If it doesn't exist, return `-1`.

Example: `[12, 35, 1, 10, 34, 1]` → `34`
Example: `[10, 10]` → `-1`

## Approach

Initialize `max = firstElem` and `secondMax = -1`. Traverse the array from index 1:
* If `curr > max, update  `max` and `secondMax`
* Else curr > secondMax and `curr < max` update secondMax

!!! IMP - add curr < max to avoid dup.

## Code
```java
class Solution {
    public int getSecondLargest(int[] arr) {
        if (arr.length < 2) return -1;

        int max = arr[0];
        int secondMax = -1;

        for (int i = 1; i < arr.length; i++) {
            if (arr[i] > max) {
                secondMax = max;
                max = arr[i];
            } else if (arr[i] < max && arr[i] > secondMax) {
                secondMax = arr[i];
            }
        }

        return secondMax;
    }
}
```

## Complexity
| Type  | Complexity | Why |
|-------|------------|-----|
| Time  | O(n)       | Single pass over the array |
| Space | O(1)       | Only two variables (`max`, `secondMax`) |

## Points to Remember
- Use `arr[i] < max` in the `else if`, not just `arr[i] > secondMax`. Otherwise a duplicate of max gets picked as second largest (`[5, 5, 3]` returns 5 instead of 3).
- `-1` as the initial `secondMax` works only because values are non-negative.
- When max changes, the old max must move to `secondMax` first, before overwriting `max`.
# DAY_10-
BULB SWITCHER



---

### Bulb Switcher

```markdown
# Bulb Switcher (LeetCode 319)

## Problem Statement
There are `n` bulbs that are initially off. For each round `i` (1 ≤ i ≤ n), you toggle every `i`-th bulb. You need to determine how many bulbs are on after `n` rounds.

## Example
**Input:** n = 3  
**Output:** 1  
**Explanation:** Only bulb 1 is on after 3 rounds.

## Insight
- A bulb ends up **on** only if it is toggled an odd number of times.
- This happens only for bulbs at positions that are **perfect squares** (e.g., 1, 4, 9, 16...).

## Solution
Return the count of perfect squares ≤ n, which is simply `⌊√n⌋`.

## Time and Space Complexity
- **Time Complexity:** O(1)
- **Space Complexity:** O(1)

## Java Code
```java
class Solution {
    public int bulbSwitch(int n) {
        return (int)Math.sqrt(n);
    }
}


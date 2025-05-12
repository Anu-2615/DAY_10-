# DAY_10-
DELETE THE MIDDLE OF LINKED LIST 


# Delete the Middle Node of a Linked List (LeetCode 2095)

## Problem Statement
You are given the head of a linked list. Delete the middle node, and return the head of the modified linked list.

- The middle node of a linked list of size `n` is the `⌊n / 2⌋`-th node using **0-based indexing**.
- If the list has only one node, delete it and return `null`.

## Example
**Input:** head = [1,3,4,7,1,2,6]  
**Output:** [1,3,4,1,2,6]

## Approach
We use the two-pointer technique:
- `fast` pointer moves two steps at a time.
- `slow` pointer moves one step at a time.
- When `fast` reaches the end, `slow` will be just before the middle node.
- We remove the middle node by skipping it: `slow.next = slow.next.next`.

## Time and Space Complexity
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)

## Java Code
```java
class Solution {
    public ListNode deleteMiddle(ListNode head) {
        if (head == null || head.next == null)
            return null;

        ListNode slow = head;
        ListNode fast = head.next;

        while (fast.next != null && fast.next.next != null) {
            fast = fast.next.next;
            slow = slow.next;
        }

        slow.next = slow.next.next;
        return head;
    }
}


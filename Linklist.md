链表环判断使用双指针.链表有环则末节点.next不会为空,且快指针在遍历的时候会和慢指针再次相遇

```java
public class Solution {
    public boolean hasCycle(ListNode head) {
		  if (head == null) {
		        return false;
		    }
		  ListNode slow = head;
		  ListNode fast = head.next;
		  while(slow != null&&fast != null&&fast.next != null) {
			  if (slow == fast) {
				  return true;
			}
			  else {
				slow = slow.next;
				fast = fast.next.next;
			}
	    }
		return false;
    }	
}
```
![image](https://github.com/1autodidact/Leetcode-Algorithm/blob/master/linklist.JPG)

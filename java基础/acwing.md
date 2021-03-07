1、反转链表

```
public ListNode reverseList(ListNode head){
		if(head == null || head.next == null){
				return head;
		}
		ListNode p1,p2;
		p1 = new ListNode();
		while(head != null){
				p2 = head.next;
				head.next = p1.next;
				p1.next = head;
				head = p2;
		}
}
```


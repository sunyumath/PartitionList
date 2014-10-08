PartitionList
=============
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;å
 *     ListNode next;
 *     ListNode(int x) {
 *         val = x;
 *         next = null;
 *     }
 * }
 */
public class Solution {
    public ListNode partition(ListNode head, int x) {
        ListNode c=head.next;
        ListNode p=head;
        while(c!=null){
            if(c.val<val){
                if(head.val>=x){
                    c.next=head;
                    head=c;
                }
                else{
                    c.next=head.next;
                    head.next=c;
                    ListNode temp=head;
                    while(c.next!=null&&c.next.val>=x){
                        tmep.next=c.next;
                        temp=c.next;
                        c.next=temp.next;
                        temp.next=c;
                    }
                }
                p.next=c.next;
                c=p.next;
            }
            else{
                 p=c;
                 c=c.next;
            }
        }
        return head;
    }
}

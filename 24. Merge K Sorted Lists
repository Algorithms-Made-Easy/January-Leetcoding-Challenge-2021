//TC: O(nlogn)
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode() {}
 *     ListNode(int val) { this.val = val; }
 *     ListNode(int val, ListNode next) { this.val = val; this.next = next; }
 * }
 */
class Solution {
    public ListNode mergeKLists(ListNode[] lists) {
        if(lists==null || lists.length==0) return null;
        
        ListNode head=new ListNode(0);
        ListNode temp=head;
        List<Integer> l=new ArrayList<>();
        for(ListNode list:lists){
            while(list!=null){
                l.add(list.val);
                list=list.next;
            }
        }
        Collections.sort(l);
        for(int val:l){
            temp.next=new ListNode(val);
            temp=temp.next;
        }
        return head.next;
    }
}

//TC: O(nk)
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode() {}
 *     ListNode(int val) { this.val = val; }
 *     ListNode(int val, ListNode next) { this.val = val; this.next = next; }
 * }
 */
class Solution {
    public ListNode mergeKLists(ListNode[] lists) {
        if(lists==null || lists.length==0) return null;
        
        ListNode head=new ListNode(0);
        ListNode temp=head;
        
        while(true){
            int p=0;
            for(int i=0;i<lists.length;i++){
                if(lists[p]==null || (lists[i]!=null && lists[p].val>lists[i].val)){
                    p=i;
                }
            }
            
            if(lists[p]==null){
                break;
            }
            temp.next=new ListNode(lists[p].val);
            temp=temp.next;
            lists[p]=lists[p].next;
        }
        
        return head.next;
    }
}

//TC: O(nlogk)
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode() {}
 *     ListNode(int val) { this.val = val; }
 *     ListNode(int val, ListNode next) { this.val = val; this.next = next; }
 * }
 */
class Solution {
    public ListNode mergeKLists(ListNode[] lists) {
        if(lists==null || lists.length==0) return null;
        
        int interval=1;
        while(interval<lists.length){
            for(int i=0;i+interval<lists.length;i=i+interval*2){
                lists[i]=mergeTwoLists(lists[i],lists[i+interval]);
            }
            interval*=2;
        }
        return lists[0];
    }
    
    ListNode mergeTwoLists(ListNode l1, ListNode l2) {
        if(l1==null) return l2;
        if(l2==null) return l1;
        
        ListNode newHead=new ListNode(l1.val);
        ListNode temp=newHead;
        while(l2!=null && l1!=null){
            if(l1.val<=l2.val){
                temp.next=new ListNode(l1.val);
                l1=l1.next;
            }else{
                temp.next=new ListNode(l2.val);
                l2=l2.next;
            }
            temp=temp.next;
        }
        
        if(l1!=null){
            temp.next=l1;
        } 
        else{
            temp.next=l2;
        }
        return newHead.next;
    }
}

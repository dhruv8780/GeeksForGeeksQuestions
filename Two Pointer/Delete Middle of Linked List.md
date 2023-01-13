# link: https://practice.geeksforgeeks.org/problems/delete-middle-of-linked-list/1?page=1&category[]=two-pointer-algorithm&sortBy=difficulty

Solution: class Solution {
    Node deleteMid(Node head) {
        // This is method only submission.
        // You only need to complete the method.
        Node slow = head;
        Node fast = head;
        Node prev = null;
        
        while(fast != null && fast.next != null){
            fast = fast.next.next;
            prev = slow;
            slow = slow.next;
        }
        
        prev.next = slow.next;
        return head;
    }
}
# link:https://practice.geeksforgeeks.org/problems/detect-loop-in-linked-list/1?page=1&category[]=two-pointer-algorithm&sortBy=difficulty


class Solution {
    //Function to check if the linked list has a loop.
    public static boolean detectLoop(Node head){
        // Add code here
        Node slow = head;
        Node fast = head;
        //Node temp = null;
        if(head == null) return false;
        
        while(fast != null && fast.next != null){
            fast = fast.next.next;
            slow = slow.next;
            
            if(fast == slow){
                return true;
            }
        }
        return false;
    }
}
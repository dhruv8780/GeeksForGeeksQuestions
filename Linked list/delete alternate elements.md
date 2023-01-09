## link: https://practice.geeksforgeeks.org/problems/delete-alternate-nodes/1?page=1&category[]=Linked%20List&sortBy=difficulty

Solution:
class Solution {
    
    public void deleteAlternate (Node head){
        //Write your code here
        Node n = head;
        
        while(n != null && n.next != null){
            n.next = n.next.next;
            n = n.next;
        }
        
    }
}
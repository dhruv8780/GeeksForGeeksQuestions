# link:https://practice.geeksforgeeks.org/problems/reverse-a-linked-list/1?page=1&difficulty[]=0&category[]=Linked%20List&sortBy=submissions

class Solution
{
    //Function to reverse a linked list.
    Node reverseList(Node head)
    {
        // code here
        Node tail = new Node(head.data);
        Node top = tail;
       // Node top = top;
       head = head.next;
        
        while(head != null){
            top = new Node(head.data);
            top.next = tail;
            tail = top;
            head = head.next;
        }
        
        return top;
        
    }
    
    
}
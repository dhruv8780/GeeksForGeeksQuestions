## link: https://practice.geeksforgeeks.org/problems/linked-list-insertion-1587115620/1?page=1&category[]=Linked%20List&sortBy=difficulty

Solution:
class Solution
{
    //Function to insert a node at the beginning of the linked list.
    Node insertAtBeginning(Node head, int x)
    {
        // code here
        Node top = new Node(x);
        top.next = head;
        head = top;
        
        
        return top;
        
    }
    
    //Function to insert a node at the end of the linked list.
    Node insertAtEnd(Node head, int x)
    {
        // code here
        Node bottom = new Node(x);
        
        if(head == null){
            head=bottom;
        }
        
        Node n1 = head;
        
        while(n1.next != null){
            n1 = n1.next;
        }
        
        n1.next = bottom;
        bottom.next = null;
        
        return head;
    }
}
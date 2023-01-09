## link: https://practice.geeksforgeeks.org/problems/print-linked-list-elements/1?page=1&category[]=Linked%20List&sortBy=difficulty

Solution: 
class Solution
{
    // Print elements of a linked list on console
    // head pointer input could be NULL as well
    // for empty list
    void display(Node head)
    {
        //add code here.
        Node next = head;
        //System.out.println(head.data);
        
        while(next != null ){
            System.out.print(next.data + " ");
            next = next.next;
        }
        
    }
}

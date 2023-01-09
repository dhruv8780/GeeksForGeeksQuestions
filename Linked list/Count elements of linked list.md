# link: https://practice.geeksforgeeks.org/problems/count-nodes-of-linked-list/1?page=1&category[]=Linked%20List&sortBy=submissions


Solution:
class Solution
{
    //Function to count nodes of a linked list.
    public static int getCount(Node head)
    {
        
        Node next = head;
        int count = 0;
        
        while(next != null){
            count++;
            next = next.next;
            
        }
        //Code here
        return count;
    }
}
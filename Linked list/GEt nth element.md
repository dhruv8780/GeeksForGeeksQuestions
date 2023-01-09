## link: https://practice.geeksforgeeks.org/problems/node-at-a-given-index-in-linked-list/1?page=1&category[]=Linked%20List&sortBy=difficulty

Solution:
class GfG
{
   
    public static int getNth(Node node, int ind)
    {
       //Your code here
       int index = 0;
       int count = 1;
       Node next = node;
       
       while(next != null){
           if(count == ind){
               return next.data;
           }
           count++;
           next = next.next;
           
       }
       
       return 0;
       
    }
}
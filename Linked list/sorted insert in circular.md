# link: https://practice.geeksforgeeks.org/problems/sorted-insert-for-circular-linked-list/1?page=2&status[]=unsolved&category[]=Linked%20List&sortBy=difficulty

# Solution: 
class Solution
{
	public static Node sortedInsert(Node head,int data)
         {
            //add code here
            Node temp = head;
            Node inserted = new Node(data);
            
            if(head == null){
                head = inserted;
                head.next = inserted;
                return head;
            }
            
            else if(head.data>=data){
                
                
                while(temp.next != head){
                    temp = temp.next;
                }
        
                temp.next = inserted;
                inserted.next = head;
                head = inserted;
                
                return head;
            }
            
            else{
                while(temp.next != head && temp.next.data < data){
                    temp = temp.next;
                }
                inserted.next = temp.next;
                temp.next = inserted;
            }
      
            return head;
         }

}
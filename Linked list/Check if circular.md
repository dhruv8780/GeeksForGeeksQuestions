# Link: https://practice.geeksforgeeks.org/problems/circular-linked-list/1?page=1&status[]=unsolved&category[]=Linked%20List&sortBy=difficulty

Solution: class GfG
{
    boolean isCircular(Node head)
    {
	// Your code here
	    Node count = head;
	    
	    while(count != null){
	        if(count.next == head){
	            break;
	        }
	        if(count.next == null){
	            return false;
	        }
	        count = count.next;
	        
	    }
	    return true;
	
    }
}
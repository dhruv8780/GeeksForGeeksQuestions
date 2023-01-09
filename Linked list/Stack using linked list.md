## link: https://practice.geeksforgeeks.org/problems/implement-stack-using-linked-list/1?page=1&category[]=Linked%20List&sortBy=difficulty

Solution:
class MyStack 
{
    // class StackNode {
    //     int data;
    //     StackNode next;
    //     StackNode(int a) {
    //         data = a;
    //         next = null;
    //     }
    // }   
    StackNode top;
    
    //Function to push an integer into the stack.
    void push(int a) 
    {
        // Add your code here
        StackNode n = new StackNode(a);
        
        n.data = a;
        n.next = top;
        top = n;
        
    }
    
    //Function to remove an item from top of the stack.
    int pop() 
    {
        // Add your code here
        if(top == null){
            return -1;
        }
        StackNode nn = top;
        
        top = top.next;
        
        return nn.data;
        
    }
}

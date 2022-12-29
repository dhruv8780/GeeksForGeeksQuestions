## Link: https://practice.geeksforgeeks.org/problems/implement-stack-using-array/1?page=1&difficulty[]=-1&category[]=Arrays&sortBy=difficulty

Solution: 


class MyStack
{
    int top;
	int arr[] = new int[1000];

    MyStack()
	{
		top = -1;
	}
	
	//Function to push an integer into the stack.
    void push(int a)
	{
	    // Your code here
	    if(top == -1){
	        arr[0] = a;
	        top = 0;
	    } else{
	        //int temp = arr[top];
	        arr[top+1] = a;
	        top+=1;
	    }
	    
	    
	} 
	
    //Function to remove an item from top of the stack.
	int pop()
	{
        // Your code here
        
        if(top == -1){
            return -1;
        } else{
            int temp = arr[top];
            arr[top] = -1;
            top -= 1;
            return temp;
        }
        
 
	}
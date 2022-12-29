## link: https://practice.geeksforgeeks.org/problems/implement-queue-using-array/1?page=1&difficulty[]=-1&category[]=Arrays&sortBy=difficulty

Solution: 
class MyQueue {

    int front, rear;
	int arr[] = new int[100005];

    MyQueue()
	{
		front=0;
		rear=0;
	}
	
	//Function to push an element x in a queue.
	void push(int x)
	{
	    // Your code here
	    if(rear == 0){
	        arr[0] = x;
	        rear+=1;
	    } else{
	        arr[rear] = x;
	        rear+=1;
	    }
	} 

    //Function to pop an element from queue and return that element.
	int pop()
	{
		// Your code here
		if(rear == front){
		    return -1;
		}
		else{
		    return arr[front++];
		}
	} 
}
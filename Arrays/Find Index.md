## Link: https://practice.geeksforgeeks.org/problems/find-index4752/1?page=1&category[]=Arrays&sortBy=difficulty

Solution: 
class Solution
{ 
    // Function to find starting and end index 
    static int[] findIndex(int a[], int N, int key) 
    { 
        //code here.
        int arr[] = {59645564,59645564};
         for(int i = 0, j = N-1; i < N && j >=0; i++, j--){
            if(a[j] == key){
                arr[0] = j;
                //System.out.println(key + " "+ a[j]);
            }
            if(a[i] == key){
                arr[1] = i;
                //System.out.println(key + " "+ a[i]" "+ i);
            }
        }
        
        if(arr[0] == 59645564 && arr[1] == 59645564){
            arr[0] = -1;
            arr[1] = -1;
        }
        return arr;
    }
}
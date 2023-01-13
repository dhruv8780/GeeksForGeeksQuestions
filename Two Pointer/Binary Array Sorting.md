# link: https://practice.geeksforgeeks.org/problems/binary-array-sorting-1587115620/1?page=1&category[]=two-pointer-algorithm&sortBy=difficulty

Solution:
class Solution
{
    //Function to sort the binary array.
    static void binSort(int A[], int N)
    {
        // add your code here
        int i = 0;
        int j = N-1;
        
        while(i<j){
            if(A[i] == 0 && A[j] == 0){
                i++;
            }
            
            if(A[i] == 1 && A[j] == 0){
                A[i] = 0;
                A[j] = 1;
                i++;
                j--;
            }
            
            if(A[j] == 1 && A[i] == 1){
                j--;
            }
            
            if(A[j] == 1 && A[i] == 0){
                j--;
                i++;
            }
        }
        
        
        
        /**************
        * No need to print the array
        * ************/
    }
}
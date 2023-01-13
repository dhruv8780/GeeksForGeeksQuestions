# Link:https://practice.geeksforgeeks.org/problems/four-elements2452/1?page=1&category[]=two-pointer-algorithm&sortBy=difficulty

Solution: class Compute
{
    boolean find4Numbers(int A[], int n, int X) 
    {
        Arrays.sort(A);
        for(int i = 0; i < n-3; i++){
            for(int j = i+1; j < n-2; j++){
                int k = j+1;
                int l = n-1;
                
                while(k<l){
                    if(A[i] + A[j] + A[k] + A[l] == X){
                        return true;
                    } else if(A[i] + A[j] + A[k] + A[l] > X){
                        l--;
                    } else{
                       k++; 
                    }
                }
            }
        }
        
        return false;
        
        
    }
}
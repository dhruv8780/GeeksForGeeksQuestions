# link: https://practice.geeksforgeeks.org/problems/count-the-triplets4615/1?page=1&category[]=two-pointer-algorithm&sortBy=difficulty

Solution: class Solution {
    int countTriplet(int arr[], int n) {
        // code here
        Arrays.sort(arr);

        
        
        int count = 0;
        for(int k = n-1; k >= 0; k--){
        int i = 0;
        int j = k-1;
            while(i<j){
            if(arr[i] + arr[j] == arr[k]){
                count++;
                i++;
                j--;
            }
            else if(arr[i] + arr[j] < arr[k]){
                i++;
            }else{
                j--;
            }
        }
        
        
        }

        
        return count;
    
}
    
}
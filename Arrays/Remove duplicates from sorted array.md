## link : https://practice.geeksforgeeks.org/problems/remove-duplicate-elements-from-sorted-array/1?page=1&difficulty[]=0&status[]=unsolved&category[]=Arrays&sortBy=difficulty

Solution: class Solution {
    int remove_duplicate(int A[],int N){
        // code here
       // ArrayList<Integer> list = new ArrayList<Integer>();
        int j = 1;
        //list.add(A[0]);
        for(int i=1; i < N; i++){
            if(A[i] > A[i-1]){
                //list.add(A[i]);
                A[j] = A[i];
                j++;
            }
            //System.out.println(list);
        }
        return j;
    }
}
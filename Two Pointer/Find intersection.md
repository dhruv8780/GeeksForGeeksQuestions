# link:https://practice.geeksforgeeks.org/problems/intersection-of-two-arrays2404/1?page=1&category[]=two-pointer-algorithm&sortBy=difficulty

class Solution {
    // Function to return the count of the number of elements in
    // the intersection of two arrays.
    public static int NumberofElementsInIntersection(int a[], int b[], int n, int m) {
        // Your code here
        Arrays.sort(a);
        Arrays.sort(b);
        
        int i = 0;
        int j = 0;
        Set<Integer> set = new HashSet<Integer>();
        
        while(i < n && j < m){
            if(a[i] > b[j]){
                j++;
            }
            else if(a[i] < b[j]){
                i++;
            }else if(a[i] == b[j]){
                
                set.add(a[i]);
                i++;
                j++;
            }
        }
        //System.out.println(set);
        return set.size();
        

    }
};
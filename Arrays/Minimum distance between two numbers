## link: https://practice.geeksforgeeks.org/problems/minimum-distance-between-two-numbers/1?page=1&difficulty[]=-1&category[]=Arrays&sortBy=difficulty

Solution: class Solution {
    int minDist(int a[], int n, int x, int y) {
        // code here
        
        int i =0;
        int fx = -1;
        int fy = -1;
        int D = n+1;
        for(int k=0; k< n; k++){
            if(a[k]==x){
               
                fx = k;
            }
            if(a[k]==y){
               
                fy = k;
            }
           // System.out.println(a[k] + "|"+ k +"|"+ tracker);
             if(fx != -1 && fy != -1){
                D = Math.min(D,Math.abs(fx-fy));
            }
        }
        return D == n+1 ? -1 : D; 
    }
}
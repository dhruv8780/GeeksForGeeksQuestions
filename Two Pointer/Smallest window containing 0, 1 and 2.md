# link: https://practice.geeksforgeeks.org/problems/d6e88f06b273a60ae83992314ac514f71841a27d/1?page=1&category[]=two-pointer-algorithm&sortBy=difficulty

Solution: class Solution {
    public int smallestSubstring(String S) {
        // Code here
        int n = S.length();
        int one = -1;
        int two = -1;
        int zero = -1;
        int res = 2147483647;
        
        for(int i = 0; i < n; i++){
            if(S.charAt(i) == '1'){
                one = i;
            }
            else if(S.charAt(i) == '2'){
                two = i;
            }
            else if(S.charAt(i) == '0'){
                zero = i;
            }
            
            if(zero != -1 && one != -1 && two != -1){
                 res = Math.min(res, Math.max(Math.max(one,two), zero) - Math.min(Math.min(one,two),zero));
            }
            
        }
        if(one == -1 || two == -1 || zero == -1){
            return -1;
        }
        
        return res+1;
    }
};
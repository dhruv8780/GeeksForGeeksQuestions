##link: https://practice.geeksforgeeks.org/problems/kth-boom-number5609/1?page=1&difficulty[]=0&category[]=Strings&category[]=Sorting&sortBy=difficulty

MySolution: class Solution {
    public static String BoomNumber(long K) {
        // code here 
        //System.out.println(checkBoom(K));
        
        
        
        long booms =0;
        int num = 0;
        
        
        
        while(booms != K){
            int count = 0;
            String str = Integer.toString(num);
            
            for(int i = 0; i < str.length(); i++){
                if(checkBoom(str.charAt(i)) == true){
                    count++;
                }
            }
        
            if(count == str.length()){
                booms +=1;
                count = 0;
                //System.out.println(num);
            }
            if(booms == K) return Integer.toString(num);
            
            num++;
        }

    return "";
        
    }
    
    static boolean checkBoom(char n){
         
            if(n == '2' || n == '3'){
                return true;
            }
        
        return false;
    }
}

Solution: 

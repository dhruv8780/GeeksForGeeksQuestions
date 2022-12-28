## https://practice.geeksforgeeks.org/problems/fascinating-number3751/1?page=1&category[]=Arrays&sortBy=difficulty

Solution: 

class Solution {
    boolean fascinating(long n) {
        // code here
        long m2 = 2*n;
        long m3 = 3*n;
        
        String finalStatement = Long.toString(n) + Long.toString(m2) + Long.toString(m3);
       // System.out.println(finalStatement);
        
        char charArr[] = finalStatement.toCharArray();
        Arrays.sort(charArr);
        
        String fin = new String(charArr);
        if(fin.equals("123456789"))
        return true;
        else return false;
    }
}
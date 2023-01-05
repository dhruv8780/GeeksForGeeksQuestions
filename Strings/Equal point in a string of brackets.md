## link: https://practice.geeksforgeeks.org/problems/find-equal-point-in-string-of-brackets2542/1?page=2&difficulty[]=0&category[]=Strings&category[]=Sorting&sortBy=difficulty

Solution:
class Solution {

    public long countSub(String str) {

        // Your code goes here 
        char[] strArr = str.toCharArray();
        long index = 0;

        for (int i = 0 ; i < strArr.length; i++){
            if(strArr[i] == ')')
               index++; 
        }

        return index;

    }

}
## link: https://practice.geeksforgeeks.org/problems/remove-all-duplicates-from-a-given-string4321/1?page=1&difficulty[]=0&category[]=Strings&category[]=Sorting&sortBy=difficulty

Solution:
class Solution {
    String removeDuplicates(String str) {
        // code here
        String res = "";
        
        for(int i = 0; i < str.length(); i++){
            if(res.contains(Character.toString(str.charAt(i))) == false){
                res+=Character.toString(str.charAt(i));
            }
        }
        
        return res;
    }
}
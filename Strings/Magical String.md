## LINK: https://practice.geeksforgeeks.org/problems/magical-string3653/1?page=7&category[]=Strings&category[]=Sorting&sortBy=difficulty

Solution:
class Solution{
    static String magicalString(String S){
        // code here
        HashMap<String, String> letters = new HashMap<String, String>();
        String res = "";
        
        for(int i =0; i < 26; i++){
            letters.put(Character.toString(i+97),Character.toString(122-i));
        }
        
        for(int i = 0; i < S.length(); i++) {
            if(letters.containsKey(String.valueOf(S.charAt(i)))){
                res += letters.get(String.valueOf(S.charAt(i)));
            }
        }
        return res;
    }
}
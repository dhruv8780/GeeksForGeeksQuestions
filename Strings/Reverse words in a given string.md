## link: https://practice.geeksforgeeks.org/problems/reverse-words-in-a-given-string5459/1

Solution:
class Solution 
{
    //Function to reverse words in a given string.
    String reverseWords(String S)
    {
        // code here 
        String res = "";
        String temp = "";
        
        String str = S+".";
        int n = str.length();
        ArrayList<String> words = new ArrayList<String>();
        
        for(int i = 0; i < n; i++){
            //res+=S.charAt(i);
            if(str.charAt(i) != '.'){
                temp+=str.charAt(i);
            }
            if(str.charAt(i) == '.'){
                words.add(temp);
                temp = "";
            }
            
        }
        //System.out.println(words);
        for(int i = words.size()-1; i >= 0; i--){
            res+=words.get(i);
            if(i != 0){
                res+=".";
            }
        }
        return res;
    }
}
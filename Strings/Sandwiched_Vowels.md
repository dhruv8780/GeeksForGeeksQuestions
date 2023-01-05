## link: https://practice.geeksforgeeks.org/problems/sandwiched-vowels5158/1?page=1&difficulty[]=-1&difficulty[]=0&status[]=unsolved&category[]=Strings&sortBy=difficulty

Solution:

class Complete{
    
   
    public static String Sandwiched_Vowel(String str) 
    { 
        // Complete function
        char[] chars = str.toCharArray();
        String vowels = "aeiou";
        String result = "";
        
        for(int i = 2; i < str.length(); i++){
            if(vowels.contains(Character. toString(chars[i-2])) == false && vowels.contains(Character. toString(chars[i-1])) && vowels.contains(Character. toString(chars[i])) == false){
                chars[i-1] = '0';
            }
        }

        String strFinal = String.valueOf(chars);
        String strFinal2 =  strFinal.replace("0", "");

        return strFinal2;
    } 
}
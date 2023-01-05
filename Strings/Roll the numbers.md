## link: https://practice.geeksforgeeks.org/problems/roll-the-characters-of-a-string2127/1?page=2&difficulty[]=0&category[]=Strings&category[]=Sorting&sortBy=difficulty

Solution: 

class Solution
{
    String findRollOut(String s,long roll[], int N)
    {
        char[] chars = s.toCharArray();
        //Arrays.sort(roll);
        
        for(int i = 0; i< roll.length; i++){
            for(int j = 0; j < roll[i];  j++){
                if(chars[j] == 'z'){
                    chars[j] = 'a';
                } else{
                    chars[j]+=1;
                }
                
            }
        }
        String string = new String(chars);
        
        return string;
    }
}
# link: https://practice.geeksforgeeks.org/problems/reverse-a-string-with-spaces-intact5213/1?page=1&category[]=two-pointer-algorithm&sortBy=difficulty

Solution:
class Solution
{
    String reverseWithSpacesIntact(String S)
    {
        // your code here
        char[] arr = S.toCharArray();
        int i = 0;
        int j = S.length() - 1;
        //String res = "";
        
        while(i<j){
            if(arr[i] == ' '){
                i++;
            }
            else if(arr[j] == ' '){
                j--;
            }
            else{
                char temp = '0';
                temp = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
                i++;
                j--;
            }
        }
        String str = new String(arr);
        return str;
        
    }
}
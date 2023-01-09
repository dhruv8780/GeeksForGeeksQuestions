## link:https://practice.geeksforgeeks.org/problems/longest-common-prefix-in-an-array5129/1


Solution:

class Solution{
    String longestCommonPrefix(String arr[], int n){
        // code here
       String prefix = arr[0];

        for (int i = 1; i <= n - 1; i++) {
            prefix = commonPrefixUtil(prefix, arr[i]);
        }
        if(prefix.length() != 0){
            return (prefix);
        }
        return "-1";
        
    }
    static String commonPrefixUtil(String str1, String str2) {
        String result = "";
        int n1 = str1.length(), n2 = str2.length();

        // Compare str1 and str2 
        for (int i = 0, j = 0; i <= n1 - 1 && j <= n2 - 1; i++, j++) {
            if (str1.charAt(i) != str2.charAt(j)) {
                break;
            }
            result += str1.charAt(i);
        }

        return (result);
    }
}
## link: https://leetcode.com/problems/valid-anagram/description/

Solution:
class Solution {
    public boolean isAnagram(String s, String t) {
        char[] s1 = s.toCharArray();
        char[] s2 = t.toCharArray();

        Arrays.sort(s1);
        Arrays.sort(s2);
        //System.out.println(s1 + " " + s2);
        //System.out.println(String.valueOf(s1));

        if(String.valueOf(s1).equals(String.valueOf(s2))){
            return true;
        }
        return false;
        

    }
}
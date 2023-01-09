## link: https://practice.geeksforgeeks.org/problems/roman-number-to-integer3201/1

Solution:
class Solution {
    public int romanToInt(String s) {
        Map<String, Integer> romans = new HashMap<String, Integer>();
        romans.put("I", 1);
        romans.put("V", 5);
        romans.put("X", 10);
        romans.put("L", 50);
        romans.put("C", 100);
        romans.put("D", 500);
        romans.put("M", 1000);
        romans.put("IV", 4);
        romans.put("IX", 9);
        romans.put("XL", 40);
        romans.put("XC", 90);
        romans.put("CD", 400);
        romans.put("CM", 900);
        //int[] romansnum = {I,X,X,L,C,D,M}

        int res = 0;
        //ArrayList<String> words = new ArrayList<String>();

        for(int i = 0; i < s.length(); i++){
            if(i+1 < s.length()){
            if(s.charAt(i) == 'I' && s.charAt(i+1) == 'V'){
                res+=romans.get("IV");
                //words.add(String.valueOf(s.charAt(i))+)
                i++;
            }else if(s.charAt(i) == 'I' && s.charAt(i+1) == 'X'){
                res+=romans.get("IX");
                i++;
            }else if(s.charAt(i) == 'X' && s.charAt(i+1) == 'L'){
                res+=romans.get("XL");
                i++;
            }else if(s.charAt(i) == 'X' && s.charAt(i+1) == 'C'){
                res+=romans.get("XC");
                i++;
            }else if(s.charAt(i) == 'C' && s.charAt(i+1) == 'D'){
                res+=romans.get("CD");
                i++;
            }else if(s.charAt(i) == 'C' && s.charAt(i+1) == 'M'){
                res+=romans.get("CM");
                i++;
            }else{
                res+=romans.get(String.valueOf(s.charAt(i)));
            }
            } else {
                res+=romans.get(String.valueOf(s.charAt(i)));
            }

        }
        //res+=romans.get(String.valueOf(s.charAt(s.length()-1)));


        //System.out.println(romans.get("L"));
        return res;
    }
    
}
## link:https://practice.geeksforgeeks.org/problems/replace-all-0s-with-5/1?page=1&difficulty[]=-1&category[]=Arrays&sortBy=difficulty

Solution: 
class GfG {
    int convertfive(int num) {
        // Your code here
        String str = Integer.toString(num);
        String str2 = "";
        for(int i = 0; i < str.length(); i++){
            if(str.charAt(i) == '0'){
                str2+= "5";
            }
            else{
                str2+=str.charAt(i);
            }
        }
        int num2 = Integer.parseInt(str2);
        return num2;
    }
}
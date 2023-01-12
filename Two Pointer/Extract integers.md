# link:https://practice.geeksforgeeks.org/problems/extract-the-integers4428/1?page=1&category[]=two-pointer-algorithm&sortBy=difficulty

Solution:
//{ Driver Code Starts
//Initial Template for Java
import java.io.*;
import java.util.*; 
class GFG{
    public static void main(String args[]) throws IOException { 
        BufferedReader read = new BufferedReader(new InputStreamReader(System.in));
        int t = Integer.parseInt(read.readLine());
        while(t-- > 0){
            String s = read.readLine();
            Solution ob = new Solution();
            ArrayList<String> ans = ob.extractIntegerWords(s);
            if(ans.size()==0)
                System.out.println("No Integers");
            else{
                for(int i=0;i<ans.size();i++)
                    System.out.print(ans.get(i)+" ");
                System.out.println();
            }
        }
    } 
} 
// } Driver Code Ends


//User function Template for Java
class Solution 
{ 
    ArrayList<String> extractIntegerWords(String s) 
    { 
        // code here
        String num = "1234567890";
        int n = s.length();
        
        ArrayList<String> numbers = new ArrayList<String>();
        String temp = "";
        
        int i = 0;
        int j = i;
        
        while(i < n){
            if(num.contains(String.valueOf(s.charAt(i)))){
                while(num.contains(String.valueOf(s.charAt(j))) != false && j < n-1){
                    temp+=s.charAt(j);
                    j++;
                }
                i = j;
            }
            if(temp != ""){
                
                numbers.add(temp);
            }
                
            temp = "";
            
            i++;
            j = i;
            
            
        }
        
        String lastChar = String.valueOf(s.charAt(n-1)));
        
        if(num.contains(lastChar){
            if(numbers.size() > 0){
                String last = numbers.get(numbers.size() -1);
                if(num.contains(lastChar)){
                    if(num.contains(String.valueOf(s.charAt(n-2)))){
                        last+=lastChar;
                        numbers.set(numbers.size() - 1,last );
                    }
                    else{
                        numbers.add(lastChar);
                    }
                }       
            }
            else{
                numbers.add(lastChar);
            }
        }
        
        return numbers;
    }
} 

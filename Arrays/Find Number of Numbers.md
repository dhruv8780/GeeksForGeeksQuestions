## link:https://practice.geeksforgeeks.org/problems/find-number-of-numbers/1?page=1&difficulty[]=-1&difficulty[]=0&status[]=unsolved&category[]=Arrays&sortBy=difficulty

Solution: 
class GfG
{
          public static int num(int a[], int n, int k)
            {
                 //Your code here
                 String str = "";
                 int count = 0;
                for(int i = 0; i < n; i++){
                    str += Integer.toString(a[i]);
                }
                
                for(int j = 0; j < str.length(); j++){
                    //String c= Integer.toString(k);
                    char c=(char)k; 
                    int ascii = '0' + k;
                    // System.out.println(ascii + " 1 $ ");
                    if(str.charAt(j) == ascii){
                        count++;
                    }
                    
                }
                return count;
            }
}
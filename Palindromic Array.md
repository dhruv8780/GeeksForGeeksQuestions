## Link : https://practice.geeksforgeeks.org/problems/palindromic-array-1587115620/1?page=1&category[]=Arrays&sortBy=difficulty

Solution: 
 /*Complete the Function below*/
class GfG
{
	public static int palinArray(int[] a, int n)
           {
                  //add code here.
                  
                  for(int i =0; i < n; i++){
                      //System.out.println(a[i]);
                      int k = checkLength(a[i]);
                      if(k == 0) return 0;
                  }
                  //System.out.println(chechLength(a[2]));
                  return 1;
           }
           
           static public int checkLength(int n){
               String str = Integer.toString(n);
               int temp = 0;
               for(int i = 0, j = str.length()-1; i < str.length() &&  j >= 0; i++ ,j--){
                  // System.out.println(str.substring(0,i) + "|"+ str.substring(j));
                  if(str.charAt(i) == str.charAt(j)){
                    //  System.out.println(str.substring(0,i) + "|"+ str.substring(j));
                     temp +=1;
                  }
                   
               }
               if (temp == str.length())
                    return 1;
                    
                return 0;
               
           }
}
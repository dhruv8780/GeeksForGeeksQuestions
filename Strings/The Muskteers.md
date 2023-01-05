## link: https://practice.geeksforgeeks.org/problems/the-muskteers3519/1?page=7&category[]=Strings&category[]=Sorting&sortBy=difficulty

Solution:
class Solution{
   static boolean checkTogether(String str){
       int first=str.indexOf('0');
       int last=str.lastIndexOf('0');
       if(first==-1)return false;
       for(int i=first;i<last;i++){
           if(str.charAt(i)=='1'){
               return false;
           }
       }
       return true;
   }
}
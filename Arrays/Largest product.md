## link: https://practice.geeksforgeeks.org/problems/largest-product/1?page=1&difficulty[]=-1&category[]=Arrays&sortBy=difficulty

Solution:
class GfG
{
    long findMaxProduct(int A[], int n, int k)
    {
	// Your code here
	long product = 1;
	long temp = 0;
	    for(int i = 0; i < n; i++){
	        if(i+k <= n){
	            for(int j = i; j < i+k ; j++){
	                product = product*A[j];
	                //System.out.println(product + "|"+ j +"|"+ A[j]);
	            }
	            if(product> temp){
	                temp = product;
	            }
	             product = 1;
	        }
	    }
	    return temp;
	}
	
}class GfG
{
    long findMaxProduct(int A[], int n, int k)
    {
	// Your code here
	long product = 1;
	long temp = 0;
	    for(int i = 0; i < n; i++){
	        if(i+k <= n){
	            for(int j = i; j < i+k ; j++){
	                product = product*A[j];
	                //System.out.println(product + "|"+ j +"|"+ A[j]);
	            }
	            if(product> temp){
	                temp = product;
	            }
	             product = 1;
	        }
	    }
	    return temp;
	}
	
}
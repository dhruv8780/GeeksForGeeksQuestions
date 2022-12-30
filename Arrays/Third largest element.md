## link: https://practice.geeksforgeeks.org/problems/third-largest-element/1?page=1&difficulty[]=-1&difficulty[]=0&status[]=unsolved&category[]=Arrays&sortBy=difficulty

Solution:
class Solution
{
    int thirdLargest(int a[], int n)

    {

        int first = a[0], second = -1, third= -1;

        if (n < 3)
        {
            return -1;
        }
        for(int i=0; i<n; i++)
        {
            if(a[i]>first)
            {
                third  = second;
                second = first;
                first = a[i];
            }

            else if (a[i]!=first && a[i]>second)
            {
                third = second;
                second = a[i];
            }

            else if(a[i]!=first && a[i]!=second && a[i]>third)
            {
                third =a[i];
            }

        }

        return third;
    }
}
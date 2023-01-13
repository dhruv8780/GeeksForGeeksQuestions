# link: https://practice.geeksforgeeks.org/problems/find-pairs-with-given-sum-in-doubly-linked-list/1?page=2&category[]=two-pointer-algorithm&sortBy=difficulty

Solution: class Solution {
    public static ArrayList<ArrayList<Integer>> findPairsWithGivenSum(int target, Node head) {
        // code here
 ArrayList<ArrayList<Integer>> list = new ArrayList<ArrayList<Integer>>();
        Node right = head;
        Node left = head;
        while(right.next != null) right = right.next;
        
        while(left != null && right != null && left.data < right.data){
            if(left.data + right.data == target){
                ArrayList<Integer> l = new ArrayList<>();
                l.add(left.data);
                l.add(right.data);
                list.add(l);
                left = left.next;
                right = right.prev;
            }else if(left.data + right.data < target)
                left = left.next;
            else if(left.data + right.data > target)
                right = right.prev;
        }
       
        return list;
        
    }
    

}
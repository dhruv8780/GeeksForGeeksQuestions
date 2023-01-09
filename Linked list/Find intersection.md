# link: https://practice.geeksforgeeks.org/problems/intersection-of-two-sorted-linked-lists/1?page=1&difficulty[]=0&category[]=Linked%20List&sortBy=difficulty


Solution: class Sol
{
   public static Node findIntersection(Node head1, Node head2)
    {
        // code here.
        Node n1 = head1;
        Node n2 = head2;
        
        Node top = new Node(0);
        Node temp = top;
        
        while(n1 != null && n2 != null){
            if(n1.data < n2.data){
                n1 = n1.next;
            } else if(n1.data > n2.data){
                n2 = n2.next;
            } else{
                //System.out.println(n1.data + " " + n2.data);
                top.next = new Node(n1.data);
                top = top.next;
                n1 = n1.next;
                n2 = n2.next;
                
            }
        }
        
        return temp.next;
    }
}
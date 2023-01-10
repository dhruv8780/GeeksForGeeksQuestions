# link:

Solution:
class Sol
{
	public static Node findUnion(Node head1,Node head2)
	{
	    //Add your code here.
	    Node n1 = head1;
	    Node n2 = head2;
	    
	    
	    TreeSet<Integer> numbers = new TreeSet<Integer>();
	    
	    Node top = new Node(0);
	    Node temp = top;
	    

	    while(n1 != null){
	        numbers.add(n1.data);
	        n1 = n1.next;
	    }
	    while(n2 != null){
	        numbers.add(n2.data);
	        n2 = n2.next;
	    }
	    //TreeSet<Integer> sorted = new TreeSet<Integer>(numbers);
	    
	    for (Integer i : numbers) {
            temp.next = new Node(i);
            temp = temp.next;
        }
        
	    //System.out.println(numbers);
	    
	    return top.next;
	    
	    
	}
}
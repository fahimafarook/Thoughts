import java.util.Scanner;
class Node
{
    int data;
    Node next;
    Node prev;
    public Node()
    {
        data=0;
        next=null;
        prev=null;
    }
}


class Function
{                       
    Node head=null;
    Node current=null;
   void create_new(int val)
    {
        Node newnode=new Node();
        newnode.data=val;
        if(head==null)
        {
            head=newnode;
            current=newnode;
            
        }
        else 
        {
           current.next=newnode;
           newnode.prev=current;
           current=newnode;
        }
    }
    void display()
    {
        current=head;
        while(current!=null)
        {
            System.out.println(current.data);
            current=current.next;
        }
    }
}


public class MyClass {
    public static void main(String args[]) {
        Scanner scan=new Scanner(System.in);
         int n=scan.nextInt();
          Function ref=new Function();
         for(int i=0;i<n;i++)
         {
              int val=scan.nextInt();
              ref. create_new(val);
         }
         ref.display();
        System.out.println("done");
    }
}

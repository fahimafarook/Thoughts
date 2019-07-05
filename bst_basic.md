  import java.util.Scanner;
class Node
{
    int data;
    Node left;
    Node rite;
    public Node()
    {
        data=0;
        left=null;
        rite=null;
    }
}
class operation
{
    static Node head=null;
  \  static Node temp=null;
    static  void newone(int val)
    {
        Node newnode=new Node();
        newnode.data=val;
        if(head==null)
        {
        head=newnode;
        }
        
        else 
        {
            temp=head;
            while(true)
            {
                 
                if(val>temp.data)
                {
                    System.out.println("rite");
                    if(temp.rite!=null)
                    {
                    temp=temp.rite;
                    }
                     else if(temp.rite==null)
                    {
                        temp.rite=newnode;
                        break;
                    }
                }
                else if(val<temp.data)
                {
                   System.out.println("left");
                    if(temp.left!=null)
                    {
                    temp=temp.left;
                    }
                     else if(temp.left==null)
                    {
                        temp.left=newnode;
                        break;
                    }
                }
            }
        }
        
    }
    static void display()
    {
        temp=head;
        while(true)
        {
            if(temp!=null)
            {
            System.out.println(temp.data);
            temp=temp.left;
            }
            else 
            break;
        }
    }

 }
  public class MyClass {
    public static void main(String args[]) {
        Scanner scan=new Scanner(System.in);
        int n=scan.nextInt();
        operation obj=new operation();
        for(int i=0;i<n;i++)
        {
            int val=scan.nextInt();
            obj.newone(val);
        }
        obj.display();
    }
}

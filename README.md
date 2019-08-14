 
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
public class carrot
{
    public static void main(String args[])throws Exception
    {
        BufferedReader read=new BufferedReader(new InputStreamReader(System.in));
        System.out.println("Enter no of nodes");
        int n=Integer.parseInt(read.readLine());
        for(int i=0;i<n;i++)
        {
            System.out.println("Enter the value of the node");
            int value=Integer.parseInt(read.readLine());
            System.out.println("Enter how many node its connected to--");
            int no_links=Integer.parseInt(read.readLine());
            
        }
        System.out.println(n);
    }
}
class node
{

}
class operation
{
    
}

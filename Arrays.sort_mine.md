import java.util.Scanner;
public class sorting{
    static  String arr[];
    static int n;
    static void swap(int ie,int je)
    {
               String temp=arr[ie];
               arr[ie]=arr[je];
               arr[je]=temp;
        
    }
    static void sortit(int ie,int je)
    {
        int l1=arr[ie].length();
        int l2=arr[je].length();
        int l;
        if(l1>l2)
        l=l2;
        else 
        l=l1;
        for(int z=0;z<l;z++)
        {
            if(arr[ie].charAt(z)!=arr[je].charAt(z)  &&  arr[ie].charAt(z)>arr[je].charAt(z))
            {
               swap(ie,je);
               break;
            }
            if(z==(l-1) && (l1>l2))
            swap(ie,je);
        }

    }
    public static void main(String args[]) {
       Scanner scan=new Scanner(System.in);
        n=scan.nextInt();
       arr=new String[n];
       for(int i=0;i<n;i++)
       arr[i]=scan.next();
       String decide;
       for(int i=0;i<n;i++)
       {
           for(int j=i+1;j<n;j++)
               sortit(i,j);
       }
         for(int i=0;i<n;i++)
         System.out.println(arr[i]);
      
    }
}

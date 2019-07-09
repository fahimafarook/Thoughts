import java.util.*;
public class MyClass {
    public static void main(String args[]) {
        Scanner scan=new Scanner(System.in);
       String s=scan.next();
       int data[]=new int[26];
       int len=0;
       for(int i=0;i<s.length();i++)
       {
           if(data[s.charAt(i)-97]!=1)
           {
           data[s.charAt(i)-97]=1;
           len++;
           }
       }
      int min=100000;
       for(int i=0;i<s.length();i++)
       {
           for(int j=i;j<s.length() ;j++)
           {
               String nu=s.substring(i,j+1);
               if(nu.length()>=len)
               {
              
                int ref[]=new int[26];
                ref=Arrays.copyOf(data,26);
                int count=0;
                for(int f=0;f<nu.length();f++)
                {
                    if(ref[nu.charAt(f)-97]==1)
                    {
                     ref[nu.charAt(f)-97]=0; 
                     count++;
                    }
                }
                if(count==len)
                {
                    if(nu.length()<min)
                    min=nu.length();
                }
               }
           }
       }
     System.out.println(min);   
    }
}

import java.util.Scanner;
public class MyClass {
    public static void main(String args[]) {
        Scanner scan=new Scanner(System.in);
        String s=scan.next();
        char arr[]=s.toCharArray();
        char stack[]=new char[arr.length];
        int current=0,count=0,max=0;
        for(int i=0;i<arr.length;i++)
        {
            if(arr[i]=='{' )
            {
                current++;
            }
             else if(arr[i]=='}' && current!=0)
            {
                current--;
            }
            else 
            {
                System.out.println("} wrong");
            break;
            }
            if(current!=0)
            count++;
            else 
            count=0;
            if(count>max)
            max=count;
        }
    
        if(current==0)
        {
        System.out.println("blanced and longest length is");
        System.out.print(max-1);
        }
        else 
        {
        System.out.println("unbalanced");
       
        }
    }
}

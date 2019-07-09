import java.util.Scanner;
public class MyClass {
    public static void main(String args[]) {
        Scanner scan=new Scanner(System.in);
        int t=scan.nextInt();
        while(t-->0)
        {
        String s=scan.next();
        char arr[]=s.toCharArray();
        int current=0,count=0,max=0;
        int curly=0,cir=0,sqr=0,flag=0;
        for(int i=0;i<arr.length;i++)
        {
            if(arr[i]=='{' )
                curly++;
            else if(arr[i]=='(' )
                cir++;
            else if(arr[i]=='[' )
                sqr++;
             else if(arr[i]=='}' && curly!=0)
                curly--;
            else if(arr[i]==')' && cir!=0)
                cir--;
            else if(arr[i]==']' && sqr!=0)
                sqr--;
            else 
            {
            flag=1;
            break;
            }
        }
    
        if(curly==0 && cir==0 && sqr==0 && flag==0)
        {
        System.out.println("balanced");
        }
        else 
        {
        System.out.println("not balanced");
        }
        }
    }
    }

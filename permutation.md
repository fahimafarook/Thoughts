import java.util.Scanner;
public class MyClass {
     static int len;
static void permute(String s,String floating)
        {
            if(floating.length()==len)
            System.out.println(floating);
            //System.out.println(floating+"-----------------"+s);
            
            for(int i=0;i<s.length();i++)
            {
                char c=s.charAt(i);
                floating=floating+c;
                s=s.substring(0,i)+s.substring(i+1);
                permute(s,floating);
                floating=floating.substring(0,floating.length()-1);
                s=c+s;
            }
        }

    public static void main(String args[]) {
       
        Scanner scan=new Scanner(System.in);
        String s=scan.next();
        len=s.length();
        System.out.println("floating"+"--------------"+"s");
        permute(s,"");
        
    }
}

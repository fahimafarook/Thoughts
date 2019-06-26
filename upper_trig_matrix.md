import java.util.Scanner;
public class MyClass {
    public static void main(String args[]) {
       Scanner scan=new Scanner(System.in);
       int n=scan.nextInt();
       int name[][]=new int[n][n];
       for(int i=0;i<n;i++)
       {
           for(int j=0;j<n;j++)
           {
               name[i][j]=scan.nextInt();
           }
       }
       int r=0,vr=0;
       int c=0,vc=0;
      
      while(c<n)
      {
          
          vr=r;
          vc=c;
          while(vr<n && vc<n)
          {
          //System.out.println("--"+r+" "+c);
          System.out.println(name[vr][vc]);
          vc++;vr++;
          }
        c++;
          
      }
}
}

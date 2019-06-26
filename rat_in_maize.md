import java.util.Scanner;
public class MyClass {
    static int n,m,data[][],count=0;
    static void cell(int row,int col)
    {
        if(row==n-1 && col==m-1)
        count++;
        System.out.println("cell"+row+" "+col);
        data[row][col]=0;
                                            //left
         if(col-1 >=0)
        {
        if(data[row][col-1]==1)
        {
             System.out.println("left");
             cell(row,col-1);
             
        }
        }
                                             //right
        if(col+1<=(m-1))
        {
         if(data[row][col+1]==1)
        {
            System.out.println("rite");
            cell(row,col+1);
        }
        }
                                             //up
        if(row-1>=0)
        {
         if(data[row-1][col]==1)
        {
            System.out.println("up");
            cell(row-1,col);
        }
        }
                                             //down
        if(row+1<=(n-1))
        {
         if(data[row+1][col]==1)
        {
            System.out.println("down");
            cell(row+1,col);
        }
        }
        data[row][col]=1;
    }
      public static void main(String args[]) {
      Scanner scan=new Scanner(System.in);
       n=scan.nextInt();
       m=scan.nextInt();
       data=new int[n][m];
       for(int i=0;i<n;i++)
       {
          for(int j=0;j<m;j++)
          {
              data[i][j]=scan.nextInt();
          }
       }
       for(int i=0;i<n;i++)
       {
           for(int j=0;j<m;j++)
          {
             System.out.print(data[i][j]);
          }
       }
      cell(0,0);
      System.out.println("count="+count);
    } 
    
}



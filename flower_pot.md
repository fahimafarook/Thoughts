package network;
import java.util.*;

import javax.print.attribute.standard.PrinterLocation;
public class udpclient {
     public static void main(String args[])
     {
    	 Scanner scan=new Scanner(System.in);
    	 String s=scan.nextLine();
    	 int l=s.length();
    	 int arr[]=new int[(l/2)+2];
    	 arr[arr.length-1]=0;
    	 int ct=0;
    	 int counting=0;
    	for(int i=0;i<l;i++)
    	{
		    		
		    arr[ct]=(s.charAt(i))-48;
		    ct++;
		    i++;
		}
		int place=scan.nextInt();
		    	
		if(arr.length>=2)
		{
		   if(arr[0]==0 && arr[1]==0)
		    {
		    	arr[0]=1;
		    	counting++;
		    }
    	}
    	for(int i=1;i<arr.length-1;i++)
    	{
    		if(arr[i-1]==0 && arr[i+1]==0 && arr[i]!=1)
    		{
	    		arr[i]=1;
	    		counting++;
    		}
    		if(counting>=place)
    			break;
    	}
    	
    	if(counting!=place)
    		System.out.println("no");
    	else 
    	{
    		for(int i=0;i<arr.length-1;i++)
    	    	System.out.print(arr[i]);
    	}
     }

}

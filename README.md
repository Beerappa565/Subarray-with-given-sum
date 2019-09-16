# Subarray-with-given-sum
/*package whatever //do not write package name here */

import java.util.*;
import java.lang.*;
import java.io.*;

class GFG {
    public void subarraysum(int arr[],int n,int k)
    {
        int sum=0;
        boolean t=true;
         for(int i=0;i<n;i++)
        {
            sum=0;
            for(int j=i;j<n;j++)
            {
                sum+=arr[j];
                
                    if(sum==k&t==true)
                    {
                        System.out.println(i+1+" "+(1+j));
                        
                        t=false;
                    } 
            }
           
        }
         if(t==true)
            {
                System.out.println(-1);
            }
    }
	public static void main (String[] args) {
	    GFG g=new GFG();
	    Scanner s=new Scanner(System.in);
	    int t=s.nextInt();
        while((t--)!=0){
	    int n=s.nextInt();
	    int k=s.nextInt();
	    int arr[]=new int[n];
	    
	    
	    for(int i=0;i<n;i++)
	    {
	        int j=s.nextInt();
	        arr[i]=j;
	   	}
	   	  g.subarraysum(arr,n,k);
	    }
	}
}

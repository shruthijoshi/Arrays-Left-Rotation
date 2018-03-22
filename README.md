# Arrays-Left-Rotation
Arrays: Left rotation (Given an array of  integers and a number, , perform  left rotations on the array)


import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {
    
    public static int[] leftRotationArray(int a[], int k, int n){
        int temp;
        for( int i=0 ; i<k; i++){          //looping through the array with 'k' rotations
            temp = a[0];                  // assigning the first element to temp varible
            for( int j=1; j<n; j++){
                a[j-1] = a[j];           // swapping values
            }
            a[n-1] = temp;              // appending temp varibale to array
        } 
        return a;
    }

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        int k = in.nextInt();
        int a[] = new int[n];
        
      
        for(int a_i=0; a_i < n; a_i++){
            a[a_i] = in.nextInt();    
        }
        
        int rotateArray[] = new int[n];
        
        /** calling a method to perform left rotation**/
        rotateArray = leftRotationArray(a,k,n);  
        
        /** printing rotated array**/
        for(int i=0 ;i<n; i++){
            System.out.print(rotateArray[i] + " ");
        }
     
    }
}

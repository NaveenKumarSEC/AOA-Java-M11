
# EX 1D Sorted Array using Divide and Conquer Approach.
## DATE:01-02-2026

## AIM:

To write a Java program to for given constraints.
Given two sorted arrays nums1 and nums2 of size m and n respectively, return the median of the two sorted arrays.

The overall run time complexity should be O(log (m+n)).

## Algorithm:

1. Start the program and import the `Scanner` class to take user input.
2. Read the sizes of the two sorted arrays and store their elements in `nums1` and `nums2`.
3. Calculate the total length of both arrays combined.
4. Use the `getMin()` method to sequentially retrieve the smallest elements from both arrays until reaching the median position.
5. Display the median value of the merged sorted arrays as the final output.  

## Program:
```
/*
Program to implement Reverse a String
Developed by: Naveenkumar M
Register Number:  212224230182
*/
```
```
import java.util.Scanner;

public class Solution {
    private int p1 = 0, p2 = 0;

    // Get the smaller value between nums1[p1] and nums2[p2], and move the pointer forward
    private int getMin(int[] nums1, int[] nums2) {
        if (p1 < nums1.length && p2 < nums2.length) {
            return nums1[p1] < nums2[p2] ? nums1[p1++] : nums2[p2++];
        } else if (p1 < nums1.length) {
            return nums1[p1++];
        } else if (p2 < nums2.length) {
            return nums2[p2++];
        }
        return -1; // Should not reach here if input is valid
    }

    // Main logic to find median of two sorted arrays
    public double findMedianSortedArrays(int[] nums1, int[] nums2) {
       //Type code here...
       
       int totlen=nums1.length + nums2.length;
       
       int mid1=-1,mid2=-1;
       
       for(int i=0;i<=totlen/2;i++)
       {
           mid1=mid2;
           mid2=getMin(nums1,nums2);
       }
       
       if(totlen%2==0)
       {
           return (mid1+mid2)/2.0;
       }else{
           return mid2;
       }
    }

    // Main method with user input
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Solution sol = new Solution();

        // Input for nums1
        int m = sc.nextInt();
        int[] nums1 = new int[m];
        for (int i = 0; i < m; i++) {
            nums1[i] = sc.nextInt();
        }

        // Input for nums2
        int n = sc.nextInt();
        int[] nums2 = new int[n];
        for (int i = 0; i < n; i++) {
            nums2[i] = sc.nextInt();
        }

        // Find and display the median
        double median = sol.findMedianSortedArrays(nums1, nums2);
        System.out.println("Median of the two sorted arrays = " + median);
        
        sc.close();
    }
}

```

## Output:

<img width="971" height="344" alt="image" src="https://github.com/user-attachments/assets/c2289405-9880-4424-84ee-8d818f1077e6" />


## Result:
The program successfully implemented and the expected output is verified.

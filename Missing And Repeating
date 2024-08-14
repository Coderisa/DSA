Missing And Repeating(done myself )

Given an unsorted array arr of size n of positive integers. One number 'A' from set {1, 2,....,N} is missing and one number 'B' occurs twice in array. Find these two numbers.
Your task is to complete the function findTwoElement() which takes the array of integers arr and n as parameters and returns an array of integers of size 2 denoting the answer (The first index contains B and second index contains A)
NOTE-ELEMENTS ARE UNORDERED IE(2,1,4,5,4)
Examples
Input: n = 2 arr[] = {2, 2}
Output: 2 1
Explanation: Repeating number is 2 and smallest positive missing number is 1

brute force 
import java.util.*;

public class tUf {

    public static int[] findMissingRepeatingNumbers(int[] a) {
        int n = a.length; // size of the array
        int repeating = -1, missing = -1;

        //Find the repeating and missing number:
        for (int i = 1; i <= n; i++) {
            //Count the occurrences:
            int cnt = 0;
            for (int j = 0; j < n; j++) {
                if (a[j] == i) cnt++;
            }

            if (cnt == 2) repeating = i;
            else if (cnt == 0) missing = i;

            if (repeating != -1 && missing != -1)
                break;
        }
        int[] ans = {repeating, missing};
        return ans;
    }

    public static void main(String[] args) {
        int[] a = {3, 1, 2, 5, 4, 6, 7, 5};
        int[] ans = findMissingRepeatingNumbers(a);
        System.out.println("The repeating and missing numbers are: {"
                           + ans[0] + ", " + ans[1] + "}");
    }
}
O(N2)
s=O(1)
=================================================================================================
T-O(2N)
S-O(N)
 import java.util.*;
     class Solve {
    int[] findTwoElement(int arr[], int n) {
        int[] result = new int[2];
        HashSet<Integer> set = new HashSet<>();//hadhset outside loop

        for (int i = 0; i < n; i++) {
            if (set.contains(arr[i])) {
                result[0] = arr[i]; // Found duplicate
            } else 
                set.add(arr[i]);
        }//fn closed
        for(int i=0;i<n;i++)
        {
            if(!set.contains(i+1))
            result[1]=i+1;
        }

        // Logic to find the missing number (not implemented here)
        // ...

        return result;
    }

    public static void main(String args[]) {
        int arr[] = {1,2,3,3};//repeted element tne ek value khali isliye lengthh of array is same
        int n = arr.length;
        Solve obj = new Solve(); // Create an object
        int[] ans = obj.findTwoElement(arr, n);//cannot call non static metho dinside static 
        System.out.println("array");
        for (int i = 0; i < ans.length; i++) {
            System.out.println(ans[i]);
        }
    }
}

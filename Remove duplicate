Given an integer array nums sorted in non-decreasing order, remove the duplicates in-place such that each unique element appears only once. 
The relative order of the elements should be kept the same. Then return the number of unique elements in nums.
Consider the number of unique elements of nums to be k
BRUTE FORCE
TIME-O(n*log(n))+O(n)
Space Complexity: O(n) 

class Solution {
    public int removeDuplicates(int[] nums) {
        Set<Integer> uniqueElements = new HashSet<>();
        
        for (int num : nums) {
            uniqueElements.add(num);
        }
       
        int index = 0;
        for (int element : uniqueElements) {
            nums[index++] = element;
        }
        Arrays.sort(nums,0,uniqueElements.size());//, starting index, ending index
        
        return uniqueElements.size();
    }
}
************************************************************************************************************8

import java.util.*;//not working on leetcode
public class Main {
    public static void main(String[] args) {
        int arr[] = {1,1,2,2,2,3,3};
        int k = removeDuplicates(arr);
        System.out.println("The array after removing duplicate elements is ");
        for (int i = 0; i < k; i++) {
            System.out.print(arr[i] + " ");
        }
    }
    static int removeDuplicates(int[] arr) {
        HashSet < Integer > set = new HashSet < > ();
        for (int i = 0; i < arr.length; i++) {
            set.add(arr[i]);
        }
        int k = set.size();
        int j = 0;
        for (int x: set) {
            arr[j++] = x;
        }
        return k;
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
OPTIMAL SOLN 
TIME-O(N)
S-O(1)
class Solution {
    public int removeDuplicates(int[] nums) {
        int j=0;
        for(int i=0;i<nums.length;i++)
        {
            if(nums[j]!=nums[i]){
                nums[++j]=nums[i];
            }
        }return ++j;
    }
}

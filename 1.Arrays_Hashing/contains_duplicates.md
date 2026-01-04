## Date 4 Jan 2026

## Question
Given an integer array nums, return true if any value appears at least twice in the array, and return false if every element is distinct.

## My Appoach

As they askeed for duplicate elements for i tried greedy approach by iterating array 2 time which means in n square time complexicity so it gave time limit exceded
the i used hashset for the duplicates as i takes only unique elements but it is slow took 14ms 

##Code snippet

class Solution {
    public boolean containsDuplicate(int[] nums) {
        HashSet<Integer> set = new HashSet<>();
        for(int i=0;i<nums.length;i++){
            
            if(set.contains(nums[i])) return true;
            set.add(nums[i]);
        }
        return false;
    }
}

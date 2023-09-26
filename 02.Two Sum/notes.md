<==================================QUESTION====================================>

Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

Example 1:

Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].

Example 2:

Input: nums = [3,2,4], target = 6
Output: [1,2]

Example 3:

Input: nums = [3,3], target = 6
Output: [0,1]
 

Constraints:
- 2 <= nums.length <= 104
- -109 <= nums[i] <= 109
- -109 <= target <= 109

Only one valid answer exists.

<==================================Solution==================================>


## Understanding the problem

We need to find the 2 indices of the elements in a given array whose elements add up to the target value. 


## Approach 1

To solve this we initialize a dictionary `numMap{}` which stores the indices and elements of the given array(hash table concept) and 
use a variable complement which is the difference btw the target and initial element and check if it is present in the 
dictionary. If it is present, the initial element's index value and the complement' index value are returned. If the 
complement does not exist in the dictionary, then no values are returned.

Time complexity: O(n), since we have a for loop which runs n times in the worst case.

Space Complexity: O(n), In the worst case, we might have to store each element of the array in the numMap{}
dictionary.

## 26- Remove Duplicates from Sorted Array

   - Problem Statement:

         Goal: Remove duplicates in a sorted array nums and return the count k of unique elements.

   - Solution:
        Approach:
            
            Use two pointers:
               - i: Tracks the position of the last unique element.
               - j: Iterates through the array.
            If nums[j] is different from nums[i], increment i and update nums[i] to nums[j].
            Return i + 1 as the count of unique elements.

##
   - Program:

        class Solution(object):
            def removeDuplicates(self, nums):
                """
                :type nums: List[int]
                :rtype: int
                """
                i = 0  # Pointer for the last unique element
                
                for j in range(1, len(nums)):  # Start iterating from the second element
                    if nums[j] != nums[i]:  # Found a unique element
                        i += 1  # Move the unique pointer
                        nums[i] = nums[j]  # Update the next unique position
                
                return i + 1  # Return the count of unique elements

##
   - Explanation of the Code:
           1.Initialization:
                Start with i = 0, pointing to the first element as unique.
           2.Iterate Through Array:
                Compare each element nums[j] with nums[i].
                If they differ, update the next position (i + 1) with the new unique element.
           3.Return the Count:
                i + 1 gives the count of unique elements.

   
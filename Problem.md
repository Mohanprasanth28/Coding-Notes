## 26- Remove Duplicates from Sorted Array

### Problem Statement:

Goal: Remove duplicates in a sorted array nums and return the count k of unique elements.

### Solution:

#### Approach:

Use two pointers:
- i: Tracks the position of the last unique element.
- j: Iterates through the array.

Steps:
1. If nums[j] is different from nums[i], increment i and update nums[i] to nums[j].
2. Return i + 1 as the count of unique elements.

---

### Program:

python
class Solution(object):
    def removeDuplicates(self, nums):       
        i = 0       
        for j in range(1, len(nums)):  
            if nums[j] != nums[i]: 
                i += 1  
                nums[i] = nums[j]
        return i + 1


---

### Explanation of the Code:

#### 1. Initialization:
Start with i = 0, pointing to the first element as unique.

#### 2. Iterate Through Array:
Compare each element nums[j] with nums[i].
- If they differ, update the next position (i + 1) with the new unique element.

#### 3. Return the Count:
i + 1 gives the count of unique elements.

---
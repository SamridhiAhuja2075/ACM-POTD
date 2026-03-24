## Easy: 2 Sum Problem 
Idea is to create a dictionaru that iterates through the list storing every value.\
For each value find its complement(ie target-value), if complement in dictionary ; return both 
Else add value to dictionary 

class Solution(object):\
    def twoSum(self, nums, target):\
        checker=dict()\
        for i in range(len(nums)):\
            complement=target-nums[i]\
            if complement in checker:\
                return[checker[complement],i]\  
            else:\
                checker[nums[i]]=i\ 

![alt text](image-1.png)

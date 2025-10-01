class Solution:
    def threeSum(self, nums: List[int]) -> List[List[int]]:
        nums.sort()
        res = []
        n = len(nums)
        
        for i in range(n-2):
            if i > 0 and nums[i] == nums[i-1]:
                continue
            
            left, right = i+1, n-1
            while left < right:
                total = nums[i] + nums[left] + nums[right]
                
                if total < 0:
                    left += 1
                elif total > 0:
                    right -= 1
                else:
                    res.append([nums[i], nums[left], nums[right]])
                    # Skip duplicates
                    while left < right and nums[left] == nums[left+1]:
                        left += 1
                    while left < right and nums[right] == nums[right-1]:
                        right -= 1
                    left += 1
                    right -= 1
        
        return res






Example Walkthrough

Input: [-1,0,1,2,-1,-4]

Sort → [-4,-1,-1,0,1,2]

i = 0 → nums[i] = -4 → no pair sums to 4

i = 1 → nums[i] = -1

left=2, right=5 → sum = -1+-1+2 = 0 ✅ → add [-1,-1,2]

left=3, right=4 → sum = -1+0+1 = 0 ✅ → add [-1,0,1]

Result → [[-1,-1,2],[-1,0,1]]

⚡ Complexity

Time: O(n²) → outer loop + two pointers

Space: O(1) (excluding output)

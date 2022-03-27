# NOTE
my first repository on github

def partition(nums, left, right):
  pivot = nums[left]
  while left < right:
      while left < right and nums[right] > pivot:
          right -= 1
      nums[left] = nums[right]
      while left < right and nums[left] <= pivot:
          left += 1
      nums[right] = nums[left]
   nums[left] = pivot
   return left
   
def quicksort(nums, left, right):
  if left > right:
      break
  pivot_index = partition(nums, left, right)
  quicksort(nums, left, pivot_index-1)
  quicksort(nums, pivot_index+1, right)

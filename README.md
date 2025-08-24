# Day18 :Remove all occurrences of val in-place. The relative order of the elements may change.  Return the number of elements in nums which are not equal to val.
**Test Cases**
Input: nums = [3,2,2,3], val =3             Output : k = 2, nums = [2,2,_,_]
Input: nums = [0,1,2,2,3,0,4,2], val = 2     Output: k = 5, nums = [0,1,3,0,4,_,_,_]
**Intuition**
1.We need to remove all occurrences of a given value val from the array.
2.We cannot use extra space → we must modify the array itself.
3.Use a pointer k to track the position of the next valid element.
4.Traverse the array:
5.If the element is not equal to val, place it at index k and increment k.
6.If the element is equal to val, skip it.
7.After the loop, the first k elements of the array are the answer
8.Return k as the new length.

**Algorithm Flow**
1.Initialize a pointer k = 0.
→ This pointer represents the position where the next non-val element will be stored.
2.Traverse the array from left to right.
3.If nums[i] != val, then copy it to nums[k] and increment k.
4.If nums[i] == val, skip it.
5.After the loop ends, return k.
→ The first k elements in nums are the final answer.

**Complexity Analysis**
Time Complexity: O(n)
Space Complexity: O(1)

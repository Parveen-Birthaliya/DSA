# Day 3-4: Searching & Sorting

## 🎯 Learning Objectives
- Master Binary Search and its variations
- Understand fundamental sorting algorithms
- Learn when to use which sorting technique
- Solve medium-level problems efficiently

---

## 📚 Theory Concepts

### **Searching Algorithms:**

#### 1. **Linear Search**
- **Time:** O(n) | **Space:** O(1)
- **Use:** Unsorted arrays, small datasets
```python
def linear_search(arr, target):
    for i in range(len(arr)):
        if arr[i] == target:
            return i
    return -1
```

#### 2. **Binary Search** ⭐
- **Time:** O(log n) | **Space:** O(1)
- **Prerequisite:** Sorted array
- **Pattern:** Divide and conquer

```python
def binary_search(arr, target):
    left, right = 0, len(arr) - 1
    
    while left <= right:
        mid = left + (right - left) // 2  # Avoid overflow
        
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    
    return -1

# Test
print(binary_search([1, 3, 5, 7, 9], 7))  # Output: 3
```

**Key Points:**
- Use `mid = left + (right - left) // 2` to avoid integer overflow
- Loop condition: `while left <= right`
- Extremely important for Infosys!

---

### **Sorting Algorithms:**

#### 1. **Bubble Sort**
- **Time:** O(n²) | **Space:** O(1)
- **Stable:** Yes
```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        swapped = False
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
                swapped = True
        if not swapped:  # Optimization
            break
    return arr
```

#### 2. **Selection Sort**
- **Time:** O(n²) | **Space:** O(1)
- **Unstable**
```python
def selection_sort(arr):
    n = len(arr)
    for i in range(n):
        min_idx = i
        for j in range(i+1, n):
            if arr[j] < arr[min_idx]:
                min_idx = j
        arr[i], arr[min_idx] = arr[min_idx], arr[i]
    return arr
```

#### 3. **Insertion Sort**
- **Time:** O(n²) average, O(n) best | **Space:** O(1)
- **Stable:** Yes
- **Use:** Nearly sorted arrays, small datasets
```python
def insertion_sort(arr):
    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1
        while j >= 0 and arr[j] > key:
            arr[j + 1] = arr[j]
            j -= 1
        arr[j + 1] = key
    return arr
```

#### 4. **Merge Sort** ⭐
- **Time:** O(n log n) | **Space:** O(n)
- **Stable:** Yes
```python
def merge_sort(arr):
    if len(arr) <= 1:
        return arr
    
    mid = len(arr) // 2
    left = merge_sort(arr[:mid])
    right = merge_sort(arr[mid:])
    
    return merge(left, right)

def merge(left, right):
    result = []
    i = j = 0
    
    while i < len(left) and j < len(right):
        if left[i] <= right[j]:
            result.append(left[i])
            i += 1
        else:
            result.append(right[j])
            j += 1
    
    result.extend(left[i:])
    result.extend(right[j:])
    return result
```

---

## 💡 Problem Set (15 Problems: 10 Easy + 5 Medium)

### **Searching Problems:**

#### 1. **Binary Search Implementation**
**Difficulty:** Easy  
**LeetCode:** #704

```python
def search(nums, target):
    left, right = 0, len(nums) - 1
    
    while left <= right:
        mid = left + (right - left) // 2
        
        if nums[mid] == target:
            return mid
        elif nums[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    
    return -1

# Test
print(search([1,3,5,7,9,11], 7))  # Output: 3
```

---

#### 2. **Find First and Last Position of Element**
**Difficulty:** Medium  
**LeetCode:** #34  
**Pattern:** Binary Search Variation

```python
def search_range(nums, target):
    def find_first(nums, target):
        left, right = 0, len(nums) - 1
        result = -1
        
        while left <= right:
            mid = left + (right - left) // 2
            if nums[mid] == target:
                result = mid
                right = mid - 1  # Continue searching left
            elif nums[mid] < target:
                left = mid + 1
            else:
                right = mid - 1
        return result
    
    def find_last(nums, target):
        left, right = 0, len(nums) - 1
        result = -1
        
        while left <= right:
            mid = left + (right - left) // 2
            if nums[mid] == target:
                result = mid
                left = mid + 1  # Continue searching right
            elif nums[mid] < target:
                left = mid + 1
            else:
                right = mid - 1
        return result
    
    return [find_first(nums, target), find_last(nums, target)]

# Test
print(search_range([5,7,7,8,8,10], 8))  # Output: [3, 4]
```

**Key Pattern:** Modify binary search to continue searching after finding target

---

#### 3. **Search Insert Position**
**Difficulty:** Easy  
**LeetCode:** #35

```python
def search_insert(nums, target):
    left, right = 0, len(nums) - 1
    
    while left <= right:
        mid = left + (right - left) // 2
        
        if nums[mid] == target:
            return mid
        elif nums[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    
    return left  # Insert position

# Test
print(search_insert([1,3,5,6], 5))  # Output: 2
print(search_insert([1,3,5,6], 2))  # Output: 1
```

---

#### 4. **Find Peak Element**
**Difficulty:** Medium  
**LeetCode:** #162

```python
def find_peak_element(nums):
    left, right = 0, len(nums) - 1
    
    while left < right:
        mid = left + (right - left) // 2
        
        if nums[mid] > nums[mid + 1]:
            right = mid  # Peak is on the left
        else:
            left = mid + 1  # Peak is on the right
    
    return left

# Test
print(find_peak_element([1,2,3,1]))  # Output: 2
```

---

#### 5. **Square Root using Binary Search**
**Difficulty:** Easy  
**LeetCode:** #69

```python
def my_sqrt(x):
    if x < 2:
        return x
    
    left, right = 1, x // 2
    
    while left <= right:
        mid = left + (right - left) // 2
        
        if mid * mid == x:
            return mid
        elif mid * mid < x:
            left = mid + 1
        else:
            right = mid - 1
    
    return right  # Floor value

# Test
print(my_sqrt(8))   # Output: 2
print(my_sqrt(16))  # Output: 4
```

---

### **Sorting Problems:**

#### 6. **Sort an Array (Implement Merge Sort)**
**Difficulty:** Medium  
**LeetCode:** #912

```python
def sort_array(nums):
    def merge_sort(arr):
        if len(arr) <= 1:
            return arr
        
        mid = len(arr) // 2
        left = merge_sort(arr[:mid])
        right = merge_sort(arr[mid:])
        
        return merge(left, right)
    
    def merge(left, right):
        result = []
        i = j = 0
        
        while i < len(left) and j < len(right):
            if left[i] <= right[j]:
                result.append(left[i])
                i += 1
            else:
                result.append(right[j])
                j += 1
        
        result.extend(left[i:])
        result.extend(right[j:])
        return result
    
    return merge_sort(nums)
```

---

#### 7. **Merge Two Sorted Arrays**
**Difficulty:** Easy  
**LeetCode:** #88

```python
def merge(nums1, m, nums2, n):
    # Start from the end
    i, j, k = m - 1, n - 1, m + n - 1
    
    while i >= 0 and j >= 0:
        if nums1[i] > nums2[j]:
            nums1[k] = nums1[i]
            i -= 1
        else:
            nums1[k] = nums2[j]
            j -= 1
        k -= 1
    
    # Copy remaining from nums2
    while j >= 0:
        nums1[k] = nums2[j]
        j -= 1
        k -= 1

# Test
nums1 = [1,2,3,0,0,0]
merge(nums1, 3, [2,5,6], 3)
print(nums1)  # Output: [1,2,2,3,5,6]
```

**Key Trick:** Start merging from the end to avoid overwriting

---

#### 8. **Sort Colors (Dutch National Flag)**
**Difficulty:** Medium  
**LeetCode:** #75

```python
def sort_colors(nums):
    # Three-way partitioning
    low = mid = 0
    high = len(nums) - 1
    
    while mid <= high:
        if nums[mid] == 0:
            nums[low], nums[mid] = nums[mid], nums[low]
            low += 1
            mid += 1
        elif nums[mid] == 1:
            mid += 1
        else:  # nums[mid] == 2
            nums[mid], nums[high] = nums[high], nums[mid]
            high -= 1

# Test
nums = [2,0,2,1,1,0]
sort_colors(nums)
print(nums)  # Output: [0,0,1,1,2,2]
```

**Important Pattern:** Three-pointer technique

---

#### 9. **Kth Largest Element**
**Difficulty:** Medium  
**LeetCode:** #215

```python
def find_kth_largest(nums, k):
    # Method 1: Using sorting (simple but O(n log n))
    nums.sort(reverse=True)
    return nums[k-1]

# Method 2: Using heap (optimal - O(n log k))
import heapq

def find_kth_largest_heap(nums, k):
    return heapq.nlargest(k, nums)[-1]

# Test
print(find_kth_largest([3,2,1,5,6,4], 2))  # Output: 5
```

---

#### 10. **Find Missing Number**
**Difficulty:** Easy  
**LeetCode:** #268

```python
def missing_number(nums):
    n = len(nums)
    expected_sum = n * (n + 1) // 2
    actual_sum = sum(nums)
    return expected_sum - actual_sum

# Alternative: Using XOR
def missing_number_xor(nums):
    result = len(nums)
    for i, num in enumerate(nums):
        result ^= i ^ num
    return result

# Test
print(missing_number([3,0,1]))  # Output: 2
```

---

#### 11. **Count Inversions**
**Difficulty:** Medium  
**Pattern:** Modified Merge Sort

```python
def count_inversions(arr):
    def merge_sort_count(arr):
        if len(arr) <= 1:
            return arr, 0
        
        mid = len(arr) // 2
        left, left_inv = merge_sort_count(arr[:mid])
        right, right_inv = merge_sort_count(arr[mid:])
        
        merged, split_inv = merge_count(left, right)
        
        return merged, left_inv + right_inv + split_inv
    
    def merge_count(left, right):
        result = []
        inversions = 0
        i = j = 0
        
        while i < len(left) and j < len(right):
            if left[i] <= right[j]:
                result.append(left[i])
                i += 1
            else:
                result.append(right[j])
                inversions += len(left) - i
                j += 1
        
        result.extend(left[i:])
        result.extend(right[j:])
        return result, inversions
    
    _, count = merge_sort_count(arr)
    return count

# Test
print(count_inversions([2, 4, 1, 3, 5]))  # Output: 3
```

---

#### 12. **Find Minimum in Rotated Sorted Array**
**Difficulty:** Medium  
**LeetCode:** #153

```python
def find_min(nums):
    left, right = 0, len(nums) - 1
    
    while left < right:
        mid = left + (right - left) // 2
        
        if nums[mid] > nums[right]:
            left = mid + 1
        else:
            right = mid
    
    return nums[left]

# Test
print(find_min([3,4,5,1,2]))  # Output: 1
```

---

### **Additional Practice Problems (3):**

#### 13. **Valid Perfect Square**
```python
def is_perfect_square(num):
    if num < 2:
        return True
    
    left, right = 2, num // 2
    
    while left <= right:
        mid = left + (right - left) // 2
        square = mid * mid
        
        if square == num:
            return True
        elif square < num:
            left = mid + 1
        else:
            right = mid - 1
    
    return False
```

#### 14. **Arranging Coins**
```python
def arrange_coins(n):
    left, right = 0, n
    
    while left <= right:
        mid = left + (right - left) // 2
        curr = mid * (mid + 1) // 2
        
        if curr == n:
            return mid
        elif curr < n:
            left = mid + 1
        else:
            right = mid - 1
    
    return right
```

#### 15. **Two Sum II - Sorted Array**
```python
def two_sum(numbers, target):
    left, right = 0, len(numbers) - 1
    
    while left < right:
        current_sum = numbers[left] + numbers[right]
        
        if current_sum == target:
            return [left + 1, right + 1]  # 1-indexed
        elif current_sum < target:
            left += 1
        else:
            right -= 1
    
    return []
```

---

## 📊 Complexity Comparison

| Algorithm | Best | Average | Worst | Space | Stable |
|-----------|------|---------|-------|-------|--------|
| Bubble Sort | O(n) | O(n²) | O(n²) | O(1) | Yes |
| Selection Sort | O(n²) | O(n²) | O(n²) | O(1) | No |
| Insertion Sort | O(n) | O(n²) | O(n²) | O(1) | Yes |
| Merge Sort | O(n log n) | O(n log n) | O(n log n) | O(n) | Yes |
| Quick Sort | O(n log n) | O(n log n) | O(n²) | O(log n) | No |

---

## ✅ Daily Checklist

**Day 3:**
- [ ] Understand Binary Search completely
- [ ] Solve problems 1-5 (Searching)
- [ ] Solve problems 6-8 (Sorting basics)
- [ ] 20 Time & Work aptitude questions

**Day 4:**
- [ ] Problems 9-12 (Advanced sorting)
- [ ] Problems 13-15 (Additional practice)
- [ ] Practice writing merge sort from scratch
- [ ] 20 Profit & Loss aptitude questions

---

## 🔥 Key Patterns

1. **Binary Search Template:** left <= right, return -1 or left
2. **Modified Binary Search:** Adjust comparison logic
3. **Merge Sort:** Divide, conquer, merge
4. **Two Pointers on Sorted Array:** Common in optimization

---

**Next:** Day 5-6 Mathematics & Bit Manipulation →

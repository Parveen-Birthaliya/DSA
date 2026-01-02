# Day 1-2: Arrays & Strings (Beginner Level)

## 🎯 Learning Objectives
- Master basic array operations and traversals
- Understand string manipulation techniques
- Learn two-pointer technique fundamentals
- Build problem-solving confidence with easy problems

---

## 📚 Theory Concepts

### **Arrays:**
1. **Definition:** Contiguous memory locations storing elements of same type
2. **Key Operations:**
   - Access: O(1)
   - Search: O(n)
   - Insert/Delete at end: O(1)
   - Insert/Delete at position: O(n)

3. **Common Techniques:**
   - Two Pointer Technique
   - Sliding Window
   - Prefix Sum
   - Kadane's Algorithm

### **Strings:**
1. **Definition:** Sequence of characters
2. **Key Properties:**
   - Immutable in many languages
   - Can be treated as character array
3. **Common Operations:**
   - Reversal, Palindrome check
   - Substring operations
   - Pattern matching

---

## 💡 Problem Set (10 Easy Problems)

### **Arrays (5 Problems):**

#### 1. **Find the Largest Element in an Array**
**Difficulty:** Easy  
**Pattern:** Linear Traversal  
**Time:** O(n) | **Space:** O(1)

```python
def find_largest(arr):
    if not arr:
        return -1
    
    max_element = arr[0]
    for num in arr:
        if num > max_element:
            max_element = num
    return max_element

# Test cases
print(find_largest([1, 8, 3, 5, 2]))  # Output: 8
print(find_largest([-5, -2, -8]))     # Output: -2
```

**Edge Cases:** Empty array, all negative, single element

---

#### 2. **Reverse an Array**
**Difficulty:** Easy  
**Pattern:** Two Pointer  
**Time:** O(n) | **Space:** O(1)

```python
def reverse_array(arr):
    left, right = 0, len(arr) - 1
    
    while left < right:
        arr[left], arr[right] = arr[right], arr[left]
        left += 1
        right -= 1
    
    return arr

# Test cases
print(reverse_array([1, 2, 3, 4, 5]))  # Output: [5, 4, 3, 2, 1]
print(reverse_array([10]))              # Output: [10]
```

**Key Learning:** Two-pointer technique for in-place operations

---

#### 3. **Check if Array is Sorted**
**Difficulty:** Easy  
**Pattern:** Linear Traversal  
**Time:** O(n) | **Space:** O(1)

```python
def is_sorted(arr):
    for i in range(1, len(arr)):
        if arr[i] < arr[i-1]:
            return False
    return True

# Test cases
print(is_sorted([1, 2, 3, 4, 5]))    # Output: True
print(is_sorted([1, 3, 2, 4]))       # Output: False
```

---

#### 4. **Remove Duplicates from Sorted Array**
**Difficulty:** Easy  
**Pattern:** Two Pointer  
**Time:** O(n) | **Space:** O(1)

```python
def remove_duplicates(arr):
    if len(arr) <= 1:
        return len(arr)
    
    unique_index = 0
    
    for i in range(1, len(arr)):
        if arr[i] != arr[unique_index]:
            unique_index += 1
            arr[unique_index] = arr[i]
    
    return unique_index + 1

# Test cases
arr1 = [1, 1, 2, 2, 3, 4, 4]
length = remove_duplicates(arr1)
print(arr1[:length])  # Output: [1, 2, 3, 4]
```

**Important:** This is a frequently asked pattern!

---

#### 5. **Left Rotate Array by One Position**
**Difficulty:** Easy  
**Pattern:** Array Manipulation  
**Time:** O(n) | **Space:** O(1)

```python
def rotate_left_by_one(arr):
    if len(arr) <= 1:
        return arr
    
    first = arr[0]
    for i in range(len(arr) - 1):
        arr[i] = arr[i + 1]
    arr[-1] = first
    
    return arr

# Test cases
print(rotate_left_by_one([1, 2, 3, 4, 5]))  # Output: [2, 3, 4, 5, 1]
```

---

### **Strings (5 Problems):**

#### 6. **Reverse a String**
**Difficulty:** Easy  
**Pattern:** Two Pointer  
**Time:** O(n) | **Space:** O(1) or O(n) depending on language

```python
def reverse_string(s):
    # Method 1: Using slicing (Python-specific)
    return s[::-1]

def reverse_string_twopointer(s):
    # Method 2: Two pointer (works in all languages)
    s = list(s)  # Convert to list (strings are immutable in Python)
    left, right = 0, len(s) - 1
    
    while left < right:
        s[left], s[right] = s[right], s[left]
        left += 1
        right -= 1
    
    return ''.join(s)

# Test cases
print(reverse_string("hello"))  # Output: "olleh"
print(reverse_string("a"))      # Output: "a"
```

---

#### 7. **Check if String is Palindrome**
**Difficulty:** Easy  
**Pattern:** Two Pointer  
**Time:** O(n) | **Space:** O(1)

```python
def is_palindrome(s):
    # Remove non-alphanumeric and convert to lowercase
    s = ''.join(c.lower() for c in s if c.isalnum())
    
    left, right = 0, len(s) - 1
    
    while left < right:
        if s[left] != s[right]:
            return False
        left += 1
        right -= 1
    
    return True

# Test cases
print(is_palindrome("racecar"))           # Output: True
print(is_palindrome("A man a plan a canal Panama"))  # Output: True
print(is_palindrome("hello"))             # Output: False
```

**Important:** Handle spaces and case sensitivity!

---

#### 8. **Count Vowels in a String**
**Difficulty:** Easy  
**Pattern:** Frequency Counting  
**Time:** O(n) | **Space:** O(1)

```python
def count_vowels(s):
    vowels = set('aeiouAEIOU')
    count = 0
    
    for char in s:
        if char in vowels:
            count += 1
    
    return count

# Test cases
print(count_vowels("hello world"))  # Output: 3
print(count_vowels("sky"))          # Output: 1
```

---

#### 9. **Find First Non-Repeating Character**
**Difficulty:** Easy  
**Pattern:** HashMap/Frequency Count  
**Time:** O(n) | **Space:** O(1) - limited to 256 chars

```python
def first_non_repeating(s):
    # Count frequency
    freq = {}
    for char in s:
        freq[char] = freq.get(char, 0) + 1
    
    # Find first with frequency 1
    for char in s:
        if freq[char] == 1:
            return char
    
    return None

# Test cases
print(first_non_repeating("leetcode"))    # Output: 'l'
print(first_non_repeating("aabbcc"))      # Output: None
```

**Key Pattern:** Two-pass solution - first count, then find

---

#### 10. **Check if Two Strings are Anagrams**
**Difficulty:** Easy  
**Pattern:** Sorting or Frequency Count  
**Time:** O(n log n) or O(n) | **Space:** O(1)

```python
def are_anagrams(s1, s2):
    # Method 1: Using sorting
    return sorted(s1.lower()) == sorted(s2.lower())

def are_anagrams_optimized(s1, s2):
    # Method 2: Using frequency count (faster)
    if len(s1) != len(s2):
        return False
    
    freq = {}
    
    for char in s1.lower():
        freq[char] = freq.get(char, 0) + 1
    
    for char in s2.lower():
        freq[char] = freq.get(char, 0) - 1
        if freq[char] < 0:
            return False
    
    return True

# Test cases
print(are_anagrams("listen", "silent"))  # Output: True
print(are_anagrams("hello", "world"))    # Output: False
```

---

## 🎯 Practice Problems (Additional)

**Try these on LeetCode/GFG:**
1. Search Insert Position (LeetCode #35)
2. Plus One (LeetCode #66)
3. Move Zeroes (LeetCode #283)
4. Valid Anagram (LeetCode #242)
5. Longest Common Prefix (LeetCode #14)

---

## 📝 Key Takeaways

### **Patterns Learned:**
✅ Two Pointer Technique  
✅ Linear Traversal  
✅ Frequency Counting with HashMap  
✅ In-place Array Manipulation  

### **Common Edge Cases:**
- Empty array/string
- Single element
- All same elements
- Negative numbers (for arrays)
- Special characters (for strings)

### **Time to Master:**
- **Day 1:** Problems 1-5 (Arrays) + Theory
- **Day 2:** Problems 6-10 (Strings) + Additional practice

---

## ✅ Daily Checklist

- [ ] Understood all theoretical concepts
- [ ] Solved all 10 problems without looking at solutions
- [ ] Identified and tested edge cases
- [ ] Practiced 20 aptitude questions (percentages & ratios)
- [ ] Revised patterns in evening

---

## 🔥 Pro Tips

1. **Always think of edge cases first** before coding
2. **Draw examples** for complex logic
3. **Test with sample inputs** before submitting
4. **Time yourself** - aim for 5-7 mins per easy problem
5. **Understand, don't memorize** - patterns matter more than solutions

---

**Next:** Day 3-4 Searching & Sorting →

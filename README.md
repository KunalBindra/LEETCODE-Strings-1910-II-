# LEETCODE-Strings-1910-II-
### Example:
**Input:**  
`s = "daabcbaabcbc"`  
`part = "abc"`

**Step-by-Step Dry Run:**

1. **Initialization:**  
   - `result = ""` (an empty `StringBuilder`).  
   - `n = 3` (length of `part`).

2. **Iterating through `s`:**
   - **First character:**  
     `ch = 'd'`  
     Append `'d'` to `result`: `result = "d"`.  

   - **Second character:**  
     `ch = 'a'`  
     Append `'a'` to `result`: `result = "da"`.  

   - **Third character:**  
     `ch = 'a'`  
     Append `'a'` to `result`: `result = "daa"`.  

   - **Fourth character:**  
     `ch = 'b'`  
     Append `'b'` to `result`: `result = "daab"`.  

   - **Fifth character:**  
     `ch = 'c'`  
     Append `'c'` to `result`: `result = "daabc"`.  
     Check the last `n` characters: `result.substring(result.length() - n) = "abc"`.  
     `"abc".equals(part)` is true, so delete `result.substring(result.length() - n)`.  
     `result = "da"`.  

   - **Sixth character:**  
     `ch = 'b'`  
     Append `'b'` to `result`: `result = "dab"`.  

   - **Seventh character:**  
     `ch = 'a'`  
     Append `'a'` to `result`: `result = "daba"`.  

   - **Eighth character:**  
     `ch = 'a'`  
     Append `'a'` to `result`: `result = "dabaa"`.  

   - **Ninth character:**  
     `ch = 'b'`  
     Append `'b'` to `result`: `result = "dabaab"`.  

   - **Tenth character:**  
     `ch = 'c'`  
     Append `'c'` to `result`: `result = "dabaababc"`.  
     Check the last `n` characters: `result.substring(result.length() - n) = "abc"`.  
     `"abc".equals(part)` is true, so delete `result.substring(result.length() - n)`.  
     `result = "dabaab"`.  

   - **Eleventh character:**  
     `ch = 'b'`  
     Append `'b'` to `result`: `result = "dabaabb"`.  

   - **Twelfth character:**  
     `ch = 'c'`  
     Append `'c'` to `result`: `result = "dabaabcbc"`.  
     Check the last `n` characters: `result.substring(result.length() - n) = "abc"`.  
     `"abc".equals(part)` is true, so delete `result.substring(result.length() - n)`.  
     `result = "dab"`.

3. **End of Loop:**  
   The loop ends, and the final `result = "dab"`.

---

### Output:
`"dab"`

---

### Explanation:
The function processes each character in `s`, appending it to the `result` while checking if the last `n` characters match `part`. If they do, the matching substring is deleted from `result`. This continues until all occurrences of `part` are removed.

### 11. NUMPY − STRING FUNCTIONS

NumPy-யில் **string functions** array-களில் உள்ள string values-ஐ manipulate செய்ய உதவுகின்றன. NumPy-யின் string functions-ஐ பயன்படுத்தி, strings-ஐ uppercase, lowercase, join, replace போன்ற operations செய்யலாம். இது data processing-ஐ எளிதாக்குவதுடன், string manipulation-ஐ memory-efficient-ஆகவும் செய்கிறது.

```python
import numpy as np

# String functions example
string_array = np.array(['hello', 'world'])
upper_case = np.char.upper(string_array)
print("Uppercase Strings:", upper_case)
```

**Output:**

```
Uppercase Strings: ['HELLO' 'WORLD']
```

- **np.char.upper()** function-ஐ பயன்படுத்தி, array-இல் உள்ள strings-ஐ uppercase-ஆக மாற்றியுள்ளோம்.
- **string_array** எனப்படும் array-இல் உள்ள 'hello' மற்றும் 'world' என்பவை 'HELLO' மற்றும் 'WORLD' ஆக மாற்றப்படுகின்றன.
- இந்த function-ஐ strings-ஐ case conversion செய்ய பயன்படுத்தலாம்.

#### Additional String Functions in NumPy

1. **Lowercase Conversion**:

   - **np.char.lower()** function-ஐ strings-ஐ lowercase-ஆக மாற்ற பயன்படுத்தலாம்.

   ```python
   lower_case = np.char.lower(string_array)
   print("Lowercase Strings:", lower_case)
   ```

   **Output:** `Lowercase Strings: ['hello' 'world']`

2. **String Concatenation**:

   - **np.char.add()** function strings-ஐ concatenate செய்ய உதவுகிறது.

   ```python
   concatenated = np.char.add(['hello '], ['world'])
   print("Concatenated String:", concatenated)
   ```

   **Output:** `Concatenated String: ['hello world']`

3. **Replace Substrings**:

   - **np.char.replace()** function strings-இல் உள்ள substring-ஐ மாற்ற பயன்படுகிறது.

   ```python
   replaced_string = np.char.replace('Hello World', 'World', 'NumPy')
   print("Replaced String:", replaced_string)
   ```

   **Output:** `Replaced String: Hello NumPy`

4. **String Split**:

   - **np.char.split()** function strings-ஐ substring-களாக பிரிக்க உதவுகிறது.

   ```python
   split_string = np.char.split('Hello World')
   print("Split String:", split_string)
   ```

   **Output:** `Split String: ['Hello', 'World']`

இந்த string functions NumPy array-களில் உள்ள strings-ஐ manipulate செய்ய memory-efficient methods-ஐ வழங்குகின்றன, இது data processing மற்றும் text handling-ஐ எளிதாக்குகிறது.


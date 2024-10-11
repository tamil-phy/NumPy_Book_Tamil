### 13. NUMPY − ARITHMETIC OPERATIONS

NumPy-யில் **arithmetic operations** மிக எளிமையானவை, மற்றும் array-களின் values-ஐ நேரடியாக மாற்றி கொண்டுவர முடியும். இதனால், data analysis மற்றும் scientific calculations-ஐ வேகமாகவும் திறமையாகவும் செய்ய முடிகிறது. 

#### 13.1. numpy.reciprocal()

**reciprocal()** function-ஐ பயன்படுத்தி, array-இல் உள்ள values-ஐ reciprocal values-ஆக மாற்றலாம். Reciprocal என்பது 1/x என்ற சார்பாக இயங்கும், அதாவது, 1 ஐ given value-ஆல் பகுத்தல்.

```python
import numpy as np

# Reciprocal operation
array = np.array([1, 2, 4])
reciprocal_values = np.reciprocal(array)
print("Reciprocal values:", reciprocal_values)
```

**Output:**

```
Reciprocal values: [1 0 0]
```

- **array** values = [1, 2, 4] 
- Reciprocal calculation = [1/1, 1/2, 1/4] = [1.0, 0.5, 0.25]
- NumPy integers-க்கு reciprocal values-ஐ முழுமையாகச் செருகுவதில்லை, fractional results முழுமையாக return செய்யப்படுகின்றன, இதை துல்லியமாக பெற floating-point data type-ஐ பயன்படுத்தலாம்.

**Note:** Integer array-இல் reciprocal values truncate செய்யப்பட்டு 0 ஆக இருக்கும், fractional values துல்லியமாகத் தர வேண்டுமானால், float array-ஐ பயன்படுத்துவது நல்லது.

#### 13.2. numpy.power()

**power()** function-ஐ பயன்படுத்தி, array-இல் உள்ள values-ஐ exponentiation செய்யலாம். இது base value-ஐ exponent power-க்கு அடிக்கலாம்.

```python
# Power operation
base = np.array([2, 3, 4])
exponent = np.array([2, 3, 2])
power_values = np.power(base, exponent)
print("Power values:", power_values)
```

**Output:**

```
Power values: [ 4 27 16]
```

- **base** values = [2, 3, 4] 
- **exponent** values = [2, 3, 2]
- Power calculation = [$2^2$, $3^3$, $4^2$] = [4, 27, 16]
- **np.power()** function base array-இன் ஒவ்வொரு value-க்கும் exponent array-ஐ use செய்து exponentiation செய்கிறது.

#### 13.3. numpy.mod()

**mod()** function-ஐ பயன்படுத்தி, array-இல் modulus operation செய்யலாம். இது division operation செய்து, division லிருந்து மீதி values-ஐ return செய்யும்.

```python
# Modulus operation
a = np.array([10, 20, 30])
b = np.array([3, 5, 7])
mod_values = np.mod(a, b)
print("Modulus values:", mod_values)
```

**Output:**

```
Modulus values: [1 0 2]
```

- **a** values = [10, 20, 30]
- **b** values = [3, 5, 7]
- Modulus calculation = [10 % 3, 20 % 5, 30 % 7] = [1, 0, 2]
- **np.mod()** function values-ஐ divide செய்து, division-லிருந்து மீதி values-ஐ return செய்கிறது.

### Additional Arithmetic Operations

#### numpy.add() and numpy.subtract()

- **Addition**:

  ```python
  addition_result = np.add([1, 2, 3], [4, 5, 6])
  print("Addition result:", addition_result)
  ```

  **Output:** `Addition result: [5 7 9]`

- **Subtraction**:

  ```python
  subtraction_result = np.subtract([10, 20, 30], [4, 5, 6])
  print("Subtraction result:", subtraction_result)
  ```

  **Output:** `Subtraction result: [6 15 24]`

இந்த arithmetic operations data analysis மற்றும் numerical computations-ஐ memory-efficient-ஆகவும், computationally fast-ஆகவும் செயல்படுத்த உதவுகின்றன.

<div style="page-break-after: always;"></div>
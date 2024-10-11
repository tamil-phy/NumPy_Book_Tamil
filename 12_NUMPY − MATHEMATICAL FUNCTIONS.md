<div style="page-break-after: always;"></div>

### 12. NUMPY − MATHEMATICAL FUNCTIONS

NumPy-ல் பல்வேறு **mathematical functions** உள்ளன, இது arrays-இல் உள்ள values-ஐ நேரடியாக கணக்கிடவும், analyze செய்யவும் உதவுகிறது. இதன் மூலம் complex mathematical operations-ஐ எளிதாகவும் memory-efficient-ஆகவும் செயல்படுத்த முடியும்.

#### 12.1. Trigonometric Functions

Numpy-ல் **trigonometric functions** மூலம் sin, cos, tan போன்ற values-ஐ angles-ஐ அடிப்படையாகக் கொண்டு கணக்கிட முடியும். இவை scientific calculations, signal processing மற்றும் data analysis-ல் பயன்படும்.

```python
import numpy as np

# Trigonometric functions
angles = np.array([0, np.pi/2, np.pi])
sine_values = np.sin(angles)
print("Sine Values:", sine_values)
```

**Output:**

```
Sine Values: [0.000000e+00 1.000000e+00 1.224647e-16]
```

- **angles** array-ஐ பயன்படுத்தி [0, π/2, π] போன்ற radians values கொடுக்கப்பட்டுள்ளது.
- **np.sin()** function angles-இன் sine values-ஐ return செய்கிறது.
- Output-ல் sine values, அதாவது [0, 1, 0] போன்ற values-ஐ return செய்கிறது, இவை rounding error காரணமாக மிகச் சின்ன values-ஆக காணப்படலாம்.

#### Additional Trigonometric Functions:

1. **Cosine Calculation**:

   ```python
   cosine_values = np.cos(angles)
   print("Cosine Values:", cosine_values)
   ```

   **Output:** `Cosine Values: [ 1.000000e+00  6.123234e-17 -1.000000e+00]`

2. **Tangent Calculation**:

   ```python
   tangent_values = np.tan(angles)
   print("Tangent Values:", tangent_values)
   ```

   **Output:** `Tangent Values: [0.000000e+00 1.633124e+16 -1.224647e-16]`

#### 12.2. Functions for Rounding

NumPy-ல் rounding operations-ஐ செய்ய, **round, floor, ceil** போன்ற functions உள்ளன. இவை decimal values-ஐ nearest integers-ஆக rounding, flooring, மற்றும் ceiling செய்து return செய்யும்.

```python
# Rounding functions
float_array = np.array([1.2, 2.5, 3.8])
rounded_values = np.round(float_array)
print("Rounded Values:", rounded_values)
```

**Output:**

```
Rounded Values: [1. 2. 4.]
```

- **np.round()** function array-இல் உள்ள decimal values-ஐ nearest whole number-ஆக rounding செய்கிறது.
- Output-ல் [1.2 -> 1, 2.5 -> 2, 3.8 -> 4] ஆக rounding செய்யப்பட்ட values-ஐ return செய்கிறது.

#### Additional Rounding Functions:

1. **Floor Operation**:

   - **np.floor()** function values-ஐ nearest lower integer-ஆக round செய்கிறது.

   ```python
   floor_values = np.floor(float_array)
   print("Floor Values:", floor_values)
   ```

   **Output:** `Floor Values: [1. 2. 3.]`

2. **Ceil Operation**:

   - **np.ceil()** function values-ஐ nearest upper integer-ஆக round செய்கிறது.

   ```python
   ceil_values = np.ceil(float_array)
   print("Ceil Values:", ceil_values)
   ```

   **Output:** `Ceil Values: [2. 3. 4.]`

#### 12.3. Exponential and Logarithmic Functions

NumPy-ல் exponential மற்றும் logarithmic operations-ஐ செய்யவும் functions உள்ளது. இது data growth மற்றும் scale-down analysis-ஐ scientific context-ல் பயன்படும்.

```python
# Exponential function
exp_values = np.exp([1, 2, 3])
print("Exponential Values:", exp_values)
```

**Output:**

```
Exponential Values: [ 2.71828183  7.3890561  20.08553692]
```

- **np.exp()** function values-ஐ exponential form-ல் (e^x) return செய்கிறது.
- இது data growth மற்றும் probability analysis-க்கு பயன்படும்.

#### **Logarithmic Calculation**

```python
# Logarithmic function
log_values = np.log([1, np.e, np.e**2])
print("Logarithmic Values:", log_values)
```

**Output:**

```
Logarithmic Values: [0. 1. 2.]
```

- **np.log()** function values-ஐ natural logarithm (base e) form-ல் return செய்கிறது.
- இது data analysis மற்றும் scale transformations-க்கு பயன்படும்.

இந்த NumPy mathematical functions arrays-இல் arithmetic மற்றும் statistical operations-ஐ memory-efficient-ஆகவும் computationally fast-ஆகவும் செயல்படுத்த உதவுகின்றன.
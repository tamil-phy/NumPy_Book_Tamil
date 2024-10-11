<div style="page-break-after: always;"></div>

### 4. NUMPY − ARRAY FROM NUMERICAL RANGES

NumPy-யில் **எண்கள் அடிப்படையிலான array** களை உருவாக்க பல functions உள்ளன. இந்த functions array values-ஐ ஏறுவரிசையில் அல்லது குறிப்பிட்ட அளவுகளில் உருவாக்குவதற்கான எளிமையான வழிகளை வழங்குகின்றன. இதனால் sequences மற்றும் ranges கொண்ட array-களை உருவாக்க முடிகிறது.

#### 4.1. numpy.arange

**arange()** function-ஐ பயன்படுத்தி, start value-இல் இருந்து stop value வரை, குறிப்பிட்ட step values-ஐ அடிப்படையாகக் கொண்டு array-ஐ உருவாக்கலாம். இந்த function, Python-ல் உள்ள **range()** function போலவே செயல்படும், ஆனால் NumPy array-களாக values-ஐ return செய்யும்.

```python
import numpy as np

array_arange = np.arange(1, 10, 2)
print("Array using arange:", array_arange)
```

**Output:**

```
Array using arange: [1 3 5 7 9]
```

இங்கு, **arange()** function **start value** 1-இல் இருந்து **stop value** 10 வரை, **step** value 2-ஐ அடிப்படையாகக் கொண்டு array values-ஐ உருவாக்குகிறது. இதனால், 1, 3, 5, 7, 9 போன்ற values கொண்ட array உருவாக்கப்படுகிறது.

#### 4.2. numpy.linspace

**linspace()** function-ஐ பயன்படுத்தி, start value மற்றும் stop value-க்கு இடையில், even spacing values கொண்ட array-ஐ உருவாக்கலாம். இங்கு values எத்தனை elements-ஆக பிரிக்கப்படும் என்பதை user define செய்ய முடியும்.

```python
array_linspace = np.linspace(0, 1, 5)
print("Array using linspace:", array_linspace)
```

**Output:**

```
Array using linspace: [0.   0.25 0.5  0.75 1.  ]
```

இங்கு, **linspace()** function **start** value 0-இல் இருந்து **stop** value 1 வரை, மொத்தம் 5 elements-ஆக values-ஐ even spacing-ஆக பிரிக்கிறது. இதனால், 0, 0.25, 0.5, 0.75, 1.0 போன்ற values கொண்ட array உருவாக்கப்படுகிறது.

#### 4.3. numpy.logspace

**logspace()** function logarithmic spacing கொண்ட array values-ஐ உருவாக்கும். இது logarithmic scale-ல் base powers-இன் values-ஐ கொண்டு array-ஐ return செய்யும்.

```python
array_logspace = np.logspace(1, 3, 5)
print("Array using logspace:", array_logspace)
```

**Output:**

```
Array using logspace: [  10.          31.6227766  100.         316.22776602 1000.        ]
```

இங்கு, **logspace()** function base 10 powers-இல், **start** value 10^1-இல் இருந்து **stop** value 10^3 வரை மொத்தம் 5 values-ஐ logarithmic scale-ல் return செய்கிறது. இதனால், [10, 31.62, 100, 316.22, 1000] போன்ற logarithmic values கொண்ட array உருவாக்கப்படுகிறது.

### Key Differences

- **arange()**: Regular intervals-ஐ கொண்ட array values-ஐ return செய்கிறது.
- **linspace()**: Start மற்றும் stop values இடையே even spacing கொண்ட values-ஐ return செய்கிறது.
- **logspace()**: Logarithmic scale-ல் evenly spaced values-ஐ return செய்கிறது.

இந்த functions, numerical ranges அடிப்படையிலான array-களை உருவாக்குவதில் மிகவும் பயனுள்ளதாக இருக்கின்றன, ஏனெனில் இதனால் sequence-based calculations மற்றும் simulations எளிதாக செய்ய முடிகிறது.
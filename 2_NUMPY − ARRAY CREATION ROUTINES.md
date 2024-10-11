### 2. NUMPY − ARRAY CREATION ROUTINES

NumPy-ல் array-களை உருவாக்க பல்வேறு methods உள்ளன, அவற்றைப் பயன்படுத்தி data handling மற்றும் computation process-களை எளிதாக்கலாம். இப்போது, சில பொதுவாகப் பயன்படுத்தப்படும் array creation functions பற்றி விரிவாகப் பார்ப்போம்.

#### 2.1. numpy.empty

**numpy.empty()** function ஒரு initialization values இல்லாத array-ஐ உருவாக்க பயன்படுகிறது. இதனால், array-இல் உள்ள values ஏதாவது முன்பே memory-யில் இருந்த random values ஆக இருக்கும். இதனால், memory-யில் உள்ள values reset செய்யப்படாமல், அந்த values 그대로 array-இல் வரலாம்.

```python
import numpy as np

empty_array = np.empty((2, 3))
print("Empty array:\n", empty_array)
```

இந்த code-இல், **np.empty()** function-ஐ பயன்படுத்தி 2 rows மற்றும் 3 columns கொண்ட ஒரு array உருவாக்கப்படுகிறது. இந்த array-இல் உள்ள values எல்லாம் எதுவும் initial values இல்லை. அதற்குப் பதிலாக, memory-யில் இருக்கும் junk values அல்லது random values array-இல் காணப்படும்.

**Output:**

```
Empty array:
 [[4.66651921e-310 0.00000000e+000 2.05833592e-312]
 [6.79038654e-313 2.14321575e-312 2.27053550e-312]]
```

இதில், array-இன் values எல்லாம் random values ஆக உள்ளன, ஏனெனில் **numpy.empty( )** function memory-யில் ஏற்கனவே இருக்கும் data-ஐ பயன்படுத்தி array-ஐ உருவாக்குகிறது. இதனால், இந்த function array-ஐ மிக வேகமாக உருவாக்கும் ஆனால் initialization values கொடுக்காது.

- **numpy.empty( )** function பயன்படுத்தப்படும் போது array-இன் values எல்லாம் unpredictable ஆக இருக்கும்.
- Performance அதிகம் தேவைப்படும் போது, initialization values-ஐ avoid செய்ய இந்த function மிகவும் உதவியாக இருக்கும்.
- எப்போது values முக்கியமாக கருதப்படுகின்றனவோ, அப்போது **numpy.zeros( )** அல்லது **numpy.ones( )** போன்ற functions-ஐ பயன்படுத்துவது சிறந்தது.

இந்த function **speed optimization** தேவைப்படும் போது மிகவும் பயனுள்ளதாக இருக்கும், ஏனெனில் இது memory allocation மட்டும் செய்து, values-ஐ initialize செய்யாது.

#### 2.2. numpy.zeros

**zeros()** function-ஐ பயன்படுத்தி, எல்லா elements-உம் 0 values கொண்ட ஒரு array-ஐ உருவாக்கலாம். இந்த function, array-இன் structure-ஐ (shape) user-defined shape-ஆக அமைத்து, அந்த shape-ஐ கொண்டு அனைத்து இடங்களிலும் 0 values-ஐ கொண்டு ஒரு array-ஐ return செய்யும்.

```python
import numpy as np

zeros_array = np.zeros((2, 2))
print("Zeros array:\n", zeros_array)
```

**Output:**

```
Zeros array:
 [[0. 0.]
 [0. 0.]]
```



- இங்கு **np.zeros()** function-ஐ பயன்படுத்தி, 2 rows மற்றும் 2 columns கொண்ட ஒரு array உருவாக்கப்பட்டுள்ளது. இந்த array-இன் எல்லா elements-ம் 0 values கொண்டவை.

- **numpy.zeros()** function memory-யை allocate செய்து, எல்லா elements-க்கும் 0 values கொடுக்கும்.
- இது, array-ஐ முழுமையாக 0 values கொண்டு initialize செய்ய விரும்பும் போது பயன்படும்.
- **zeros()** function data initialization தேவையுள்ள போது மிகவும் பயனுள்ளதாக இருக்கும், ஏனெனில் இது memory-யை efficient-ஆக நிரப்பி array-ஐ உருவாக்குகிறது.



#### 2.3. numpy.ones

**ones()** function-ஐ பயன்படுத்தி, எல்லா elements-உம் 1 values கொண்ட ஒரு array-ஐ உருவாக்கலாம். இந்த function, array-இன் structure-ஐ (shape) user-defined shape-ஆக அமைத்து, அந்த shape-ஐ கொண்டு அனைத்து இடங்களிலும் 1 values-ஐ கொண்டு ஒரு array-ஐ return செய்யும்.

```python
import numpy as np

ones_array = np.ones((3, 3))
print("Ones array:\n", ones_array)
```

**Output:** 

```
Ones array:
 [[1. 1. 1.]
 [1. 1. 1.]
 [1. 1. 1.]]
```

- இங்கு **np.ones()** function-ஐ பயன்படுத்தி, 3 rows மற்றும் 3 columns கொண்ட ஒரு array உருவாக்கப்பட்டுள்ளது.
- இந்த array-இன் எல்லா elements-ம் 1 values கொண்டவை.



இதன் மூலம், **zeros()** மற்றும் **ones()** functions மிகவும் பயனுள்ளதாக இருக்கும், ஏனெனில் அவை predictable values கொண்ட array-களை உருவாக்குகின்றன, computation-ஐ எளிதாக்குகின்றன.
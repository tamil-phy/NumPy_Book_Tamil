# NumPy

### 1. NUMPY − ARRAY ATTRIBUTES

#### 1.1. ndarray.shape

**shape** attribute என்பது NumPy array-இன் அமைப்பை (structure) குறிக்கிறது. இது array-இல் எத்தனை rows மற்றும் columns உள்ளன என்பதை சொல்கிறது. 

எந்த ஒரு array-யும் கையாளும்போது, அதன் **shape** attribute மூலம் array-இன் பரிமாணங்களை (dimensions) அறிந்து கொள்ளலாம். **shape** attribute-ல் உள்ள  values array-இல் உள்ள rows மற்றும் columns எண்ணிக்கையை தருகின்றன.

```python
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6]])
print("Shape of array:", arr.shape)
```

மேலே கொடுக்கப்பட்டுள்ள code-இல், **arr** என்ற 2D array உருவாக்கப்பட்டுள்ளது. இந்த array-இன் **shape** attribute-ஐ பயன்படுத்தி array-இன் அமைப்பை அறியலாம்.

அதாவது, இதன் **output:**

```
Shape of array: (2, 3)
```

  இந்த array-இல் 2 rows மற்றும் 3 columns உள்ளன என்று பொருள். 

இதன் மூலம், **shape** attribute ஒரு Numpy array-இன் கட்டமைப்பை (structure) முழுமையாக குறிக்க உதவுகிறது.

#### 1.2. ndarray.ndim

**ndim** என்பது array-இன் பரிமாணங்களின் எண்ணிக்கையை (number of dimensions) குறிக்கிறது. NumPy array-களின் பரிமாணங்களை புரிந்து கொள்ள இது மிகவும் முக்கியமான attribute ஆகும்.

ஒரு array எத்தனை dimension-களை கொண்டுள்ளது என்பதை **ndim** attribute-ஐ பயன்படுத்தி எளிதில் அறிய முடியும். இதன் உதவியால், 1D, 2D அல்லது multi-dimensional array என்பதை நம்மால் அறிய முடியும்.

```python
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6]])
print("Number of dimensions:", arr.ndim)
```

மேலே கொடுக்கப்பட்டுள்ள code-இல், **arr** என்ற 2D array உருவாக்கப்பட்டுள்ளது. இந்த array-இன் **ndim** attribute-ஐ பயன்படுத்தி array-இன் பரிமாணங்களின் எண்ணிக்கையை (number of dimensions) அறியலாம்.

**Output:**

```
Number of dimensions: 2
```

**2** என்று வரும்போது, இந்த array ஒரு 2D array என்று பொருள். 

இதன் மூலம், **ndim** attribute ஒரு Numpy array-இன் பரிமாணங்களின் எண்ணிக்கையை முழுமையாக அறிய உதவுகிறது.

#### 1.3. numpy.itemsize

**itemsize** attribute ஒரு element-ஐ represent செய்ய memory-யில் எத்தனை bytes எடுக்கின்றது என்பதை அளிக்கிறது. இது, NumPy array-ல் உள்ள ஒவ்வொரு element-க்கும் memory allocation-ஐ எவ்வளவு எடுக்கும் என்பதை அறிய உதவுகிறது.

```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
print("Item size of array:", arr.itemsize, "bytes")
```

இந்த code-இல், **arr** என்ற 1D array உருவாக்கப்பட்டுள்ளது, மற்றும் **itemsize** attribute-ஐ பயன்படுத்தி array-இன் ஒவ்வொரு element-ஐ memory-யில் represent செய்ய எவ்வளவு bytes எடுக்கின்றது என்பதை பார்க்கலாம்.

**Output:**

```
Item size of array: 8 bytes
```

**8 bytes** என்று வரும்போது, அந்த array-இல் உள்ள ஒவ்வொரு element-மும் 8 bytes அளவு memory-யைப் பயன்படுத்துகின்றது என்று பொருள்.

இதன் மூலம், **itemsize** attribute ஒரு Numpy array-இல் உள்ள ஒவ்வொரு element-இன் memory அளவை சரியாக அளக்க உதவுகிறது.

#### 1.4. numpy.flags

**flags** attribute என்பது NumPy array-இன் memory layout-ஐ குறிக்கிறது. இது array-இன் உள்ளமைப்புகள் (properties) மற்றும் memory-இன் அடிப்படையில் array எவ்வாறு அமைக்கப்பட்டுள்ளது என்பதை விளக்குகிறது.

```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
print("Flags of the array:\n", arr.flags)
```

இந்த code-இல், **arr** என்ற 1D array உருவாக்கப்பட்டுள்ளது, மற்றும் **flags** attribute-ஐ பயன்படுத்தி array-இன் memory layout பற்றிய தகவல்களை அறியலாம்.

**Output:**

```
Flags of the array:
  C_CONTIGUOUS : True
  F_CONTIGUOUS : False
  OWNDATA : True
  WRITEABLE : True
  ALIGNED : True
  WRITEBACKIFCOPY : False
```

இந்த **flags** attribute இவ்வாறு array-இன் memory layout பற்றிய விவரங்களை கொடுக்கிறது:

- **C_CONTIGUOUS**: Array-இன் memory layout C-style (row-major) ஆக உள்ளது.
- **F_CONTIGUOUS**: Array-இன் memory layout Fortran-style (column-major) ஆக இல்லை.
- **OWNDATA**: Array-க்கு சொந்தமாக memory data இருக்கிறது.
- **WRITEABLE**: Array-இல் உள்ள data மாற்றக்கூடியது.
- **ALIGNED**: Data memory alignment சரியாக உள்ளது.
- **WRITEBACKIFCOPY**: Write-back operation தேவைப்படும்போது False ஆகும்.

இதன் மூலம், **flags** attribute NumPy array-இன் memory layout மற்றும் array-இன் உள்ளமைப்புகள் பற்றிய முழு தகவல்களை வழங்குகிறது.

<div style="page-break-after: always;"></div>

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

<div style="page-break-after: always;"></div>

### 3. NUMPY − ARRAY FROM EXISTING DATA

Numpy-ல் array-களை உருவாக்குவதற்கான முக்கியமான வழிகளில் ஒன்றாக **Existing data**-விலிருந்து array-ஐ உருவாக்குவது அமைகிறது. இது Python-ல் ஏற்கனவே இருக்கும் data structures, போன்றவை (lists, buffers, iterables) கொண்டு நமக்கு தேவையான array-களை எளிதாக உருவாக்க உதவுகிறது. இதனால் data-ஐ NumPy-யின் powerful array operations-இல் பயன்படுத்த முடியும்.

#### 3.1. numpy.asarray

**asarray()** function-ஐ பயன்படுத்தி, ஒரு existing data-ஐ NumPy array-ஆக மாற்றலாம். இதன் முக்கிய பயனாக, இதனால் original data-ஐ clone செய்து, array-ஆக மாற்றுவதில் பயன்படுத்தப்படும் memory space குறைவாக இருக்கும்.

```python
import numpy as np

# list data-யை numpy array-ஆக மாற்றுதல்
list_data = [1, 2, 3, 4, 5]
array_data = np.asarray(list_data)
print("Array from list:", array_data)
```

**Output:**

```
Array from list: [1 2 3 4 5]
```

இந்த Code-இல், ஒரு Python list **list_data**-ஐ **asarray()** function-ஐ பயன்படுத்தி NumPy array-ஆக மாற்றுகிறோம். இதன் மூலம், original data type retain ஆகிறது (சேமித்து),  list_data array-ஆக மாற்றப்படுகிறது, மேலும் நம்மால் memory usage-யை திறமையாக கையாள முடிகிறது.

#### 3.2. numpy.frombuffer

**frombuffer()** method-ஐ பயன்படுத்தி, buffer-ல் உள்ள data-ஐ NumPy array-ஆக மாற்ற முடியும். buffer-ல் உள்ள binary data-ஐ NumPy array-இல் மாற்றுவதன் மூலம், அதனுடன் அடுத்தடுத்த data manipulations மேற்கொள்ள உதவுகிறது.

```python
buffer = b'Hello World'
array_buffer = np.frombuffer(buffer, dtype='S1')
print("Array from buffer:", array_buffer)
```

**Output:**

```
Array from buffer: [b'H' b'e' b'l' b'l' b'o' b' ' b'W' b'o' b'r' b'l' b'd']
```

இங்கு, **buffer** என்ற binary data-ஐ **frombuffer()** method மூலம் NumPy array-ஆக மாற்றுகிறோம். இதனால், byte data அலகு அலகாக array-இல் element-களாகக் கிடைக்கிறது. இதுபோன்ற conversions binary data parsing மற்றும் manipulation-ஐ எளிதாக்கும்.

#### 3.3. numpy.fromiter

**fromiter()** function-ஐ பயன்படுத்தி, iterable object-களை NumPy array-ஆக மாற்ற முடியும். இது memory-efficient-ஆகவும், high-performance data conversion-ஐ உருவாக்கவும் உதவுகிறது. **fromiter()** iterable values-ஐ array-ஆக dynamic-ஆக மாற்றுவதற்கான ஒரு method ஆகும். Iterables-ல் இருந்து continuous data stream-ஐ NumPy array-ஆக உருவாக்குவதன் மூலம், sequence-களை நேரடியாக array-களாக மாற்ற முடியும். 

```python
iterable = (x*x for x in range(5))
array_iter = np.fromiter(iterable, dtype='int32')
print("Array from iterable:", array_iter)
```

**Output:**

```
Array from iterable: [ 0  1  4  9 16]
```

இந்த Code-இல், **iterable** என்ற generator expression-ஐ **fromiter()** method மூலம் NumPy array-ஆக மாற்றுகிறோம். இதனால் iterator-ல் உள்ள data sequential order-ஆக array-இல் சேமிக்கப்படுகிறது.

**குறிப்புகள்:**

- **asarray()** function data-ஐ NumPy array-ஆக மாற்றும்போது, original data-ஐ duplicate செய்யாமல், அதை memory-efficient-ஆக array-ஆக மாற்றும்.
- **frombuffer()** method buffer-ல் உள்ள binary data-ஐ NumPy array-ஆக மாற்றி, low-level data manipulation செய்ய உதவுகிறது.
- **fromiter()** method iterators அல்லது generators கொண்டு data stream-ஐ array-ஆக மாற்றும், sequence operations-ஐ அதிக அளவில் எளிமையாக மாற்றுகிறது.
- **Memory Efficiency**: **fromiter()** function memory-ஐ குறைவாக பயன்படுத்தி iterable object-களை array-ஆக நேரடியாக மாற்ற உதவுகிறது. இது, ஒரு iterator data-ஐ dynamic-ஆக உருவாக்கி, memory allocation-ஐ தற்செயலாக (lazy evaluation) செய்ய அனுமதிக்கிறது.
- **High Performance**: Large-scale data conversions-இல் **fromiter()** function வேகமாக செயல்படுகிறது. Python list comprehension-ஐப் பயன்படுத்தி data-ஐ உருவாக்கும் முறைக்குப் பதிலாக, NumPy-யின் vectorized operations-ஐ பயன்படுத்துவதால், performance அதிகரிக்கிறது.

இதனால், NumPy-யில் data-ஐ நமக்கு வேண்டிய படி நமக்கு ஏற்கனவே உள்ள structures-இல் இருந்து array-களாக மாற்றி manipulations மற்றும் calculations செய்ய நம்மால் முடியும்.

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

<div style="page-break-after: always;"></div>

### 5. NUMPY − INDEXING & SLICING

NumPy array-களில் **indexing** மற்றும் **slicing** methods மிக முக்கியமானவை, ஏனெனில் இவையால் array-களின் தனிப்பட்ட elements-ஐ அணுகுவதோடு, array-களின் ஒரு பகுதியை எளிதாக பிரிக்கவும் முடிகிறது. இவை data extraction மற்றும் manipulation-ஐ மிக எளிதாக்குகின்றன.

```python
import numpy as np

arr = np.array([10, 20, 30, 40, 50])
print("Element at index 2:", arr[2])  # Indexing
print("Sliced array:", arr[1:4])  # Slicing
```

**Output:**

```
Element at index 2: 30
Sliced array: [20 30 40]
```

#### Explanation

- **Indexing**: Indexing-ஐ பயன்படுத்தி, array-இல் உள்ள குறிப்பிட்ட இடத்தில் இருக்கும் element-ஐ நேரடியாக அணுக முடியும். Example-இல், **arr[2]** என்பது array-இன் மூன்றாவது இடத்தில் உள்ள value **30**-ஐ அணுகுகிறது.

- **Slicing**: Slicing-ன் மூலம், array-இன் ஒரு பகுதியை எளிதாக பிரித்து, அந்த பகுதியில் உள்ள values-ஐ return செய்யலாம். Example-இல், **arr[1:4]** என்பது array-இல் இரண்டாவது இடத்திலிருந்து நான்காவது இடம் வரை உள்ள values **[20, 30, 40]**-ஐ return செய்கிறது.

இந்த methods data extraction-ஐ மிக எளிமையாக மாற்றுகின்றன, மேலும் NumPy array-களுடன் நாம் பயனுள்ளதாக மற்றும் திறமையாக செயல்பட உதவுகின்றன.

<div style="page-break-after: always;"></div>

### 6. NUMPY − ADVANCED INDEXING

NumPy-இல் **advanced indexing** முலம் array values-ஐ எளிதாக அணுகவும், update செய்யவும் அனுமதிக்கின்றன. இவை data selection மற்றும் manipulation-ஐ மேலும் திறமையாக செயல்படுத்த உதவுகின்றன.

#### 6.1. Integer Indexing

Integer indexing-ன் மூலம் array-யின் குறிப்பிட்ட இடங்களில் உள்ள elements-ஐ எளிதாக பெறலாம். இதன் மூலம், multi-dimensional array-களில் அதிக specific data points-ஐ எளிதாக அணுக முடியும்.

```python
import numpy as np

arr = np.array([[1, 2], [3, 4], [5, 6]])
print("Element at position (2, 1):", arr[2, 1])
```

**Output:**

```
Element at position (2, 1): 6
```

இந்தCode-இல், **arr[2, 1]** என்பது array-இன் மூன்றாவது row-இல் உள்ள இரண்டாவது element-ஐ காட்டுகிறது, அதாவது value **6**.

#### 6.2. Boolean Array Indexing

Boolean array indexing-ன் மூலம், condition அடிப்படையில் array values-ஐ எளிதாக filter செய்ய முடியும். இது data analysis மற்றும் condition-based filtering-ஐ மிக எளிதாக்கும்.

```python
arr = np.array([10, 20, 30, 40, 50])
condition = arr > 25
print("Filtered array with condition:", arr[condition])
```

**Output:**

```
Filtered array with condition: [30 40 50]
```

இந்த Code-இல், condition **arr > 25**-ஐ அடிப்படையாகக் கொண்டு array-இல் 25-ஐ விட அதிகமான values மட்டுமே return செய்கின்றன. இதனால் **[30, 40, 50]** என்ற values மட்டும் filter ஆகின்றன.

<div style="page-break-after: always;"></div>

### 7. NUMPY − BROADCASTING

NumPy-யில் **broadcasting** என்பது shape-கள் வேறுபட்ட array-களை arithmetic operations-ல் பயன்படுத்த ஒரு நுட்பமாகும். இது data-ஐ duplicate செய்யாமல், memory-efficient-ஆக operations-ஐ நேரடியாக செய்ய உதவுகிறது. Broadcasting-ஐ பயன்படுத்தி arrays-இல் arithmetic operations செய்யும்போது, NumPy data-ஐ தானாகவே மிக எளிதாகப் பொருந்தும் விதமாக மாற்றுகிறது.

#### Broadcasting என்றால் என்ன?

Broadcasting என்பது NumPy-யின் திறனாக, இரண்டு array-களின் shape-கள் பொருந்தாதபோதும், arithmetic operations-ஐ செய்து முடிக்க data-ஐ தானாக விரிவாக்கி ஆக்க முறையாகும். NumPy-யின் broadcasting விதிகள் array-களை ஒன்று சேர்க்கவும், குறைந்த memory-யில் calculations செய்யவும் உதவுகின்றன.

```python
import numpy as np

# Broadcasting உதாரணம்
array1 = np.array([1, 2, 3])
array2 = np.array([[1], [2], [3]])
print("array1 shape: ", array1.shape)
print("array2 shape: ", array2.shape)
result = array1 + array2
print("Broadcasted array:\n", result)
```

**Output:**

```
Broadcasted array:
 [[2 3 4]
 [3 4 5]
 [4 5 6]]
```

#### விளக்கம்:

- **array1**: 1D array, இதன் shape `(3,)`
- **array2**: 2D array, இதன் shape `(3, 1)`

இங்கு, broadcasting நுட்பம் **array1**-ஐ **array2**-இன் shape-க்கு பொருந்தும் வகையில் தானாக விரிவாக்குகிறது, அதன் பிறகு arithmetic operation நடக்கிறது. NumPy இவ்வாறு array-களை தானாக பொருத்துவது மூலமாக memory-யை சிக்கனமாக பயன்படுத்தி calculations செய்யும் திறன் அதிகரிக்கிறது.

Broadcasting பின்பற்ற வேண்டிய முக்கியமான விதிமுறைகள்:

1. **Dimension Compatibility**: இரண்டு array-களின் dimensions சமமாக இருக்க வேண்டும் அல்லது அவற்றில் ஏதாவது ஒரு dimension 1 என்ற அளவிற்கு சமமாக இருக்க வேண்டும்.
2. **Automatic Expansion**: Lower-dimensional arrays தானாகவே higher-dimensional array-க்கு பொருந்தும் வகையில் விரிவாக்கப்படுகின்றன.
3. **Efficient Operations**: Broadcasting-ன் மூலம் unnecessary data duplication-ஐ தவிர்க்கும் மற்றும் memory-யை சிறப்பாக பயன்படுத்தும்.
4. **Memory Efficiency**: Broadcasting data duplication இல்லாமல் calculations செய்ய உதவுகிறது, இதனால் memory utilization மேம்படுகிறது.
5. **Code Simplification**: Code-ஐ சுருக்கமாகவும் சுலபமாகவும் எழுத முடிகிறது, அதனால் complex array operations-ஐ நேரடியாக எழுதி புரியவைக்கலாம்.
6. **Performance**: Broadcasting arithmetic operations-ஐ வேகமாக செய்யும் திறன் கொண்டது, ஏனெனில் NumPy backend-ல் vectorized operations பயன்படுத்துகிறது.

### எப்போது Broadcasting உதவிகரமாக இருக்கும்?

- **வெவ்வேறு Shape கொண்ட Array-களுக்கு Calculations செய்யும்போது**.
- **Data Analysis மற்றும் Machine Learning** calculations செய்யும் போது broadcasting மிகவும் முக்கியம்.

Broadcasting மூலம், NumPy பயனர் data-ஐ duplicate செய்யாமல் எளிமையாகவும் திறமையாகவும் operations-ஐ செய்ய உதவுகிறது, இதன் மூலம் high-performance calculations மற்றும் memory efficiency ஆகியவை அதிகரிக்கின்றன.

<div style="page-break-after: always;"></div>

### 8. NUMPY − ITERATING OVER ARRAY

NumPy array-களை **iterate** செய்வது Python list-களை iterate செய்வதைப் போலவே எளிதானது. NumPy array-களில் iteration செய்யும் நுட்பங்கள் அதிக துல்லியமாகவும் வேகமாகவும் செயல்படுவதற்காக வடிவமைக்கப்பட்டுள்ளன. இதன் மூலம், multi-dimensional array-களில் iteration செய்யும்போது memory efficiency மற்றும் execution speed அதிகரிக்கின்றன.

#### 8.1. Iteration Order

NumPy array-களை iterate செய்வதில் **row-major** அல்லது **column-major** order-ல் iteration செய்ய முடியும். 

```python
import numpy as np

# Row-major order iteration
array = np.array([[1, 2, 3], [4, 5, 6]])
for row in array:
    print("Row:", row)

# Column-major order iteration
for element in array.flat:
    print("Element:", element)
```

**Output:**

```
Row: [1 2 3]
Row: [4 5 6]
Element: 1
Element: 2
Element: 3
Element: 4
Element: 5
Element: 6
```

- **Row-major** order-ல் iteration செய்யும் போது, ஒவ்வொரு row-யும் தனித்தனியாக iterate செய்யப்படுகிறது. Example-இல், `array`-இன் ஒவ்வொரு row-ஐ print செய்கிறோம்.
- **flat** attribute-ஐ பயன்படுத்தி, array-இன் அனைத்து elements-ஐ flatten செய்து, அவற்றை column-major order-ல் iterate செய்கிறோம்.

**Row-major order** என்பதனால் rows-ஐ முன்னுரிமை கொடுத்து iterate செய்யப்படுகிறது, அதாவது முழு row-ஐ முன்னதாக process செய்யும்.
**flat** attribute-ஐ பயன்படுத்தி, multi-dimensional array-ஐ ஒரு single-dimensional array போல iterate செய்ய முடியும்.

#### 8.2. Modifying Array Values

Iteration-ஐ பயன்படுத்தி array values-ஐ நேரடியாக மாற்றவும் (update) முடியும். இதனால், array-இன் original values-ஐ iteration முறையில் update செய்வது எளிதாகும்.



```python
# Array values-ஐ iterate செய்து மாற்றுதல்
for i in np.nditer(array, op_flags=['readwrite']):
    i[...] = i * 2
print("Modified array:\n", array)
```

**Output:**

```
Modified array:
 [[ 2  4  6]
 [ 8 10 12]]
```

- **`np.nditer()`**:
  - **`np.nditer()`** என்பது NumPy array-ஐ iterate செய்ய உதவும் ஒரு iterator object-ஐ உருவாக்குகிறது.
  - இது multi-dimensional arrays-ஐ எளிமையாக iterate செய்யக்கூடியதாக மாற்றுகிறது.

- **`op_flags=['readwrite']`**:
  - **`op_flags`** argument-ஐ பயன்படுத்தி iteration செய்யும் போது array-ஐ எப்படி access செய்ய வேண்டும் என்பதை நிர்ணயிக்க முடியும்.
  - **`readwrite`** flag-ஐ பயன்படுத்துவதன் மூலம் iteration செய்து கொண்டிருக்கும் போது array values-ஐ both (மேம்படுத்தவும் மற்றும் படிக்கவும்) access செய்ய முடிகிறது.

- **`i[...] = i * 2`**:
  - **`i[...]`** மூலம், iterator (i) pointing செய்யும் array-இன் தற்போதைய element-ஐ access செய்கிறோம்.
  - இங்கு, ஒவ்வொரு element-ஐ இரட்டிப்பு (double) செய்து, அதை array-இல் replace செய்கிறோம், அதாவது original array-இன் values-ஐ update செய்கிறோம்.

### Iteration-ஐ எப்போது பயன்படுத்துவது?

- **Row-major order iteration**: நமக்கு row-by-row analysis அல்லது manipulation தேவையான போது.
- **flat attribute iteration**: Multi-dimensional array-களை flatten செய்து, அவர்களுடன் சுலபமாக iterate செய்ய வேண்டிய போது.
- **Modifying array values**: Iteration செய்கையில் values-ஐ நேரடியாக update செய்ய விரும்பும் போது.

#### Iteration-ன் முக்கியத்துவம்:

NumPy-யில் iteration methods-ஐ பயன்படுத்தி array values-ஐ access மற்றும் update செய்வது நமக்கு மிக வேகமாகவும் திறமையாகவும் data handling செய்ய உதவுகிறது. இதனால், data manipulation, analysis மற்றும் computation போன்ற செயல்பாடுகள் மிக எளிமையாகும்.

### 8.3. External Loop

**External Loop** iteration நுட்பம் array values-ஐ மேம்படுத்தி மற்றும் memory-efficient-ஆக iterate செய்ய உதவுகிறது. **external_loop** flag-ஐ பயன்படுத்தி, iteration செய்யும்போது data-ஐ ஒரு continuous block-ஆக iterate செய்ய முடியும், இதனால் execution speed அதிகரிக்கிறது.

```python
import numpy as np

# External loop iteration
array = np.array([[2, 4, 6], [8, 10, 12]])
for x in np.nditer(array, flags=['external_loop'], order='F'):
    print("External loop iteration:", x)
```

**Output:**

```
External loop iteration: [2 8]
External loop iteration: [ 4 10]
External loop iteration: [ 6 12]
```

- **`flags=['external_loop']`**: இந்த flag-ஐ பயன்படுத்தி, iteration செய்யும் போது data continuous block-ஆக iterate செய்யப்படுகிறது.
- **`order='F'`**: Iteration order-ஐ Fortran-style (column-major) ஆக மாற்றுகிறது, இதனால் column-wise data-ஐ iterate செய்யலாம்.

External loop iteration-ஐ column-wise data handling-க்கு பயன்படுத்தும்போது, இது calculations மற்றும் data processing-ஐ வேகமாகவும் memory-efficient-ஆகவும் செய்கிறது.

### 8.4. Broadcasting Iteration

Broadcasting iteration மூலம் shape வேறுபட்ட array values-ஐ ஒரே நேரத்தில் iterate செய்ய உதவுகிறது. இது NumPy-யின் broadcasting principle-ஐ பயன்படுத்தி, operations-ஐ சிறப்பாக நிறைவேற்றுகிறது.

```python
import numpy as np

array1 = np.array([1, 2, 3])
array2 = np.array([[1], [2], [3]])
for x, y in np.nditer([array1, array2]):
    print(f"x: {x}, y: {y}")
```

**Output:**

```
x: 1, y: 1
x: 2, y: 1
x: 3, y: 1
x: 1, y: 2
x: 2, y: 2
x: 3, y: 2
x: 1, y: 3
x: 2, y: 3
x: 3, y: 3
```

- **Broadcasting Iteration**: Broadcasting iteration-ஐ பயன்படுத்தி shape-ல் வேறுபாடுகள் இருந்தாலும் array values-ஐ இணைத்து iterate செய்ய முடிகிறது.
- **`np.nditer([array1, array2])`**: இரண்டு array-களையும் ஒரே iteration-ல் பயணிக்க பயன்படுகிறது, அதனால் values-ஐ side-by-side compare மற்றும் process செய்ய முடிகிறது.

இந்த broadcasting iteration data manipulation மற்றும் array operations-ஐ மிகவும் சுலபமாகவும் திறமையாகவும் செய்கிறது, ஏனெனில் இது different shapes கொண்ட array-களையும் ஒரு நேரத்தில் iterate செய்து எளிதாக இணைக்கிறது.

<div style="page-break-after: always;"></div>

### 9. NUMPY – ARRAY MANIPULATION

NumPy, array-களை மாற்றவும் அதனை மாற்றி அமைக்கவும் பல்வேறு வழிகள் உண்டு. அதாவது இவை array-களின் structure-ஐ மாற்றுவதில், flatten செய்வதில், மற்றும் iterator-களை பயன்படுத்துவதில் மிகவும் பயனுள்ளதாக இருக்கும்.

#### 9.1. numpy.reshape

**reshape()** function-ஐ பயன்படுத்தி, NumPy array-இன் shape-ஐ மாற்றலாம். இதனால், array-இல் உள்ள elements-ஐ மறு அமைப்பு செய்து, data structure-ஐ எளிதாக மாற்ற முடியும்.

```python
import numpy as np

# Reshape operation
array = np.array([1, 2, 3, 4, 5, 6])
reshaped_array = array.reshape(2, 3)
print("Reshaped array:\n", reshaped_array)
```

**Output:**

```
Reshaped array:
 [[1 2 3]
 [4 5 6]]
```

- **reshape()** function-ஐ பயன்படுத்தி, 1D array `[1, 2, 3, 4, 5, 6]`-ஐ 2 rows மற்றும் 3 columns கொண்ட 2D array-ஆக மாற்றியுள்ளோம்.
- Reshape operation செய்வதற்கு array-இன் மொத்த elements எண்ணிக்கை மாறாமல் இருக்க வேண்டும்.
- **reshape()**: Array-இன் structure-ஐ மாற்ற உதவும், ஆனால் original shape-க்கு elements எண்ணிக்கை பொருந்த வேண்டும்.

**குறிப்பு**: Reshape operation செய்யும் போது, புதிய shape-க்கு elements கிட்டத்தட்ட இருந்தால் மட்டுமே அது செயல்படும்.

#### 9.2. numpy.ndarray.flat

**flat** attribute-ஐ பயன்படுத்தி, array-இன் elements-ஐ ஒரு iterator-ஆக பெறலாம். இதன் மூலம், multi-dimensional array-ஐ ஒரு iterator-ஆக flatten செய்து iterate செய்ய முடியும்.

```python
# Flat iteration
for element in array.flat:
    print("Flat element:", element)
```

**Output:**

```
Flat element: 1
Flat element: 2
Flat element: 3
Flat element: 4
Flat element: 5
Flat element: 6
```

- **flat** attribute-ஐ பயன்படுத்தி, multi-dimensional array-இல் உள்ள elements-ஐ ஒரு continuous sequence-ஆக iterator-ஆக iterate செய்கிறோம்.
- இது memory-efficient-ஆக array-ஐ handle செய்ய உதவுகிறது, மற்றும் எளிதாக elements-ஐ access செய்ய அனுமதிக்கிறது.

#### 9.3. numpy.ndarray.flatten

**flatten()** method-ஐ பயன்படுத்தி, multi-dimensional array-ஐ ஒரு single-dimensional array-ஆக மாற்றலாம். இது array-இல் உள்ள அனைத்து elements-ஐ ஒரு single line-ல் வைத்து return செய்யும்.

```python
# Flatten operation
flattened_array = array.flatten()
print("Flattened array:", flattened_array)
```

**Output:**

```
Flattened array: [1 2 3 4 5 6]
```

- **flatten()** method-ஐ பயன்படுத்தி multi-dimensional array-ஐ ஒரே dimension-க்குள் flatten செய்து convert செய்கிறோம்.
- Flatten operation array-ஐ reshape செய்யாமல், ஒரு continuous structure-ஆக return செய்யும்.
- **flatten()**: Multi-dimensional array-ஐ single-dimensional array-ஆக மாற்றும், இது ஒரு new flattened copy-ஐ return செய்யும்.

#### 9.4. numpy.ravel

**ravel()** method-ஐ பயன்படுத்தி, multi-dimensional array-ஐ flattened array-ஆக மாற்றலாம். இது **flatten()** போலவே செயல்படும், ஆனால் பெரும்பாலான சூழல்களில் original memory-யை share செய்ய memory-efficient ஆக செயல்படுகிறது.

```python
import numpy as np

# Ravel operation
array = np.array([[1, 2, 3], [4, 5, 6]])
raveled_array = array.ravel()
print("Raveled array:", raveled_array)
```

**Output:**

```
Raveled array: [1 2 3 4 5 6]
```

- **ravel()** method multi-dimensional array-ஐ flattened array-ஆக மாற்றி return செய்கிறது.
- இது memory-யை சிக்கனமாக பயன்படுத்தி, wherever possible, original data-ஐ share செய்வதால் memory allocation குறைவாக இருக்கும்.

#### 9.5. numpy.transpose

**transpose()** function-ஐ பயன்படுத்தி, array-இன் axes-ஐ மாற்றி அமைக்க முடியும். இது row-களை column-களாகவும் column-களை row-களாகவும் மாற்றுவதற்கான method ஆகும்.

```python
# Transpose operation
reshaped_array = np.array([[1, 2, 3], [4, 5, 6]])
transposed_array = reshaped_array.transpose()
print("Transposed array:\n", transposed_array)
```

**Output:**

```
Transposed array:
 [[1 4]
 [2 5]
 [3 6]]
```

- **transpose()** function array-இன் structure-ஐ மாற்றி row-களை column-களாகவும் column-களை row-களாகவும் மாற்றுகிறது.
- இது data analysis மற்றும் matrix operations-இல் அதிகமாக பயன்படும்.

#### 9.6. numpy.ndarray.T

**T** attribute transpose operation-ஐ எளிதாக செய்ய alternate முறையாக பயன்படுகிறது. இது **transpose()** function-ஐ போன்றே செயல்படும், ஆனால் syntax சிறிது சுருக்கமாக இருக்கும்.

```python
# Transpose operation using T attribute
print("Transposed array using T:\n", reshaped_array.T)
```

**Output:**

```
Transposed array using T:
 [[1 4]
 [2 5]
 [3 6]]
```

- **T** attribute-ஐ பயன்படுத்தி array-இன் transpose-ஐ செய்யலாம், இது code-ஐ சுருக்கமாகவும் வாசிக்க எளிதாகவும் அமைக்கும்.
- **T** attribute transpose-ஐ எளிதாகவும் வேகமாகவும் செயல்படுத்த உதவுகிறது.

#### 9.6. numpy.swapaxes

**swapaxes()** function-ஐ பயன்படுத்தி array-இல் உள்ள axes-ஐ மாற்றி அமைக்க முடியும். இதனால் multi-dimensional array-இல் axes-ஐ மாற்றி data structure-ஐ மாற்றலாம்.

```python
import numpy as np

# Swap axes operation
reshaped_array = np.array([[1, 2, 3], [4, 5, 6]])
swapped_array = reshaped_array.swapaxes(0, 1)
print("Swapped axes array:\n", swapped_array)
```

**Output:**

```
Swapped axes array:
 [[1 4]
 [2 5]
 [3 6]]
```

- **swapaxes()** function-ஐ பயன்படுத்தி, array-இல் 0 மற்றும் 1 axes-ஐ மாற்றியுள்ளோம்.
- இது data-ஐ transpose செய்யும் ஒரு alternate method ஆகும், ஆனால் குறிப்பிட்ட axes-ஐ user-defined இடத்தில் மாற்றிக் கொள்ளலாம்.

#### 9.7. numpy.rollaxis

**rollaxis()** method-ஐ பயன்படுத்தி, multi-dimensional array-இல் உள்ள axes-ஐ ஒரு குறிப்பிட்ட இடத்திற்கு மாற்றி அமைக்க முடியும். இது axes-ஐ flexibly reorder செய்ய உதவுகிறது.

```python
# Roll axes operation
rolled_array = np.rollaxis(swapped_array, 1)
print("Rolled axes array:\n", rolled_array)
```

**Output:**

```
Rolled axes array:
 [[1 2 3]
 [4 5 6]]
```

- **rollaxis()** method axes-ஐ ஒரு குறிப்பிட்ட இடத்திற்கு மாற்றி அமைக்கிறது.

- இங்கு, axis-ஐ 1 இடத்தில் இருந்து 0 இடத்திற்கு மாற்றியுள்ளோம், இதனால் data structure மாற்றப்பட்டது.

  **குறிப்பு**: **swapaxes()** மற்றும் **rollaxis()**: Array-இல் உள்ள axes-ஐ மாற்றி data structure-ஐ reconfigure செய்ய பயன்படுகின்றன.

#### 9.8. numpy.broadcast

**broadcast()** function broadcasting operation எப்படி செயல்படுகிறது என்பதை காட்ட உதவுகிறது. இது shape-ல் பொருந்தாத array values-ஐ, NumPy broadcasting principle-ஐ பயன்படுத்தி இணைக்கும்.

```python
array1 = np.array([1, 2, 3])
array2 = np.array([[1], [2], [3]])
broadcasted = np.broadcast(array1, array2)
for x, y in broadcasted:
    print(f"Broadcasted elements: x = {x}, y = {y}")
```

**Output:**

```
Broadcasted elements: x = 1, y = 1
Broadcasted elements: x = 2, y = 1
Broadcasted elements: x = 3, y = 1
Broadcasted elements: x = 1, y = 2
Broadcasted elements: x = 2, y = 2
Broadcasted elements: x = 3, y = 2
Broadcasted elements: x = 1, y = 3
Broadcasted elements: x = 2, y = 3
Broadcasted elements: x = 3, y = 3
```

- **broadcast()** function-ஐ பயன்படுத்தி shape-ல் வேறுபட்ட arrays-ஐ iterate செய்து, broadcasting operation எவ்வாறு செயல்படுகிறது என்பதை பார்க்க முடிகிறது.

#### 9.9. numpy.broadcast_to

**broadcast_to()** function-ஐ பயன்படுத்தி, ஒரு array-யை ஒரு குறிப்பிட்ட shape-க்கு broadcast செய்யலாம். இது data-ஐ duplicate செய்யாமல், memory-efficient-ஆக operations செய்ய உதவுகிறது.

```python
# Broadcasting array to a new shape
array = np.array([1, 2, 3])
broadcasted_array = np.broadcast_to(array, (3, 3))
print("Broadcasted array:\n", broadcasted_array)
```

**Output:**

```
Broadcasted array:
 [[1 2 3]
 [1 2 3]
 [1 2 3]]
```

- **broadcast_to()** function array-ஐ புதிய shape-க்கு broadcast செய்து, memory-யை duplicate செய்யாமல் arithmetic operations செய்ய முடிகிறது.
- இது array-ஐ வேகமாக மற்றும் memory-efficient-ஆக புதிய structure-க்கு conform செய்ய உதவுகிறது.

**குறிப்பு**: **broadcast()** மற்றும் **broadcast_to()**: Broadcasting principle-ஐ பயன்படுத்தி arrays-இல் operations செய்ய memory-efficient-ஆகவும் computationally fast-ஆகவும் மாற்றுகின்றன.

#### 9.10. numpy.expand_dims

**expand_dims()** function-ஐ பயன்படுத்தி array-இல் ஒரு புதிய axis-ஐ சேர்த்து, அதன் dimensionality-ஐ அதிகரிக்க முடியும். இது array-ஐ reshape செய்து, அதனை higher-dimensional array-ஆக மாற்ற உதவுகிறது.

```python
import numpy as np

# Array dimensionality-ஐ அதிகரித்தல்
array = np.array([1, 2, 3])
expanded_array = np.expand_dims(array, axis=0)
print("Expanded array:\n", expanded_array)
```

**Output:**

```
Expanded array:
 [[1 2 3]]
```

- இங்கு, **expand_dims()** function array-இல் ஒரு புதிய axis-ஐ (dimension) சேர்க்கிறது.
- **axis=0** என்பதை குறிப்பிடுவதன் மூலம், original 1D array `[1, 2, 3]` ஒரு 2D array-ஆக (`[[1, 2, 3]]`) மாற்றப்படுகிறது.
- இது data-ஐ reshape செய்ய, multi-dimensional data handling-ஐ எளிதாக்க உதவுகிறது.

#### 9.12. numpy.squeeze

**squeeze()** function-ஐ பயன்படுத்தி array-இல் உள்ள unwanted singleton dimensions-ஐ (அதாவது length 1 கொண்ட dimensions) அகற்றலாம். இது array-ஐ compact-ஆக மாற்றி அதன் shape-ஐ குறைக்க உதவுகிறது.

```python
# Singleton dimensions-ஐ நீக்குதல்
array = np.array([[[1, 2, 3]]])
squeezed_array = np.squeeze(array)
print("Squeezed array:", squeezed_array)
```

**Output:**

```
Squeezed array: [1 2 3]
```

- **squeeze()** method array-இல் உள்ள unnecessary singleton dimensions-ஐ நீக்குகிறது.
- எங்கள் உதாரணத்தில், 3D array `[ [[1, 2, 3]] ]` ஒரு 1D array `[1, 2, 3]`-ஆக மாற்றப்படுகிறது.
- இது unwanted dimensions-ஐ அகற்றுவதால் memory usage மற்றும் data processing எளிதாகும்.

#### 9.13. numpy.concatenate

**concatenate()** function-ஐ பயன்படுத்தி இரண்டு அல்லது அதற்கும் அதிகமான array-களை ஒரு இணைந்த array-ஆக உருவாக்கலாம். இது arrays-ஐ sequentially இணைத்து, single array-ஆக return செய்கிறது.

```python
# Arrays-ஐ concatenate செய்தல்
array1 = np.array([1, 2, 3])
array2 = np.array([4, 5, 6])
concatenated_array = np.concatenate((array1, array2))
print("Concatenated array:", concatenated_array)
```

**Output:**

```
Concatenated array: [1 2 3 4 5 6]
```

- **concatenate()** function array-களை இணைத்து ஒரு single-dimensional array-ஆக return செய்கிறது.
- உதாரணத்தில், **array1** மற்றும் **array2** இணைக்கப்பட்டு, **[1, 2, 3, 4, 5, 6]** என்ற array-ஆகவும் உருவாக்கப்பட்டது.
- இது data merging மற்றும் continuous sequences-ஐ உருவாக்க உதவுகிறது.

#### 9.14. numpy.stack

**stack()** function-ஐ பயன்படுத்தி arrays-ஐ ஒரு புதிய axis-இல் stack செய்ய முடியும். இது arrays-ஐ vertically அல்லது horizontally stack செய்து, multi-dimensional structure-ஆக மாற்ற உதவுகிறது.

```python
# Arrays-ஐ stack செய்தல்
array1 = np.array([1, 2, 3])
array2 = np.array([4, 5, 6])
stacked_array = np.stack((array1, array2), axis=1)
print("Stacked array:\n", stacked_array)
```

**Output:**

```
Stacked array:
 [[1 4]
 [2 5]
 [3 6]]
```

- **stack()** function arrays-ஐ ஒரு புதிய axis-இல் stack செய்கிறது, இதனால் data-ஐ multi-dimensional format-ஆக மாற்றுகிறது.
- **axis=1** என்ற option-ஐ பயன்படுத்தியதால், **array1** மற்றும் **array2** values horizontal-ஆக stack ஆகின்றன.
- இது data representation-ஐ மாற்றுவதிலும், matrix operations செய்யவும் பயன்படும்.

#### 9.15. numpy.hstack and numpy.vstack

**hstack()** மற்றும் **vstack()** functions-ஐ பயன்படுத்தி arrays-ஐ horizontal மற்றும் vertical-ஆக stack செய்ய முடியும். 

#### Horizontal Stacking with `hstack()`

**hstack()** function-ஐ பயன்படுத்தி, arrays-ஐ horizontal-ஆக (ஒரே row-ல்) stack செய்யலாம். இது arrays-ஐ இருவரையிலும் இணைத்து, ஒரே-dimensional row format-ல் merge செய்கிறது.

```python
import numpy as np

# Arrays to stack
array1 = np.array([1, 2, 3])
array2 = np.array([4, 5, 6])

# Horizontal stacking
hstacked_array = np.hstack((array1, array2))
print("Horizontally stacked array:", hstacked_array)
```

**Output:**

```
Horizontally stacked array: [1 2 3 4 5 6]
```

- **hstack()** function arrays-ஐ ஒரே-dimensional format-ல் horizontally stack செய்கிறது.
- இந்த உதாரணத்தில், **array1** மற்றும் **array2** values ஒன்று சேர்ந்து ஒரே row-ஆக return செய்யப்படுகின்றன.

#### Vertical Stacking with `vstack()`

**vstack()** function-ஐ பயன்படுத்தி, arrays-ஐ vertical-ஆக (ஒரே column-ல்) stack செய்யலாம். இது arrays-ஐ இருவரையிலும் vertically merge செய்து multi-dimensional array ஆக return செய்கிறது.

```python
# Vertical stacking
vstacked_array = np.vstack((array1, array2))
print("Vertically stacked array:\n", vstacked_array)
```

**Output:**

```
Vertically stacked array:
 [[1 2 3]
 [4 5 6]]
```

- **vstack()** function arrays-ஐ vertical-ஆக stack செய்கிறது, அதாவது arrays-ஐ row-wise align செய்து multi-dimensional array ஆக return செய்கிறது.
- இது data handling மற்றும் matrix operations-ஐ சிறப்பாக செய்ய உதவுகிறது.

#### 9.16. numpy.split

**split()** function-ஐ பயன்படுத்தி, ஒரு array-ஐ பல துண்டுகளாக பிரிக்கலாம். இது array-ஐ user-defined number of sub-arrays ஆக களவாக பிரிக்க உதவுகிறது.

```python
# Array-ஐ split செய்தல்
array = np.array([1, 2, 3, 4, 5, 6])
split_array = np.split(array, 3)
print("Split arrays:", split_array)
```

**Output:**

```
Split arrays: [array([1, 2]), array([3, 4]), array([5, 6])]
```

- **split()** function array-ஐ user-defined size-க்கு sub-arrays ஆகப் பிரிக்கிறது.
- இந்த உதாரணத்தில், **array** ஐ மூன்று sub-arrays ஆக பிரிக்கப்பட்டு, ஒவ்வொரு array-க்கும் 2 elements ஆக return செய்கிறது.

#### 9.17. numpy.hsplit and numpy.vsplit

**hsplit()** மற்றும் **vsplit()** functions-ஐ horizontal மற்றும் vertical-ஆக arrays-ஐ பிரிக்க முடியும். 

#### Horizontal Split with `hsplit()`

**hsplit()** function horizontal direction-ல் arrays-ஐ சில பகுதிகளாகப் பிரிக்க பயன்படும்.

```python
# Horizontal split
harray = np.array([[1, 2, 3], [4, 5, 6]])
hsplit_array = np.hsplit(harray, 3)
print("Horizontally split arrays:", hsplit_array)
```

**Output:**

```
Horizontally split arrays: [array([[1],
       [4]]), array([[2],
       [5]]), array([[3],
       [6]])]
```

- **hsplit()** function arrays-ஐ horizontal-ஆக column-wise பிரிக்கிறது.
- இதனால், ஒவ்வொரு column data-ஐ தனித்தனியாக sub-arrays ஆக return செய்கிறது.

#### Vertical Split with `vsplit()`

**vsplit()** function vertical direction-ல் arrays-ஐ சில பகுதிகளாகப் பிரிக்க உதவுகிறது.

```python
# Vertical split
vsplit_array = np.vsplit(harray, 2)
print("Vertically split arrays:", vsplit_array)
```

**Output:**

```
Vertically split arrays: [array([[1, 2, 3]]), array([[4, 5, 6]])]
```

- **vsplit()** function arrays-ஐ vertical-ஆக row-wise பிரிக்க உதவுகிறது.
- இது multi-dimensional arrays-ஐ row-wise sub-arrays ஆக பிரிக்க உதவுகிறது.

#### 9.18. numpy.resize

**resize()** function array-ஐ ஒரு புதிய shape-க்கு மாற்றி அமைக்க உதவுகிறது. இது array-ஐ நினைவில் (memory) நிரப்பியபடி அல்லது பின்னர் அளவுடன் conform செய்து மாற்றிக்கொள்ள முடியும்.

```python
# Array-ஐ resize செய்தல்
array = np.array([1, 2, 3, 4])
resized_array = np.resize(array, (2, 3))
print("Resized array:\n", resized_array)
```

**Output:**

```
Resized array:
 [[1 2 3]
 [4 1 2]]
```

- **resize()** function array-ஐ ஒரு புதிய shape-க்கு conform செய்து மாற்றுகிறது.
- இதன் output, புதிய shape conform ஆக elements இல்லை என்றால், original தரவுகளை மீண்டும் மீண்டும் நிரப்பும்.

இந்த methods எல்லாம் NumPy array-களை விரிவாக manipulate செய்து, memory-efficient-ஆக data handling மற்றும் reshaping செய்ய உதவுகின்றன.

#### 9.19. numpy.append

**append()** function-ஐ பயன்படுத்தி, existing array-இன் முடிவில் values-ஐ சேர்க்க முடியும். இது original array-ஐ மாற்றாது; இதற்கு பதிலாக, புதிய array-ஐ return செய்யும், அதில் original values மற்றும் புதிய values இணைக்கப்படும்.

```python
import numpy as np

# Array-இல் values-ஐ append செய்தல்
array = np.array([1, 2, 3])
appended_array = np.append(array, [4, 5, 6])
print("Appended array:", appended_array)
```

**Output:**

```
Appended array: [1 2 3 4 5 6]
```

- **append()** function-ஐ பயன்படுத்தி **array**-இன் முடிவில் **[4, 5, 6]** values-ஐ சேர்த்துள்ளோம்.

- இது original array-ஐ மாற்றாது, புதிய array-ஐ return செய்கிறது.

- இது frequently array-இல் new data add செய்யும்போது மிகவும் பயனுள்ளதாக இருக்கும்.


#### 9.20. numpy.insert

**insert()** function-ஐ பயன்படுத்தி, array-இல் ஒரு குறிப்பிட்ட இடத்தில் values-ஐ insert செய்ய முடியும். இந்த method-ல், நீங்கள் எந்த இடத்தில் values-ஐ சேர்க்க வேண்டும் என்பதையும், எந்த values-ஐ சேர்க்க வேண்டும் என்பதையும் குறிப்பிடலாம்.

```python
# Array-இல் values-ஐ insert செய்தல்
array = np.array([1, 2, 3])
inserted_array = np.insert(array, 1, [7, 8])
print("Inserted array:", inserted_array)
```

**Output:**

```
Inserted array: [1 7 8 2 3]
```

- **insert()** function-ஐ பயன்படுத்தி, **array**-இன் இடத்தில் (index 1) **[7, 8]** values-ஐ insert செய்துள்ளோம்.

- இது original array-ஐ மாற்றாமல், புதிய array-ஐ return செய்கிறது.

- இந்த method-ஐ பயன்படுத்தி array-இல் values-ஐ middle-ல் அல்லது specific positions-ல் add செய்ய முடியும்.

  **குறிப்பு**: எந்த இடத்தில் values சேர்க்க வேண்டும் என்பதையும், அந்த values-ஐ குறிப்பிட்ட இடத்தில் insert செய்வதை நிர்ணயிக்கலாம்.

#### 9.21. numpy.delete

**delete()** function-ஐ பயன்படுத்தி, array-இல் unwanted values-ஐ அல்லது indices-ஐ அகற்றலாம். இது original array-ஐ modify செய்யாது; இது unwanted values-ஐ அகற்றி, புதிய array-ஐ return செய்கிறது.

```python
# Array-இல் values-ஐ delete செய்தல்
array = np.array([1, 2, 3, 4, 5])
deleted_array = np.delete(array, [1, 3])
print("Deleted array:", deleted_array)
```

**Output:**

```
Deleted array: [1 3 5]
```

- **delete()** function-ஐ பயன்படுத்தி, **array**-இல் index 1 மற்றும் 3 (values **2** மற்றும் **4**) அகற்றப்பட்டுள்ளன.

- இதன் மூலம் unwanted values-ஐ array-இல் இருந்து remove செய்து, clean data-ஐ பெறலாம்.

  **குறிப்பு**: Original array-ஐ மாற்றாது, புதிய array-ஐ return செய்து unwanted data-ஐ clean செய்கிறது.

#### 9.22. numpy.unique

**unique()** function-ஐ பயன்படுத்தி, array-இல் உள்ள repeating elements-ஐ அகற்றி, unique values-ஐ மட்டும் return செய்யலாம். இது data analysis மற்றும் data cleaning செயல்பாடுகளில் மிகவும் பயனுள்ளது.

```python
# Array-இல் unique values-ஐ பெறுதல்
array = np.array([1, 2, 2, 3, 4, 4, 5])
unique_values = np.unique(array)
print("Unique values:", unique_values)
```

**Output:**

```
Unique values: [1 2 3 4 5]
```

- **unique()** function-ஐ பயன்படுத்தி, **array**-இல் repeating values-ஐ அகற்றி, unique values மட்டும் return செய்யப்படுகிறது.
- இது data-இல் redundancy-ஐ அகற்றி, data-ஐ compact-ஆகவும் organized-ஆகவும் மாற்றுகிறது.

**குறிப்பு**: Data analysis மற்றும் data cleaning செயல்பாடுகளில் redundancy-ஐ அகற்றுகிறது.

<div style="page-break-after: always;"></div>

### 10. NUMPY – BINARY OPERATORS

NumPy-யில் **binary operators** பயன்படுத்தி bitwise operations செய்யலாம். Bitwise operations binary (இரும) data-களில் வேலை செய்யும், அதாவது bit-அளவிலான data-ஐ நேரடியாக மாற்றும். இவை data manipulation மற்றும் bit-level operations-ஐ எளிதாக்கும்.

#### 10.1. numpy.bitwise_and

**bitwise_and** operator இரண்டு arrays-இன் bitwise AND operation-ஐ return செய்கிறது. இது ஒவ்வொரு bit-இல் உள்ள values-ஐ எடுத்து AND operation செய்கிறது, அதாவது, இரண்டு bit-களும் 1 என்றால் மட்டுமே முடிவு 1 ஆக இருக்கும்.

```python
import numpy as np

# Bitwise AND operation
a = np.array([0b1100])
b = np.array([0b1010])
result = np.bitwise_and(a, b)
print("Bitwise AND:", result)
```

**Output:**

```
Bitwise AND: [8]
```

- **a** = 0b1100 (binary) = 12 (decimal)
- **b** = 0b1010 (binary) = 10 (decimal)
- Bitwise AND operation (1100 AND 1010) = 1000 (binary) = 8 (decimal)

**bitwise_and** operation AND logic பயன்படுத்தி இரண்டு arrays-இன் corresponding bit-களை compare செய்து, முடிவுகளை return செய்கிறது.

#### 10.2. numpy.bitwise_or

**bitwise_or** operator இரண்டு arrays-இன் bitwise OR operation-ஐ return செய்கிறது. இது OR operation-ஐ ஒவ்வொரு bit-ஐ வைத்து செய்கிறது, அதாவது, bit-களில் எதாவது ஒரு value 1 என்றால், முடிவாக 1 return ஆகும்.

```python
# Bitwise OR operation
a = np.array([0b1100])
b = np.array([0b1010])
result = np.bitwise_or(a, b)
print("Bitwise OR:", result)
```

**Output:**

```
Bitwise OR: [14]
```

- **a** = 0b1100 (binary) = 12 (decimal)
- **b** = 0b1010 (binary) = 10 (decimal)
- Bitwise OR operation (1100 OR 1010) = 1110 (binary) = 14 (decimal)

**bitwise_or** operation OR logic-ஐ பயன்படுத்தி bit-level-ல் values-ஐ compare செய்து, final result-ஐ return செய்கிறது.

#### 10.3. numpy.invert()

**invert()** function-ஐ பயன்படுத்தி array-இல் உள்ள ஒவ்வொரு bit-ஐ எதிர்மறையாக மாற்றலாம். இதன் பொருள், bit 1 இருந்தால் 0 ஆகவும், 0 இருந்தால் 1 ஆகவும் மாற்றம் செய்யும்.

```python
# Bitwise NOT operation
a = np.array([0b1100], dtype=np.uint8)
result = np.invert(a)
print("Bitwise NOT:", result)
```

**Output:**

```
Bitwise NOT: [243]
```

- **a** = 0b1100 (binary) = 12 (decimal)
- **invert()** operation bit-களில் inversion செய்கிறது, அதாவது 1100 becomes 11110011 (for an 8-bit integer) = 243 (decimal).

**invert()** operation bit-level inversion-ஐ எளிதாக செய்து, data-ஐ logically toggle செய்ய உதவுகிறது.

#### 10.4. numpy.left_shift

**left_shift** operator-ஐ பயன்படுத்தி array-இன் bits-ஐ இடது பக்கம் (left side) நகர்த்தலாம். இது bit values-ஐ shift செய்து, அதற்கு வலது பக்கம் புதிய 0s சேர்க்கும்.

```python
# Left shift operation
a = np.array([0b0010])
result = np.left_shift(a, 2)
print("Left Shift:", result)
```

**Output:**

```
Left Shift: [8]
```

- **a** = 0b0010 (binary) = 2 (decimal)
- Left shift operation shifts the bits 2 positions to the left: 0010 becomes 1000 (binary) = 8 (decimal).

**left_shift** operation bit-level-ல் values-ஐ இடது பக்கம் நகர்த்தி, binary representation-ஐ மாற்ற உதவுகிறது.

#### 10.5. numpy.right_shift

**right_shift** operator-ஐ பயன்படுத்தி array-இன் bits-ஐ வலது பக்கம் (right side) நகர்த்தலாம். இது bit values-ஐ shift செய்து, அதற்கு இடது பக்கம் 0s சேர்க்கும்.

```python
# Right shift operation
a = np.array([0b1000])
result = np.right_shift(a, 2)
print("Right Shift:", result)
```

**Output:**

```
Right Shift: [2]
```

- **a** = 0b1000 (binary) = 8 (decimal)
- Right shift operation shifts the bits 2 positions to the right: 1000 becomes 0010 (binary) = 2 (decimal).

**right_shift** operation bit-level-ல் values-ஐ வலது பக்கம் நகர்த்தி, binary data-ஐ சுருக்க உதவுகிறது.

இந்த binary operators data-ஐ bit-level-ல் manipulate செய்யவும், binary data handling ஐ memory-efficient-ஆகவும் செய்ய உதவுகின்றன.

<div style="page-break-after: always;"></div>

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

<div style="page-break-after: always;"></div>

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

<div style="page-break-after: always;"></div>

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

<div style="page-break-after: always;"></div>

<div style="page-break-after: always;"></div>

### 14. NUMPY − STATISTICAL FUNCTIONS

NumPy-யில் பல **statistical functions** உள்ளன, இது data-யை எளிதாக புள்ளிவிவரமாக பரிசோதிக்க உதவுகிறது. இந்த statistical functions data analysis மற்றும் decision-making செயல்பாடுகளை துல்லியமாகவும் memory-efficient-ஆகவும் செய்ய உதவுகின்றன.

#### 14.1. numpy.amin() and numpy.amax()

**amin()** மற்றும் **amax()** functions-ஐ பயன்படுத்தி array-இல் உள்ள குறைந்த மற்றும் அதிகமான values-ஐ கண்டறியலாம். இது data-யின் minimum மற்றும் maximum values-ஐ எளிதாக return செய்கிறது.

```python
import numpy as np

# Finding min and max values
array = np.array([10, 20, 30, 40, 50])
min_value = np.amin(array)
max_value = np.amax(array)
print("Minimum value:", min_value)
print("Maximum value:", max_value)
```

**Output:**

```
Minimum value: 10
Maximum value: 50
```

- **np.amin()** function array-இல் உள்ள குறைந்த value-ஐ return செய்கிறது.
- **np.amax()** function array-இல் உள்ள அதிகமான value-ஐ return செய்கிறது.
- இந்த functions data-யின் extreme values-ஐ கண்டறிய data validation மற்றும் data quality analysis-க்கு பயனுள்ளது.

#### 14.2. numpy.ptp()

**ptp()** function-ஐ பயன்படுத்தி array-இன் maximum மற்றும் minimum values-இன் range-ஐ காணலாம். இது peak-to-peak range-ஐ எளிதாக return செய்கிறது.

```python
# Range of values using ptp()
range_value = np.ptp(array)
print("Range (ptp):", range_value)
```

**Output:**

```
Range (ptp): 40
```

- **ptp()** function array-இல் உள்ள maximum value மற்றும் minimum value இடையிலான difference-ஐ return செய்கிறது.
- இந்த range values data-யின் spread-ஐ அளவிடும் metric ஆகும், இது data variability-ஐ அறிய உதவும்.

#### 14.3. numpy.percentile()

**percentile()** function-ஐ array-இல் உள்ள values-இன் percentile-ஐ கண்டறிய பயன்படுத்தலாம். Percentile என்பது data-இல் உள்ள values-ஐ ஒரு குறிப்பிட்ட அளவிற்கு மேல் அல்லது கீழ் உள்ளவர்களாகப் பகுக்க உதவும்.

```python
# Percentile calculation
percentile_value = np.percentile(array, 50)
print("50th Percentile:", percentile_value)
```

**Output:**

```
50th Percentile: 30.0
```

- **np.percentile()** function array-இல் உள்ள values-இன் குறிப்பிட்ட percentile-ஐ return செய்கிறது.
- 50th percentile என்பது median value ஆகும், இது data distribution-ஐ அறிய மிகவும் முக்கியமானது.
- Percentile calculations data-யின் distribution-ஐ அறிந்து data analysis-ல் useful insights அளிக்கிறது.

#### 14.4. numpy.median()

**median()** function array-இல் values-ஐ arrange செய்த பிறகு, அதில் உள்ள center value-ஐ return செய்கிறது. Median என்பது values-ஐ ascending order-ல் வரிசைப்படுத்திய பிறகு உள்ள நடுநிலையான value ஆகும்.

```python
import numpy as np

# Median calculation
array = np.array([10, 20, 30, 40, 50])
median_value = np.median(array)
print("Median value:", median_value)
```

**Output:**

```
Median value: 30.0
```

- **median()** function array-இல் உள்ள values-ஐ arrange செய்து, center value-ஐ return செய்கிறது.
- Median calculation data-இன் central tendency-ஐ அளவிட மிகவும் பயனுள்ளது, ஏனெனில் இது extreme values-ஐ (outliers) ignore செய்கிறது.

#### 14.5. numpy.mean()

**mean()** function array-இல் values-இன் arithmetic mean (average) value-ஐ return செய்கிறது. Mean என்பது data-இல் உள்ள values-ஐ sum செய்து, அந்த sum-ஐ values-இன் எண்ணிக்கையால் பகுத்தல்.

```python
# Mean calculation
mean_value = np.mean(array)
print("Mean value:", mean_value)
```

**Output:**

```
Mean value: 30.0
```

- **mean()** function array-இல் values-ஐ average-ஆக return செய்கிறது.
- Mean calculation data distribution-ஐ அறிய முக்கியமானது, இது values-ஐ central tendency-ல் புரிந்து கொள்ள உதவுகிறது.

#### 14.6. numpy.average()

**average()** function array-இல் values-ஐ weighted average-ஆக return செய்கிறது. Weighted average-ல் values-க்கு கொடுக்கப்படும் importance (weight) அடிப்படையில் calculations செய்யப்படுகிறது.

```python
# Weighted average calculation
weights = np.array([1, 2, 3, 4, 5])
weighted_average = np.average(array, weights=weights)
print("Weighted average:", weighted_average)
```

**Output:**

```
Weighted average: 40.0
```

- **average()** function values-இல் weights கொடுத்த பிறகு weighted average-ஐ return செய்கிறது.
- Weighted average data importance-ஐ அடிப்படையாக கொண்டு average value-ஐ return செய்யும், இது decision-making process-ல் மிக முக்கியம்.

#### 14.7. Standard Deviation

**std()** function array-இல் values-ஐ standard deviation-ஆக return செய்கிறது. Standard deviation என்பது values-ஐ mean-இன் சுற்றிலும் எவ்வளவு scatter ஆக இருக்கின்றன என்பதை அளவிடும்.

```python
# Standard deviation calculation
std_value = np.std(array)
print("Standard Deviation:", std_value)
```

**Output:**

```
Standard Deviation: 14.142135623730951
```

- **std()** function array-இல் values-ஐ standard deviation-ஆக return செய்கிறது.
- Standard deviation values-ஐ mean-இன் சுற்றிலும் எவ்வளவு வித்தியாசமாக உள்ளன என்பதை காட்டும், இது data variability-ஐ அறிய உதவுகிறது.

#### 14.8. Variance

**var()** function array-இல் values-ஐ variance-ஆக return செய்கிறது. Variance என்பது values-ஐ mean-இன் சுற்றிலும் deviation-ஐ square செய்து return செய்கிறது.

```python
# Variance calculation
variance_value = np.var(array)
print("Variance:", variance_value)
```

**Output:**

```
Variance: 200.0
```

- **var()** function array-இல் values-ஐ variance-ஆக return செய்கிறது.
- Variance values-ஐ mean-இன் சுற்று deviation-ஐ square செய்து அளவிடும், இது data spread-ஐ மேம்பட அறிய உதவும்.

இந்த statistical functions data analysis மற்றும் data interpretation-ல் முக்கிய பங்காற்றுகின்றன, மேலும் decision-making செயல்பாடுகளை துல்லியமாகவும் memory-efficient-ஆகவும் செய்ய உதவுகின்றன.

<div style="page-break-after: always;"></div>

### 15. NUMPY − SORT, SEARCH & COUNTING FUNCTIONS

NumPy-யில் **sort, search மற்றும் counting** functions-ஐ பயன்படுத்தி array-களின் values-ஐ வரிசைப்படுத்தவும், தேடவும் மற்றும் எண்ணிக்கையிடவும் முடியும். இவை data analysis மற்றும் data manipulation-ஐ எளிமையாக்க உதவுகின்றன.

#### 15.1. numpy.sort()

**sort()** function-ஐ பயன்படுத்தி array-இல் values-ஐ ascending order-ல் வரிசைப்படுத்தலாம். இது data-ஐ reorganize செய்ய memory-efficient-ஆகவும் computationally fast-ஆகவும் செய்கிறது.

```python
import numpy as np

# Array sort operation
array = np.array([5, 2, 8, 1, 9])
sorted_array = np.sort(array)
print("Sorted array:", sorted_array)
```

**Output:**

```
Sorted array: [1 2 5 8 9]
```

- **np.sort()** function array-இல் values-ஐ ascending order-ல் வரிசைப்படுத்துகிறது.
- இது data-ஐ orderly format-ஆக மாற்றி, analysis-க்கு எளிதாகிறது.

#### 15.2. numpy.argsort()

**argsort()** function-ஐ பயன்படுத்தி, array-இல் values-ஐ வரிசைப்படுத்த indices-ஐ return செய்கிறது. இது values-ஐ original order-ல் எவ்வாறு வரிசைப்படுத்த வேண்டுமென காட்டும்.

```python
# Argsort operation
indices = np.argsort(array)
print("Indices of sorted array:", indices)
```

**Output:**

```
Indices of sorted array: [3 1 0 2 4]
```

- **np.argsort()** function-ஐ பயன்படுத்தி sorted order-ல் values எங்கே இருக்கின்றன என்பதன் indices-ஐ return செய்கிறது.
- இது data-ஐ arrange செய்யாதே, values-ஐ reference அடிப்படையில் access செய்ய உதவுகிறது.

#### 15.3. numpy.lexsort()

**lexsort()** function ஒரு அல்லது அதற்கும் அதிகமான keys-ஐ அடிப்படையாக வைத்து data-ஐ வரிசைப்படுத்தும். இது multi-dimensional data-ஐ இரண்டு அல்லது அதற்கு மேற்பட்ட criteria அடிப்படையில் organize செய்ய உதவுகிறது.

```python
# Lexsort operation
names = ['banana', 'apple', 'cherry']
prices = [40, 10, 30]
sorted_indices = np.lexsort((prices, names))
print("Sorted indices based on names and prices:", sorted_indices)
```

**Output:**

```
Sorted indices based on names and prices: [1 2 0]
```

- **np.lexsort()** function-ஐ இரண்டு keys (names, prices) அடிப்படையில் data-ஐ arrange செய்ய பயன்படுத்தியுள்ளோம்.
- இது data-ஐ multi-level sorting-ஆக reorder செய்ய உதவுகிறது, இதன் மூலம் complex data-ஐ organize செய்யலாம்.

#### 15.4. numpy.argmax() and numpy.argmin()

**argmax()** மற்றும் **argmin()** functions array-இல் உள்ள மிகப் பெரிய மற்றும் சிறிய values-இருக்கும் indices-ஐ return செய்கின்றன. இது array-இல் உள்ள extreme values-ஐ எளிதாக கண்டறிய உதவுகிறது.

```python
# Argmax and Argmin operations
max_index = np.argmax(array)
min_index = np.argmin(array)
print("Index of maximum value:", max_index)
print("Index of minimum value:", min_index)
```

**Output:**

```
Index of maximum value: 4
Index of minimum value: 3
```

- **np.argmax()** function array-இல் உள்ள maximum value-ஐ கொண்ட index-ஐ return செய்கிறது.
- **np.argmin()** function minimum value-ஐ கொண்ட index-ஐ return செய்கிறது.
- இது data-ஐ identify செய்து, peak values-ஐ track செய்ய உதவுகிறது.

#### 15.5. numpy.nonzero()

**nonzero()** function array-இல் 0 அல்லாத values-இருக்கும் இடங்களை return செய்கிறது. இது sparse data-ஐ handle செய்யும் போது மிகவும் பயனுள்ளது.

```python
# Non-zero indices
nonzero_indices = np.nonzero(array)
print("Indices of non-zero elements:", nonzero_indices)
```

**Output:**

```
Indices of non-zero elements: (array([0, 1, 2, 3, 4]),)
```

- **np.nonzero()** function array-இல் 0 values இல்லாத இடங்களை return செய்கிறது.
- இது data-ஐ filter செய்து, sparse data structures-ஐ அறிய memory-efficient-ஆகப் பயன்படுத்தப்படுகிறது.

#### 15.6. numpy.where()

**where()** function ஒரு condition அடிப்படையில் array-இல் values-இருக்கும் இடங்களை return செய்கிறது. இது conditional logic-ஐ பயன்படுத்தி data-ஐ filter செய்ய உதவுகிறது.

```python
# Where operation
condition_indices = np.where(array > 4)
print("Indices where values > 4:", condition_indices)
```

**Output:**

```
Indices where values > 4: (array([0, 2, 4]),)
```

- **np.where()** function-ஐ condition (values > 4) அடிப்படையில் values-இருக்கும் இடங்களை return செய்கிறது.
- இது boolean indexing-ஐ பயன்படுத்தி data-ஐ filter செய்ய எளிதாக்குகிறது.

#### 15.7. numpy.extract()

**extract()** function-ஐ condition அடிப்படையில் array-இல் values-ஐ return செய்ய பயன்படுத்தலாம். இது data-இல் குறிப்பிட்ட condition satisfy செய்யும் values-ஐ எளிதாக பெற உதவுகிறது.

```python
# Extract operation
extracted_values = np.extract(array > 4, array)
print("Extracted values greater than 4:", extracted_values)
```

**Output:**

```
Extracted values greater than 4: [5 8 9]
```

- **np.extract()** function array values-இல் condition satisfy செய்யும் values-ஐ return செய்கிறது.
- இது data analysis மற்றும் decision-making-ல் memory-efficient filtering operation ஆகிறது.

இந்த functions data sorting, searching மற்றும் filtering operations-ஐ memory-efficient-ஆகவும் computationally fast-ஆகவும் செய்கின்றன, மேலும் data analysis மற்றும் data handling-ஐ எளிதாக்குகின்றன.

<div style="page-break-after: always;"></div>

### 16. NUMPY − BYTE SWAPPING

NumPy-யில் **byteswap()** function-ஐ பயன்படுத்தி array-இல் உள்ள values-ஐ byte-order மாற்றம் செய்ய முடியும். Byte swapping என்பது data representation-ஐ big-endian மற்றும் little-endian format-களுக்கு இடையே மாற்றுவது ஆகும். இது cross-platform data compatibility மற்றும் binary data handling-க்கு உதவுகிறது.

#### Byte-order: Big-endian vs Little-endian

- **Big-endian**: Data-யின் முக்கியமான byte (most significant byte) memory-யில் முதலில் சேமிக்கப்படும்.
- **Little-endian**: Data-யின் முக்கியமல்லாத byte (least significant byte) memory-யில் முதலில் சேமிக்கப்படும்.

Byte-order format என்பது data-ஐ எவ்வாறு memory-யில் represent செய்ய வேண்டும் என்பதைக் குறிப்பிடுகிறது, இது different computer architectures-ல் வேறுபடும்.

```python
import numpy as np

# Byte swapping operation
array = np.array([1, 256, 8755], dtype=np.int16)
swapped_array = array.byteswap()
print("Original array:", array)
print("Byte swapped array:", swapped_array)
```

**Output:**

```
Original array: [   1  256 8755]
Byte swapped array: [  256     1 38530]
```

- **Original array**: [1, 256, 8755] என்ற values-ஐ **little-endian** format-ல் represent செய்யப்பட்டுள்ளது.
- **byteswap()** function-ஐ பயன்படுத்திய பிறகு, **byte-order** மாற்றப்பட்டு values-ஐ **big-endian** format-ல் represent செய்கிறது.
- **Swapped array**: [256, 1, 38530] என values-ஐ மாற்றியுள்ளோம், இது byte-level representation-ஐ மாற்றியது.

#### எப்போது Byte Swapping பயன்படுத்த வேண்டும்?

1. **Cross-platform Compatibility**: Different systems-ல் data-ஐ transfer செய்யும்போது byte-order மாற்றம் தேவையானது. 
2. **Binary Data Handling**: Low-level data processing மற்றும் file I/O operations-ல் byte-order conversion மிகவும் முக்கியம்.
3. **Networking Protocols**: Data-ஐ network-ல் different architectures-க்கு அனுப்பும்போது byte-order conversion தேவைப்படும்.

#### Additional Details about Byte Swapping

- **dtype Selection**: **byteswap()** operation-ஐ பயன்படுத்தும்போது, array-இன் data type (like np.int16, np.int32) மிகவும் முக்கியமானது, ஏனெனில் byte-order conversion அதில் இருக்கும் byte count-ஐ அடிப்படையாகக் கொண்டது.
- **In-place Operation**: **byteswap()** function array-ஐ original array-யை மாற்றாமல், புதிய array-ஐ return செய்கிறது. இதனால் original data intact ஆக இருக்கும்.

### Byte-order Representation:

- **Little-endian**: Data-யின் முக்கியமல்லாத byte முதலில் வரும். உதாரணமாக, 256 என்ற integer value **little-endian**-ல் `0x0100` ஆக represent செய்யப்படும்.
- **Big-endian**: Data-யின் முக்கியமான byte முதலில் வரும். அதே 256 value **big-endian**-ல் `0x0001` ஆக represent செய்யப்படும்.

### Byte Swapping's Importance in Data Processing

- **Data Interoperability**: Systems-ல் data-ஐ endian-specific format-ல் represent செய்ய வேண்டும். 
- **Performance Optimization**: Different architectures-ல் memory access operations-byte-order alignment எவ்வாறு செய்யப்படுகிறது என்பதைக் குறிக்கிறது.
- **Data Integrity**: Byte swapping operations-இல் data corruption இல்லாமல் transfer-ஐ உறுதி செய்கிறது.

இந்த **byteswap()** operation data interoperability மற்றும் endianess conversion-ஐ எளிமையாக memory-efficient-ஆகவும் நுட்பமாகவும் செயல்படுத்த உதவுகிறது.

<div style="page-break-after: always;"></div>

### 17. NUMPY − COPIES & VIEWS

NumPy-யில் data-ஐ manage செய்வதற்கான மூன்று முக்கியமான concepts உள்ளன: **No Copy, View அல்லது Shallow Copy, Deep Copy**. இவை memory-யை எவ்வாறு handle செய்ய வேண்டும், data-ஐ duplicate செய்ய வேண்டுமா என்பதனை புரிந்து கொள்ள உதவுகின்றன.

#### 17.1. No Copy

ஒரு array-ஐ மற்றொரு variable-க்கு assign செய்தால், அது original data-ஐ reference செய்து கொண்டிருக்கும். இதற்கு copy உருவாகாது. இதன் பொருள், original array மற்றும் new variable ஒன்று data-ஐ share செய்கின்றன.

```python
import numpy as np

# No copy operation
array = np.array([1, 2, 3])
no_copy_array = array
no_copy_array[0] = 10
print("Original array after modification:", array)
print("No Copy array:", no_copy_array)
```

**Output:**

```
Original array after modification: [10  2  3]
No Copy array: [10  2  3]
```

- **No Copy**-இல், original array-ஐ new variable-க்கு assign செய்தால், அது original data-ஐ reference செய்கிறது.
- **no_copy_array**-இல் மாற்றம் செய்யும் போது, **array**-யிலும் அதே மாற்றம் நிகழ்கிறது, ஏனெனில் இவை இரண்டுமே ஒரே memory location-ஐ reference செய்கின்றன.

#### 17.2. View or Shallow Copy

**view()** method-ஐ பயன்படுத்தி ஒரு shallow copy உருவாக்கலாம். Shallow copy என்பது data-இல் உள்ள changes-ஐ reflect செய்யும், ஆனால் data structure மாற்றும்போது மாற்றம் இல்லாது இருக்கும்.

```python
# Shallow copy operation
view_array = array.view()
view_array[1] = 20
print("Original array after view modification:", array)
print("View array:", view_array)
```

**Output:**

```
Original array after view modification: [10  2  3]
View array: [10 20  3]
```

- **Shallow Copy**-இல், **view_array**-ஐ modify செய்தாலும், original array-யில் எந்த மாற்றமும் இல்லை, ஏனெனில் shallow copy data structure-ஐ share செய்கிறது.
- இதற்காக memory usage குறைவாக இருக்கும், ஆனால் data values-ஐ மட்டுமே modify செய்யலாம்.

#### 17.3. Deep Copy

**copy()** method-ஐ பயன்படுத்தி ஒரு deep copy உருவாக்கலாம். Deep copy data-ஐ முழுமையாக independent-ஆக duplicate செய்கிறது. இதனால், original data-ஐ மாற்றினாலும், copy-ஐ எந்த விதமான பாதிப்பும் இருக்காது.

```python
# Deep copy operation
deep_copy_array = array.copy()
deep_copy_array[2] = 30
print("Original array after deep copy modification:", array)
print("Deep copy array:", deep_copy_array)
```

**Output:**

```
Original array after deep copy modification: [10  2  3]
Deep copy array: [10  2 30]
```

- **Deep Copy**-இல், **deep_copy_array** என்பது original data-ஐ முற்றிலும் duplicate செய்தது, எனவே copy-ஐ modify செய்தாலும், original array-யில் எந்த மாற்றமும் இல்லை.
- இது data integrity மற்றும் data isolation-ஐ உறுதிப்படுத்தும் போது மிகவும் பயனுள்ளதாக இருக்கும்.

### எப்போது எந்த Copy-ஐ பயன்படுத்த வேண்டும்?

1. **No Copy**: Data-ஐ share செய்ய வேண்டுமானால், memory efficient-ஆக இருக்கும்.
2. **Shallow Copy**: Data structure-ஐ பயன்படுத்தும்போது memory usage குறைவாக வேண்டுமானால்.
3. **Deep Copy**: Data-ஐ completely duplicate செய்து, isolated environment-ல் manipulate செய்யவேண்டும் என்றால்.

NumPy-யின் **copies & views** methods data manipulation-ஐ எளிதாக்கி, memory-யை திறமையாக handle செய்ய உதவுகின்றன.

<div style="page-break-after: always;"></div>

### 18. NUMPY − MATRIX LIBRARY

NumPy-யில் உள்ள **matrix library** என்பது matrix-களை உருவாக்கவும், நிர்வகிக்கவும் உதவும் functions-களை கொண்டுள்ளது. NumPy.matlib functions-ஐ பயன்படுத்தி, நீங்கள் matrix operations-ஐ memory-efficient-ஆகவும் computationally fast-ஆகவும் செயல்படுத்த முடியும். இது scientific computing மற்றும் linear algebra operations-ஐ எளிமையாக செய்கிறது.

#### 18.1. matlib.empty()

**matlib.empty()** function-ஐ பயன்படுத்தி, uninitialized values கொண்ட ஒரு matrix-ஐ உருவாக்கலாம். Uninitialized matrix என்பது memory-யில் உள்ள பயனற்ற values-ஐ பயன்படுத்தி matrix-ஐ உருவாக்கும், இதனால் memory allocation மிக வேகமாக இருக்கும்.

```python
import numpy.matlib as matlib

# Empty matrix உருவாக்கல்
empty_matrix = matlib.empty((2, 3))
print("Empty matrix:\n", empty_matrix)
```

**Output:**

```
Empty matrix:
 [[4.66651921e-310 0.00000000e+000 2.05833592e-312]
 [6.79038654e-313 2.14321575e-312 2.27053550e-312]]
```

- **matlib.empty()** function-ஐ பயன்படுத்தி, 2 rows மற்றும் 3 columns கொண்ட uninitialized matrix-ஐ உருவாக்கியுள்ளோம்.
- Uninitialized matrix values என்பது random memory values ஆகும், ஏனெனில் values-ஐ initialize செய்யாமல் memory-யில் allocate செய்யப்படுகிறது.
- இந்த method-ஐ data initialization தேவையில்லாத computation-ல், மிக வேகமாக memory-யை allocate செய்ய பயன்படுத்தலாம்.

#### எப்போது **matlib.empty()** பயன்படுத்த வேண்டும்?

- **Performance Optimization**: Memory-யை வேகமாக allocate செய்ய வேண்டிய இடத்தில், ஆனால் values-ஐ பின்னர் initialize செய்யும் data structures-ல்.
- **Data Allocation**: Data-ஐ அடிப்படையாக பயன்படுத்தாமல் placeholder ஆக memory-யில் data structure உருவாக்கும்போது.

#### 18.2. numpy.matlib.zeros()

**matlib.zeros()** function-ஐ பயன்படுத்தி, எல்லா elements-னும் zeros ஆக உள்ள ஒரு matrix-ஐ உருவாக்கலாம். இது scientific calculations மற்றும் numerical computations-ஐ நேரடியாக initialize செய்ய உதவும், ஏனெனில் zeros கொண்ட matrix-கள் இடம் பிடிக்கும் computation-ஐ எளிமையாக மாற்றுகின்றன.

```python
# Zeros matrix உருவாக்கல்
zeros_matrix = matlib.zeros((3, 3))
print("Zeros matrix:\n", zeros_matrix)
```

**Output:**

```
Zeros matrix:
 [[0. 0. 0.]
 [0. 0. 0.]
 [0. 0. 0.]]
```

- **matlib.zeros()** function-ஐ பயன்படுத்தி 3 rows மற்றும் 3 columns கொண்ட matrix-ஐ உருவாக்கியுள்ளோம், இதில் எல்லா values-ஐயும் zero-ஆக initialize செய்துள்ளோம்.
- Zeros matrix scientific computing-ல் உள்ள data structures-ஐ initialize செய்ய உதவுகிறது, ஏனெனில் calculations-ல் zero values கொண்ட matrix-கள் computation-ஐ தொடங்குவதற்கு ஆரம்ப கட்டமாக பயன்படுத்தப்படுகின்றன.

#### எப்போது **matlib.zeros()** பயன்படுத்த வேண்டும்?

- **Default Initialization**: Numerical operations-ஐ ஆரம்ப கட்டமாக zeros matrix-கள் கொண்ட data structure-ஐ பயன்படுத்தும்போது.
- **Matrix Operations**: Linear algebra மற்றும் matrix multiplication போன்ற கணக்கீடுகளுக்கு ஆரம்ப கட்டத்தில் null values ஆக இருக்கும் data-ஐ initialize செய்ய வேண்டும்.

#### 18.3. numpy.matlib.ones()

**matlib.ones()** function-ஐ பயன்படுத்தி, எல்லா elements-னும் ones ஆக உள்ள ஒரு matrix-ஐ உருவாக்கலாம். இது matrix-ஐ முழுமையாக ones values-ஆக initialize செய்வதற்காக memory-efficient-ஆக செயல்படுகிறது.

```python
import numpy.matlib as matlib

# Ones matrix உருவாக்கல்
ones_matrix = matlib.ones((2, 4))
print("Ones matrix:\n", ones_matrix)
```

**Output:**

```
Ones matrix:
 [[1. 1. 1. 1.]
 [1. 1. 1. 1.]]
```

- **matlib.ones()** function-ஐ பயன்படுத்தி 2 rows மற்றும் 4 columns கொண்ட matrix-ஐ உருவாக்கியுள்ளோம், இதில் எல்லா values-னும் ones ஆக இருக்கும்.
- இது scientific calculations மற்றும் linear algebra operations-ல் முக்கியமான data structures-ஐ initialize செய்ய உதவுகிறது.

#### எப்போது **matlib.ones()** பயன்படுத்த வேண்டும்?

- **Data Initialization**: Calculations-ஐ ஆரம்பிக்கும் முன் default values-ஆக ones கொண்ட data structures-ஐ initialize செய்ய.
- **Matrix Operations**: Machine learning algorithms மற்றும் matrix algebra operations-ல் identity values-ஐ represent செய்ய.

#### 18.4. numpy.matlib.eye()

**matlib.eye()** function-ஐ diagonal values-ல் ones மற்றும் மற்ற இடங்களில் zeros values கொண்ட ஒரு identity matrix-ஐ உருவாக்க பயன்படுத்தலாம். இது rectangular shape-உம் diagonal-ல் identity values-ஐ represent செய்யும்.

```python
# Eye matrix (identity matrix) உருவாக்கல்
eye_matrix = matlib.eye(n=3, M=4, k=0, dtype=int)
print("Eye matrix:\n", eye_matrix)
```

**Output:**

```
Eye matrix:
 [[1 0 0 0]
 [0 1 0 0]
 [0 0 1 0]]
```

- **matlib.eye()** function-ஐ பயன்படுத்தி 3 rows மற்றும் 4 columns கொண்ட matrix-ஐ diagonal-ல் ones values-ஐ கொண்டு உருவாக்கியுள்ளோம்.
- **k=0** என்பது main diagonal-ஐ குறிக்கிறது, ஆனால் positive அல்லது negative values கொடுத்தால், upper அல்லது lower diagonals-ஐ represent செய்ய முடியும்.

#### எப்போது **matlib.eye()** பயன்படுத்த வேண்டும்?

- **Identity Matrix Creation**: Linear algebra மற்றும் matrix inversion operations-ல் identity matrix-ஐ உருவாக்க.
- **Diagonal Operations**: Specific diagonal-ல் values-ஐ represent செய்து computations-ஐ எளிதாக்க.

#### 18.5. numpy.matlib.identity()

**matlib.identity()** function square matrix-ஐ உருவாக்குவதற்காக diagonal-ல் மட்டும் ones values-ஐ கொண்டு பயன்படுத்தப்படுகிறது. இது square matrix-களில் diagonal values-ஐ identity values-ஆக represent செய்யும்.

```python
# Identity matrix உருவாக்கல்
identity_matrix = matlib.identity(4, dtype=float)
print("Identity matrix:\n", identity_matrix)
```

**Output:**

```
Identity matrix:
 [[1. 0. 0. 0.]
 [0. 1. 0. 0.]
 [0. 0. 1. 0.]
 [0. 0. 0. 1.]]
```

- **matlib.identity()** function-ஐ பயன்படுத்தி 4x4 square identity matrix-ஐ diagonal-ல் ones values-ஐ கொண்டு உருவாக்கியுள்ளோம்.
- Identity matrix என்பது square matrix algebra மற்றும் linear transformations-ல் மிகவும் முக்கியமானது.

#### எப்போது **matlib.identity()** பயன்படுத்த வேண்டும்?

- **Square Matrix Operations**: Linear algebra operations மற்றும் machine learning algorithms-ல் identity matrix-ஐ represent செய்ய.
- **Matrix Calculations**: Square matrix calculations-ஐ ஆரம்ப கட்டத்தில் identity values கொண்டு initialize செய்ய.

### 18.6. numpy.matlib.rand()

**matlib.rand()** function-ஐ பயன்படுத்தி, uniform distribution அடிப்படையில் random values கொண்ட ஒரு matrix-ஐ உருவாக்கலாம். இது scientific computing மற்றும் statistical analysis-ல் random data generation-ஐ memory-efficient-ஆக செய்ய உதவுகிறது.

```python
import numpy.matlib as matlib

# Random matrix உருவாக்கல்
random_matrix = matlib.rand(3, 3)
print("Random matrix:\n", random_matrix)
```

**Output:**

```
Random matrix:
 [[0.54358789 0.23467931 0.67890512]
 [0.89012345 0.12345678 0.67894321]
 [0.56781234 0.23456789 0.89123456]]
```

- **matlib.rand()** function-ஐ பயன்படுத்தி 3 rows மற்றும் 3 columns கொண்ட random values கொண்ட matrix-ஐ உருவாக்கியுள்ளோம்.
- இங்கு random values-ஐ **uniform distribution** அடிப்படையில் உருவாக்கியுள்ளோம், அதாவது values-ஐ 0 மற்றும் 1 இடையே சமமான probability கொண்டு எடுத்துக்கொள்ளப்பட்டுள்ளன.
- இந்த method-ஐ stochastic simulations, Monte Carlo methods, மற்றும் statistical modeling-ல் random values-ஐ உருவாக்க பயன்படுத்தலாம்.

### எப்போது **matlib.rand()** function-ஐ பயன்படுத்த வேண்டும்?

- **Statistical Analysis**: Data-ஐ random sampling அடிப்படையில் உருவாக்கும்போது.
- **Simulation Modeling**: Random values-ஐ அடிப்படையாக simulation-களை உருவாக்க வேண்டிய data structures-ல்.
- **Algorithm Testing**: Machine learning algorithms மற்றும் computational models-ஐ random input data கொண்டு validate செய்ய.

### Key Features of matlib.rand()

- **Uniform Distribution**: Random values-ஐ 0 மற்றும் 1 இடையே சமமான probability கொண்டு உருவாக்கும்.
- **Memory-efficient**: Memory-யை அளவிற்கேற்ப allocate செய்து, large-scale data generation-ஐ செய்யும்.
- **Scientific Computing**: Stochastic analysis மற்றும் random sampling operations-ஐ memory-efficient-ஆக செய்ய உதவும்.

NumPy-யின் matrix library functions-ஐ memory-efficient-ஆகவும், computationally fast-ஆகவும், data structures-ஐ initialize செய்ய பயன்படுத்தலாம். Scientific computing மற்றும் data analysis-ல் matrix-களை உருவாக்கவும், manipulate செய்யவும் இந்த functions மிகவும் பயனுள்ளதாக இருக்கும்.

<div style="page-break-after: always;"></div>

### 19. NUMPY − LINEAR ALGEBRA

NumPy-யில் **linear algebra** operations-ஐ செய்ய பல முக்கியமான functions உள்ளன. இந்த functions matrix multiplication, inner products, determinants, மற்றும் linear equations-ஐ solve செய்ய memory-efficient மற்றும் computationally fast-ஆக செயல்படுகின்றன. 

#### 19.1. numpy.dot()

**dot()** function-ஐ பயன்படுத்தி, இரண்டு arrays-இன் dot product-ஐ கணக்கிடலாம். Dot product என்பது linear algebra-இல் முக்கியமான operation ஆகும், இது vectors மற்றும் matrices-இன் multiplication-ஐ உள்ளடக்கியது.

```python
import numpy as np

# Dot product operation
a = np.array([1, 2])
b = np.array([3, 4])
dot_product = np.dot(a, b)
print("Dot product:", dot_product)
```

**Output:**

```
Dot product: 11
```

- **np.dot()** function-ஐ பயன்படுத்தி arrays **a** மற்றும் **b**-இன் dot product-ஐ கணக்கிட்டோம்.
- Dot product calculation: (1 * 3) + (2 * 4) = 3 + 8 = 11

#### 19.2. numpy.vdot()

**vdot()** function-ஐ flattened arrays-இன் dot product-ஐ கணக்கிட பயன்படுத்தலாம். Flattened arrays-இல், multi-dimensional arrays-ஐ single-dimensional-ஆக மாற்றி dot product operation செய்யும்.

```python
# Vdot product operation
vdot_product = np.vdot(a, b)
print("Vdot product:", vdot_product)
```

**Output:**

```
Vdot product: 11
```

- **np.vdot()** function-ஐ flattened arrays-இல் dot product operation செய்ய memory-efficient-ஆக பயன்படுத்துகிறோம்.
- Flattening ensures that the dot product operation works on single-dimensional data.

#### 19.3. numpy.inner()

**inner()** function-ஐ பயன்படுத்தி, arrays-இன் inner product-ஐ கண்டறியலாம். Inner product என்பது vectors-இன் corresponding elements-ஐ multiply செய்து, அதன் summation-ஐ return செய்யும் operation ஆகும்.

```python
# Inner product operation
inner_product = np.inner(a, b)
print("Inner product:", inner_product)
```

**Output:**

```
Inner product: 11
```

- **np.inner()** function-ஐ inner product operation செய்ய vectors-ஐ பயன்படுத்தியுள்ளோம்.
- Inner product calculation: (1 * 3) + (2 * 4) = 11, which is similar to dot product.

#### 19.4. numpy.matmul()

**matmul()** function-ஐ matrix multiplication செய்ய பயன்படுத்தலாம். Matrix multiplication என்பது two-dimensional arrays-இல் row-by-column multiplication operation ஆகும்.

```python
# Matrix multiplication operation
matrix1 = np.array([[1, 2], [3, 4]])
matrix2 = np.array([[5, 6], [7, 8]])
matrix_product = np.matmul(matrix1, matrix2)
print("Matrix product:\n", matrix_product)
```

**Output:**

```
Matrix product:
 [[19 22]
 [43 50]]
```

- **np.matmul()** function-ஐ matrix multiplication செய்ய பயன்படுத்தியுள்ளோம்.
- Matrix multiplication:
  - Row 1: (1 * 5) + (2 * 7) = 19
  - Row 2: (3 * 5) + (4 * 7) = 43

#### 19.5. Determinant Calculation

Numpy-யின் **det()** function-ஐ பயன்படுத்தி, square matrix-இன் determinant-ஐ கண்டறியலாம். Determinant என்பது linear algebra-இல் matrix-ஐ invertible ஆக மாற்றுவதற்கு பயன்படும் scalar value ஆகும்.

```python
# Determinant calculation
det_value = np.linalg.det(matrix1)
print("Determinant:", det_value)
```

**Output:**

```
Determinant: -2.0000000000000004
```

- np.linalg.det()** function-ஐ பயன்படுத்தி square matrix-இன் determinant-ஐ கண்டறிந்தோம்.
- Determinant-ஐ use செய்து matrix invertible property-ஐ validate செய்யலாம்.

#### 19.6. numpy.linalg.solve()

**solve()** function-ஐ linear equations-இன் solution-ஐ கண்டறிய பயன்படுத்தலாம். இது linear equations-ஐ matrix representation-ல் convert செய்து, variables-ஐ கண்டறிகிறது.

```python
# Solving linear equations
coefficients = np.array([[3, 1], [1, 2]])
constants = np.array([9, 8])
solutions = np.linalg.solve(coefficients, constants)
print("Solutions:", solutions)
```

**Output:**

```
Solutions: [2. 3.]
```

- **np.linalg.solve()** function-ஐ linear equations-ஐ solve செய்ய matrix algebra-ஐ பயன்படுத்தி variables-ஐ கண்டறிந்தோம்.
- Equations:
  - 3x + 1y = 9
  - 1x + 2y = 8
  - Solution: x = 2, y = 3

<div style="page-break-after: always;"></div>

### 20. NUMPY − MATPLOTLIB

NumPy-யுடன் **Matplotlib**-ஐ இணைத்து data-ஐ visualizations செய்வது மிகவும் எளிதாகவும் பயனுள்ளதாகவும் இருக்கிறது. Matplotlib plotting library-ஐ பயன்படுத்தி graphs மற்றும் charts உருவாக்கலாம். இது data-ஐ graphical format-ஆக represent செய்து, trends மற்றும் patterns-ஐ எளிதாக புரிந்து கொள்ள உதவுகிறது.

#### 20.1. Sine Wave Plot

**Sine wave plot**-ஐ உருவாக்கி data-ஐ visualize செய்வது data trends-ஐ புரிந்துகொள்ள உதவுகிறது. Sine wave என்பது periodic function-ஐ graph-ஆக காட்டும் representation ஆகும்.

```python
import matplotlib.pyplot as plt
import numpy as np

# Sine wave plot
x = np.linspace(0, 10, 100)  # 0 முதல் 10 வரை 100 values
y = np.sin(x)  # sine function-ஐ calculate செய்கிறது
plt.plot(x, y)  # sine wave-ஐ plot செய்கிறது
plt.title("Sine Wave")  # plot-க்கு தலைப்பு
plt.xlabel("X-axis")  # horizontal axis-க்கு பெயர்
plt.ylabel("Y-axis")  # vertical axis-க்கு பெயர்
plt.show()  # plot-ஐ காட்டுகிறது
```

**Output:**

<img src="data:image/png;base64,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" alt="img" style="zoom:50%;" /> 

- **x** values 0 முதல் 10 வரை equal intervals-ல் values-ஐ கொண்டு வருகிறது.
- **y = np.sin(x)** என்பது sine function-ஐ பயன்படுத்தி values-ஐ பெறுகிறது.
- **plt.plot()**-ஐ பயன்படுத்தி sine wave-ஐ visualize செய்கிறது.
- இது signal processing மற்றும் periodic functions-ஐ study செய்ய பயன்படுகிறது.

#### 20.2. subplot()

**subplot()** function-ஐ ஒரே figure-இல் பல plots-ஐ உருவாக்க பயன்படுத்தலாம். இது multiple graphs-ஐ ஒரே chart-ல் அணுக்கமாகக் காண்பிக்க உதவுகிறது.

```python
# Subplots creation
plt.subplot(2, 1, 1)  # முதல் subplot
plt.plot(x, np.sin(x))  # sine wave plot
plt.title("Sine Wave")

plt.subplot(2, 1, 2)  # இரண்டாம் subplot
plt.plot(x, np.cos(x))  # cosine wave plot
plt.title("Cosine Wave")

plt.tight_layout()  # subplot-களுக்குள் overlap இல்லாமல் düzenle செய்கிறது
plt.show()
```

<img src="data:image/png;base64,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" alt="img" style="zoom:50%;" />



- **plt.subplot(2, 1, 1)** என்பது 2 rows மற்றும் 1 column கொண்ட subplot layout-ஐ முதலில் sine wave-க்கு set செய்கிறது.
- **plt.subplot(2, 1, 2)** என்பது இரண்டாவது subplot-ஐ cosine wave-ஐ plot செய்ய set செய்கிறது.
- இது graphs-ஐ compare செய்வதற்கான சிறந்த முறையாகும், data trends-ஐ side-by-side analyze செய்ய உதவுகிறது.

#### 20.3. bar( )

**bar( )** function-ஐ data-ஐ bar chart-ஆக plot செய்ய பயன்படுத்தலாம். Bar chart-கள் data-ஐ categories அடிப்படையில் compare செய்ய உதவுகின்றன.

```python
# Bar chart creation
categories = ['A', 'B', 'C']  # Categories names
values = [3, 7, 5]  # Corresponding values
plt.bar(categories, values)  # bar chart-ஐ plot செய்கிறது
plt.title("Bar Chart")  # bar chart-க்கு தலைப்பு
plt.xlabel("Categories")  # categories-ஐ x-axis-ல் காட்டுகிறது
plt.ylabel("Values")  # values-ஐ y-axis-ல் காட்டுகிறது
plt.show()
```

#### <img src="data:image/png;base64,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AAAWCHLy4OfPn1fr1q3VoUMHrV69WpUqVVJKSorKly/v5FgAAMASjobKlClTFB0drQULFnjX1apVy8GJAACATRy99PPpp5+qefPm6tevnypXrqymTZvqvffeu+b2Ho9H2dnZPg8AAHDncjRU/vWvfykhIUF169bV2rVr9cwzz2j06NH661//etXt4+LiFBER4X1ER0cX88QAAKA4uYwxxqmDBwcHq3nz5tq+fbt33ejRo7Vz50599dVXBbb3eDzyeDze5ezsbEVHRysrK0vh4eHFMjNQnGq++LnTI8BhqZO7Oz0CcMtlZ2crIiKiUP//dvSMSrVq1dSwYUOfdffee69OnTp11e3dbrfCw8N9HgAA4M7laKi0bt1aR48e9Vn39ddf6+6773ZoIgAAYBNHQ+W5557Tjh079MYbb+jYsWNatGiR5s6dq9jYWCfHAgAAlnA0VB544AGtWLFCixcvVuPGjfXnP/9ZM2bM0KBBg5wcCwAAWMLRz1GRpB49eqhHjx5OjwEAACzk+EfoAwAAXAuhAgAArEWoAAAAaxEqAADAWoQKAACwFqECAACsRagAAABrESoAAMBahAoAALAWoQIAAKxFqAAAAGsRKgAAwFqECgAAsBahAgAArEWoAAAAaxEqAADAWoQKAACwFqECAACsRagAAABrESoAAMBahAoAALAWoQIAAKxFqAAAAGsRKgAAwFqECgAAsBahAgAArEWoAAAAaxEqAADAWoQKAACwFqECAACsRagAAABrESoAAMBahAoAALAWoQIAAKxFqAAAAGsRKgAAwFqECgAAsBahAgAArEWoAAAAazkaKq+++qpcLpfPo0GDBk6OBAAALBLk9ACNGjXS+vXrvctBQY6PBAAALOF4FQQFBalq1apOjwEAACzk+D0qKSkpioqKUu3atTVo0CCdOnXqmtt6PB5lZ2f7PAAAwJ3L0TMqDz74oBITE1W/fn2lp6dr4sSJatOmjQ4ePKiwsLAC28fFxWnixIkOTAoAJVPNFz93egQ4LHVyd0eP7+gZlZiYGPXr109NmjRR165d9cUXXygzM1NLly696vbjxo1TVlaW95GWllbMEwMAgOLk+D0qv1SuXDnVq1dPx44du+rzbrdbbre7mKcCAABOcfwelV/KycnR8ePHVa1aNadHAQAAFnA0VJ5//nlt3rxZqamp2r59u/r06aPA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ql+/flHOBgAASrhCh0qpUqX0t7/9TT169FBgYGBRzgQAACDJj1D59NNPi3IOAACAAm7qXT8AAABFiVABAADWIlQAAIC1CBUAAGAtQgUAAFjL0VBJSEhQkyZNFB4ervDwcLVs2VKrV692ciQAAGARR0Plrrvu0uTJk7V7927t2rVLHTt21G9/+1sdOnTIybEAAIAlbvi7fm6Fnj17+ixPmjRJCQkJ2rFjhxo1auTQVAAAwBaOhsov5eXl6eOPP9bFixfVsmXLq27j8Xjk8Xi8y9nZ2cU1HgAAcIDjoXLgwAG1bNlSP/74o8qWLasVK1aoYcOGV902Li5OEydOLLbZar74ebEdC3ZKndzd6REAoERz/F0/9evX1969e/WPf/xDzzzzjIYMGaJ//vOfV9123LhxysrK8j7S0tKKeVoAAFCcHD+jEhwcrDp16kiSmjVrpp07d2rmzJl69913C2zrdrvldruLe0QAAOAQx8+o/Fp+fr7PfSgAAKDkcvSMyrhx4xQTE6MaNWrowoULWrRokTZt2qS1a9c6ORYAALCEo6Fy5swZPf7440pPT1dERISaNGmitWvXqkuXLk6OBQAALOFoqMybN8/JwwMAAMtZd48KAADAFYQKAACwFqECAACsRagAAABrESoAAMBahAoAALAWoQIAAKxFqAAAAGsRKgAAwFqECgAAsBahAgAArEWoAAAAaxEqAADAWoQKAACwFqECAACsRagAAABrESoAAMBahAoAALAWoQIAAKxFqAAAAGsRKgAAwFqECgAAsBahAgAArEWoAAAAaxEqAADAWoQKAACwFqECAACsRagAAABrESoAAMBahAoAALAWoQIAAKxFqAAAAGsRKgAAwFqECgAAsBahAgAArEWoAAAAaxEqAADAWoQKAACwFqECAACs5WioxMXF6YEHHlBYWJgqV66s3r176+jRo06OBAAALOJoqGzevFmxsbHasWOH1q1bp8uXL+vhhx/WxYsXnRwLAABYIsjJg69Zs8ZnOTExUZUrV9bu3bvVtm1bh6YCAAC2cDRUfi0rK0uSVKFChas+7/F45PF4vMvZ2dnFMhcAAHCGNTfT5ufna8yYMWrdurUaN2581W3i4uIUERHhfURHRxfzlAAAoDhZEyqxsbE6ePCglixZcs1txo0bp6ysLO8jLS2tGCcEAADFzYpLPyNHjtSqVau0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/fbb5uuvvzZffvmladq0qRk6dKgxxpidO3eawMBAs2jRIpOammr27NljZs6ceav+qAH4gVABYIwx5h//+IeRZJYvX+7X6z7++GMTGRnpXV6wYIFPXBhjzMmTJ01gYKD59ttvfdZ36tTJjBs3zhhjzKOPPmq6d+/u8/ygQYN89tWqVSszYsQIn2369etnHnnkEe+yJDNmzBifbX4dKsOHDzdPPfWUzzZbt241AQEB5ocffjDLli0z4eHhJjs7+z//AQAoUlz6ASBJMoX8IvX169erU6dOql69usLCwvTYY4/p3LlzunTp0jVfc+DAAeXl5alevXoqW7as97F582YdP35cknT06FG1aNHC53W/Xj58+LBat27ts65169Y6fPiwz7rmzZtf92fYt2+fEhMTfWbp2rWr8vPzdeLECXXp0kV33323ateurccee0wffvjhdX8+AEWHm2kBSJLq1q0rl8t13RtmU1NT1aNHDz3zzDOaNGmSKlSooG3btmn48OHKzc1VmTJlrvq6nJwcBQYGavfu3QoMDPR5rmzZsrf055Ck0NDQ6z6fk5Ojp59+WqNHjy7wXI0aNRQcHKw9e/Zo06ZN+vvf/67x48fr1Vdf1c6dO617RxNwp+OMCgBJUoUKFdS1a1fFx8f73FR6RWZmpnbv3q38/HxNmzZN//3f/6169erp9OnTPtsFBwcrLy/PZ13Tpk2Vl5enM2fOqE6dOj6PK+/GqV+/vnbu3Onzul8v33vvvfryyy991n355Zdq2LChXz/rb37zG/3zn/8sMEudOnUUHBwsSQoKClLnzp315ptvav/+/UpNTVVSUpJfxwFw8wgVAF7x8fHKy8tTixYttGzZMqWkpOjw4cOaNWuWWrZsqTp16ujy5ct655139K9//Uvvv/++5syZ47OPmjVrKicnRxs2bNDZs2d16dIl1atXT4MGDdLjjz+u5cuX68SJE0pOTlZcXJw+//xzSdKoUaP0xRdfaPr06UpJSdG7776r1atXy+Vyeff9pz/9SYmJiUpISFBKSoqmT5+u5cuX6/nnn/fr53zhhRe0fft2jRw5Unv37lVKSoo++eQTjRw5UpK0atUqzZo1S3v37tXJkye1cOFC5efnq379+jf5JwzAb07fJAPALqdPnzaxsbHm7rvvNsHBwaZ69eqmV69eZuPGjcYYY6ZPn26qVatmQkJCTNeuXc3ChQt9blQ1xpjf//73JjIy0kgyEyZMMMYYk5uba8aPH29q1qxpSpUqZapVq2b69Olj9u/f733d3LlzTfXq1U1ISIjp3bu3ef31103VqlV95ps9e7apXbu2KVWqlKlXr55ZuHChz/OSzIoVK3zW/fpmWmOMSU5ONl26dDFly5Y1oaGhpkmTJmbSpEnGmJ9vrG3Xrp0pX768CQkJMU2aNDEfffTRzf3BArghLmMKeQcdABSzESNG6MiRI9q6davTowBwCDfTArDGW2+9pS5duig0NFSrV6/WX//6V82ePdvpsQA4iDMqAKzRv39/bdq0SRcuXFDt2rU1atQo/f73v3d6LAAOIlQAAIC1eNcPAACwFqECAACsRagAAABrESoAAMBahAoAALAWoQIAAKxFqAAAAGsRKgAAwFqECgAAsNb/B/bGlfbUQpi1AAAAAElFTkSuQmCC" alt="img" style="zoom:50%;" />



- **categories** array-ல் உள்ள values horizontal axis-ல் (X-axis) காட்டப்படும்.
- **values** array-ல் உள்ள corresponding heights vertical axis-ல் (Y-axis) காட்டப்படும்.
- Bar chart-கள் data-ஐ categories அடிப்படையில் visual comparison செய்ய மிகவும் உதவுகின்றன.

<div style="page-break-after: always;"></div>

### 21. NUMPY – HISTOGRAM USING MATPLOTLIB

Numpy-யுடன் **Matplotlib**-ஐ histogram உருவாக்கி data distribution-ஐ காணலாம். Histogram என்பது data-இன் frequency distribution-ஐ காண்பிக்கும் visual representation ஆகும், இது data-இல் values எவ்வாறு spread ஆகவுள்ளது என்பதைக் காட்டுகிறது.

#### 21.1. numpy.histogram()

**histogram()** function-ஐ data distribution-ஐ கண்டறிய பயன்படுத்தலாம். இது data-ஐ bins எனப்படும் intervals-களாக பிரித்து, ஒவ்வொரு interval-ல் values எவ்வளவு உள்ளன என்பதைக் காட்டுகிறது.

```python
import matplotlib.pyplot as plt
import numpy as np

# Histogram creation
data = np.random.randn(1000)  # Randomly generated data with normal distribution
plt.hist(data, bins=30, alpha=0.7, color='blue')  # Histogram plot
plt.title("Histogram")  # Plot title
plt.xlabel("Data Values")  # X-axis label
plt.ylabel("Frequency")  # Y-axis label
plt.show()  # Display the plot
```

<img src="data:image/png;base64,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" alt="img" style="zoom:50%;" />



- **data = np.random.randn(1000)** என்பது normal distribution கொண்ட 1000 random values-ஐ உருவாக்குகிறது.
- **plt.hist()** function data-ஐ 30 bins-ஆக பிரித்து frequency distribution-ஐ காட்டுகிறது.
- Histogram data distribution-ஐ எடுத்துக்காட்டி, data-இல் values எந்த range-ல் அதிகமாக உள்ளன என்பதைக் காட்டுகிறது.

<div style="page-break-after: always;"></div>

### 22. NUMPY − I/O WITH NUMPY

NumPy-யில் data-ஐ save மற்றும் load செய்ய பல methods உள்ளன, இதனால் data-ஐ file format-ல் எளிதாக சேமிக்கவும், retrieve செய்யவும் முடியும். Data I/O operations scientific computing மற்றும் data analysis-ல் மிகவும் முக்கியமானவை.

#### 22.1. numpy.save()

**save()** function-ஐ பயன்படுத்தி, array-ஐ binary format-ல் (.npy) சேமிக்கலாம். இது data-ஐ compact-ஆகவும் memory-efficient-ஆகவும் சேமிக்க உதவுகிறது.

```python
import numpy as np

# Saving array to file
array = np.array([1, 2, 3, 4, 5])
np.save('my_array', array)  # Save the array as a .npy file
```

**Output:**

```
Array saved as 'my_array.npy' in the current directory.
```

- **np.save()** function-ஐ array-ஐ binary format-ல் சேமிக்க பயன்படுத்துகிறோம்.
- இந்த method data-ஐ efficient-ஆக save செய்து, future usage-க்கு compact format-ல் வைத்திருக்கிறது.

#### 22.2. numpy.savetxt()

**savetxt()** function-ஐ பயன்படுத்தி, array-ஐ text file format-ல் சேமிக்கலாம். Text format-ல் data-ஐ human-readable-ஆக save செய்ய இது பயன்படும்.

```python
# Saving array to text file
np.savetxt('my_array.txt', array, delimiter=',')  # Save the array as a .txt file
```

**Output:**

```
Array saved as 'my_array.txt' with comma-separated values.
```

- **np.savetxt()** function array-ஐ text file format-ல் (.txt) சேமிக்கிறது.
- Text file format data-ஐ human-readable-ஆக save செய்ய உதவுகிறது, இது data analysis மற்றும் data sharing-க்கு பயனுள்ளதாக இருக்கும்.

<div style="page-break-after: always;"></div>

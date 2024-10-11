[toc]



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

### 2. NUMPY − ARRAY CREATION ROUTINES

### 2. NUMPY − ARRAY CREATION ROUTINES

NumPy-ல் array-களை உருவாக்க பல்வேறு methods உள்ளன, அவற்றைப் பயன்படுத்தி data handling மற்றும் computation process-களை எளிதாக்கலாம். இப்போது, சில பொதுவாகப் பயன்படுத்தப்படும் array creation functions பற்றி விரிவாகப் பார்ப்போம்.

#### 2.1. numpy.empty

**numpy.empty()** function ஒரு initialization values இல்லாத array-ஐ உருவாக்க பயன்படுகிறது. இதனால், array-இல் உள்ள values ஏதாவது முன்பே memory-யில் இருந்த random values ஆக இருக்கும். இதனால், memory-யில் உள்ள values reset செய்யப்படாமல், அந்த values 그대로 array-இல் வரலாம்.

**Syntax:**
```python
numpy.empty(shape, dtype=float, order='C')
```

- **shape**: இது array-இன் structure-ஐ (rows, columns) குறிப்பிடுகிறது.
- **dtype**: இந்த optional parameter மூலம் array-இன் data type-ஐ குறிப்பிடலாம். (default: `float`)
- **order**: memory layout-ஐ குறிப்பிடும் (default: 'C', C-style row-major order).

**Example:**
```python
import numpy as np

empty_array = np.empty((2, 3))
print("Empty array:\n", empty_array)
```

**Explanation:**

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

**Explanation:**

- இங்கு **np.ones()** function-ஐ பயன்படுத்தி, 3 rows மற்றும் 3 columns கொண்ட ஒரு array உருவாக்கப்பட்டுள்ளது.
- இந்த array-இன் எல்லா elements-ம் 1 values கொண்டவை.

**Key Differences:**
- **empty()** function data-ஐ ஆரம்பத்தில் initialize செய்யாமல் array-ஐ memory-யில் உள்ள random values கொண்டு உருவாக்கும்.
- **zeros()** மற்றும் **ones()** functions, memory-யில் அடர்த்தியான array-களை உருவாக்கி, array-ஐ முறையாக initialize செய்து, எளிமையான calculations செய்ய உதவுகின்றன.

இதன் மூலம், **zeros()** மற்றும் **ones()** functions மிகவும் பயனுள்ளதாக இருக்கும், ஏனெனில் அவை predictable values கொண்ட array-களை உருவாக்குகின்றன, computation-ஐ எளிதாக்குகின்றன.

### 3. NUMPY − ARRAY FROM EXISTING DATA

Numpy-ல் array-களை உருவாக்குவதற்கான முக்கியமான வழிகளில் ஒன்றாக **முந்தைய data**-விலிருந்து array-ஐ உருவாக்குவது அமைகிறது. இது Python-ல் ஏற்கனவே இருக்கும் data structures, போன்றவை (lists, buffers, iterables) கொண்டு நமக்கு தேவையான array-களை எளிதாக உருவாக்க உதவுகிறது. இதனால் data-ஐ NumPy-யின் powerful array operations-இல் பயன்படுத்த முடியும்.

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

இந்த Code-இல், ஒரு Python list **list_data**-ஐ **asarray()** function-ஐ பயன்படுத்தி NumPy array-ஆக மாற்றுகிறோம். இதன் மூலம், original data type retain (சேமித்து) array-ஆக மாற்றப்படுகிறது, மேலும் memory usage நம்மால் more efficiently பயன்படுத்த முடிகிறது.

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

### 5. NUMPY − INDEXING & SLICING

NumPy array-களில் **indexing** மற்றும் **slicing** methods மிக முக்கியமானவை, ஏனெனில் இவையால் array-களின் தனிப்பட்ட elements-ஐ அணுகுவதோடு, array-களின் ஒரு பகுதியை எளிதாக பிரிக்கவும் முடிகிறது. இவை data extraction மற்றும் manipulation-ஐ மிக எளிதாக்குகின்றன.

#### Example of Indexing and Slicing

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

### Key Points to Remember
- **Indexing** array-இன் குறிப்பிட்ட இடத்தில் இருக்கும் individual element-ஐ return செய்கிறது.
- **Slicing** array-இல் ஒரு range-ஐ (start:stop) அடிப்படையாகக் கொண்டு elements-ஐ return செய்கிறது.
- Slicing-ல் **start** value அடங்கும், ஆனால் **stop** value அடங்காது.

இந்த methods data extraction-ஐ மிக எளிமையாக மாற்றுகின்றன, மேலும் NumPy array-களுடன் நாம் பயனுள்ளதாக மற்றும் திறமையாக செயல்பட உதவுகின்றன.



### 6. NUMPY − ADVANCED INDEXING

NumPy-இல் **advanced indexing** முறைகள் array values-ஐ எளிதாக அணுகவும், update செய்யவும் அனுமதிக்கின்றன. இவை data selection மற்றும் manipulation-ஐ மேலும் திறமையாக செயல்படுத்த உதவுகின்றன.

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

### Summary of Advanced Indexing

- **Integer indexing**: Array-இல் specific elements-ஐ position அடிப்படையில் எளிதாக பெற உதவுகிறது.
- **Boolean indexing**: Condition-based filtering-ஐ பயன்படுத்தி array values-ஐ வேகமாகவும் எளிதாகவும் தேர்வு செய்ய உதவுகிறது.

இந்த advanced indexing முறைகள் NumPy array-களில் data selection மற்றும் manipulation-ஐ நுணுக்கமாகவும் திறமையாகவும் செயல்படுத்த உதவுகின்றன.



- ### 7. NUMPY − BROADCASTING

  NumPy-யில் **broadcasting** என்பது shape-கள் வேறுபட்ட array-களை arithmetic operations-ல் பயன்படுத்த ஒரு நுட்பமாகும். இது data-ஐ duplicate செய்யாமல், memory-efficient-ஆக operations-ஐ நேரடியாக செய்ய உதவுகிறது. Broadcasting-ஐ பயன்படுத்தி arrays-இல் arithmetic operations செய்யும்போது, NumPy data-ஐ தானாகவே மிக எளிதாகப் பொருந்தும் விதமாக மாற்றுகிறது.

  #### Broadcasting என்றால் என்ன?

  Broadcasting என்பது NumPy-யின் திறனாக, இரண்டு array-களின் shape-கள் பொருந்தாதபோதும், arithmetic operations-ஐ செய்து முடிக்க data-ஐ தானாக விரிவாக்கி ஆக்க முறையாகும். NumPy-யின் broadcasting விதிகள் array-களை ஒன்று சேர்க்கவும், குறைந்த memory-யில் calculations செய்யவும் உதவுகின்றன.

  

  ```python
  import numpy as np
  
  # Broadcasting உதாரணம்
  array1 = np.array([1, 2, 3])
  array2 = np.array([[1], [2], [3]])
  
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

### 8. NUMPY − ITERATING OVER ARRAY

NumPy array-களை **iterate** செய்வது Python list-களை iterate செய்வதைப் போலவே எளிதானது. NumPy array-களில் iteration செய்யும் நுட்பங்கள் அதிக துல்லியமாகவும் வேகமாகவும் செயல்படுவதற்காக வடிவமைக்கப்பட்டுள்ளன. இதன் மூலம், multi-dimensional array-களில் iteration செய்யும்போது memory efficiency மற்றும் execution speed அதிகரிக்கின்றன.

#### 8.1. Iteration Order

NumPy array-களை iterate செய்வதில் **row-major** அல்லது **column-major** order-ல் iteration செய்ய முடியும். 

**Example**:

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

#### விளக்கம்:
- **Row-major** order-ல் iteration செய்யும் போது, ஒவ்வொரு row-யும் தனித்தனியாக iterate செய்யப்படுகிறது. Example-இல், `array`-இன் ஒவ்வொரு row-ஐ print செய்கிறோம்.
- **flat** attribute-ஐ பயன்படுத்தி, array-இன் அனைத்து elements-ஐ flatten செய்து, அவற்றை column-major order-ல் iterate செய்கிறோம்.

**Row-major order** என்பதனால் rows-ஐ முன்னுரிமை கொடுத்து iterate செய்யப்படுகிறது, அதாவது முழு row-ஐ முன்னதாக process செய்யும்.
**flat** attribute-ஐ பயன்படுத்தி, multi-dimensional array-ஐ ஒரு single-dimensional array போல iterate செய்ய முடியும்.

#### 8.2. Modifying Array Values

Iteration-ஐ பயன்படுத்தி array values-ஐ நேரடியாக மாற்றவும் (update) முடியும். இதனால், array-இன் original values-ஐ iteration முறையில் update செய்வது எளிதாகும்.

**Example**:

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

#### Explanation in Tamil:

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

#### External Loop Example:

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

#### விளக்கம்:
- **`flags=['external_loop']`**: இந்த flag-ஐ பயன்படுத்தி, iteration செய்யும் போது data continuous block-ஆக iterate செய்யப்படுகிறது.
- **`order='F'`**: Iteration order-ஐ Fortran-style (column-major) ஆக மாற்றுகிறது, இதனால் column-wise data-ஐ iterate செய்யலாம்.

External loop iteration-ஐ column-wise data handling-க்கு பயன்படுத்தும்போது, இது calculations மற்றும் data processing-ஐ வேகமாகவும் memory-efficient-ஆகவும் செய்கிறது.

### 8.4. Broadcasting Iteration

Broadcasting iteration மூலம் shape வேறுபட்ட array values-ஐ ஒரே நேரத்தில் iterate செய்ய உதவுகிறது. இது NumPy-யின் broadcasting principle-ஐ பயன்படுத்தி, operations-ஐ சிறப்பாக நிறைவேற்றுகிறது.

#### Broadcasting Iteration Example:

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

#### விளக்கம்:
- **Broadcasting Iteration**: Broadcasting iteration-ஐ பயன்படுத்தி shape-ல் வேறுபாடுகள் இருந்தாலும் array values-ஐ இணைத்து iterate செய்ய முடிகிறது.
- **`np.nditer([array1, array2])`**: இரண்டு array-களையும் ஒரே iteration-ல் பயணிக்க பயன்படுகிறது, அதனால் values-ஐ side-by-side compare மற்றும் process செய்ய முடிகிறது.

இந்த broadcasting iteration data manipulation மற்றும் array operations-ஐ மிகவும் சுலபமாகவும் திறமையாகவும் செய்கிறது, ஏனெனில் இது different shapes கொண்ட array-களையும் ஒரு நேரத்தில் iterate செய்து எளிதாக இணைக்கிறது.

### External Loop மற்றும் Broadcasting Iteration-ன் முக்கியத்துவம்

- **External Loop**: ஒரு continuous block-ஆக iteration செய்ய memory-efficient-ஆகவும் வேகமாகவும் செயல்படுகிறது, குறிப்பாக column-wise data processing செய்யும்போது.
- **Broadcasting Iteration**: shape-கள் வேறுபட்டிருந்தாலும் array-களை iterate செய்து, அதனுடன் calculations அல்லது comparisons செய்வதில் மிகவும் பயனுள்ளது.

இவை NumPy array-களில் iteration மற்றும் data handling-ஐ மிகவும் திறமையான முறையில் செய்ய உதவுகின்றன.



### 9. NUMPY – ARRAY MANIPULATION

Numpy array-களை மாற்றவும் மாற்றி அமைக்கவும் பல்வேறு methods உண்டு.

#### 9.1. numpy.reshape

**reshape()** function array-இன் shape-ஐ மாற்றி அமைக்க உதவுகிறது.

```python
# Reshape operation
array = np.array([1, 2, 3, 4, 5, 6])
reshaped_array = array.reshape(2, 3)
print("Reshaped array:\n", reshaped_array)
```

**Output:**

```

```

#### 9.2. numpy.ndarray.flat

**flat** attribute-ஐ பயன்படுத்தி array-இல் உள்ள values-ஐ ஒரு iterator-ஆக பெறலாம்.

```python
for element in array.flat:
    print("Flat element:", element)
```

**Output:**

```

```

#### 9.3. numpy.ndarray.flatten

**flatten()** method multi-dimensional array-ஐ ஒரு single-dimensional array-ஆக மாற்றும்.

```python
flattened_array = array.flatten()
print("Flattened array:", flattened_array)
```

**Output:**

```

```

#### 9.4. numpy.ravel

**ravel()** method multi-dimensional array-ஐ flattened array-ஆக மாற்றும், memory-யை சிக்கனமாக பயன்படுத்தி.

```python
raveled_array = array.ravel()
print("Raveled array:", raveled_array)
```

**Output:**

```

```

#### 9.5 numpy.transpose

**transpose()** function array-இன் axes-ஐ மாற்றி அமைக்க உதவும்.

```python
transposed_array = reshaped_array.transpose()
print("Transposed array:\n", transposed_array)
```

**Output:**

```

```

#### 9.5. numpy.ndarray.T

**T** attribute transpose-ஐ எளிதாக செய்ய ஒரு alternate முறையாகும்.

```python
print("Transposed array using T:\n", reshaped_array.T)
```

**Output:**

```

```

#### 9.6. numpy.swapaxes

**swapaxes()** function array-இல் உள்ள axes-ஐ மாற்றி அமைக்க உதவுகிறது.

```python
swapped_array = reshaped_array.swapaxes(0, 1)
print("Swapped axes array:\n", swapped_array)
```

**Output:**

```

```

#### 9.7. numpy.rollaxis

**rollaxis()** method ஒரு array-இல் உள்ள axes-ஐ ஒரு குறிப்பிட்ட இடத்திற்கு மாற்ற உதவுகிறது.

```python
rolled_array = np.rollaxis(swapped_array, 1)
print("Rolled axes array:\n", rolled_array)
```

**Output:**

```

```

#### 9.7. numpy.broadcast

**broadcast()** function broadcasting operation எப்படி செயல்படுகிறது என்பதை காட்ட உதவுகிறது.

```python
broadcasted = np.broadcast(array1, array2)
for x, y in broadcasted:
    print(f"Broadcasted elements: x = {x}, y = {y}")
```

**Output:**

```

```

இந்த array manipulation methods-அனைத்தும் data-ஐ organize செய்யவும், memory-யை சிக்கனமாக பயன்படுத்தவும் முக்கியமானவை. Numpy-யின் array operations எளிமையானது மற்றும் computationally efficient ஆக இருக்கின்றன.

#### 9.8. numpy.broadcast_to

Numpy-யில் **broadcast_to()** function-ஐ பயன்படுத்தி ஒரு array-யை ஒரு குறிப்பிட்ட shape-க்கு broadcast செய்யலாம். இதனால் array-ஐ duplicate செய்யாமல், arithmetic operations செய்ய முடியும்.

```python
import numpy as np

# Broadcasting array to a new shape
array = np.array([1, 2, 3])
broadcasted_array = np.broadcast_to(array, (3, 3))
print("Broadcasted array:\n", broadcasted_array)
```

**Output:**

```

```

- **broadcast_to()** function array-ஐ புதிய shape-க்கு broadcast செய்கிறது, memory-யை சிக்கனமாகவும் வேகமாகவும் பயன்படுத்தி.

#### 9.9. numpy.expand_dims

**expand_dims()** function array-இல் புதிய axes-ஐ சேர்த்து அதன் dimensionality-ஐ அதிகரிக்க உதவுகிறது.

```python
# Array dimensionality-ஐ அதிகரித்தல்
array = np.array([1, 2, 3])
expanded_array = np.expand_dims(array, axis=0)
print("Expanded array:\n", expanded_array)
```

**Output:**

```

```

- **expand_dims()** function array-இல் ஒரு புதிய axis-ஐ சேர்க்கிறது, இதனால் array-ஐ reshape செய்ய உதவுகிறது.

#### 9.10. numpy.squeeze

**squeeze()** function array-இல் உள்ள unnecessary singleton dimensions-ஐ நீக்க உதவுகிறது.

```python
# Singleton dimensions-ஐ நீக்குதல்
array = np.array([[[1, 2, 3]]])
squeezed_array = np.squeeze(array)
print("Squeezed array:", squeezed_array)
```

**Output:**

```

```

- **squeeze()** method array-இல் உள்ள unwanted singleton dimensions-ஐ அகற்றுகிறது.

#### 9.11. numpy.concatenate

**concatenate()** function-ஐ பயன்படுத்தி இரண்டு அல்லது அதற்கும் அதிகமான array-களை ஒரு இணைந்த array-ஆக உருவாக்கலாம்.

```python
# Arrays-ஐ concatenate செய்தல்
array1 = np.array([1, 2, 3])
array2 = np.array([4, 5, 6])
concatenated_array = np.concatenate((array1, array2))
print("Concatenated array:", concatenated_array)
```

**Output:**

```

```

- **concatenate()** function array-களை இணைத்து ஒரு array-ஆக உருவாக்குகிறது.

#### 9.12. numpy.stack

**stack()** function-ஐ பயன்படுத்தி arrays-ஐ ஒரு புதிய axis-இல் stack செய்யலாம்.

```python
# Arrays-ஐ stack செய்தல்
array1 = np.array([1, 2, 3])
array2 = np.array([4, 5, 6])
stacked_array = np.stack((array1, array2), axis=1)
print("Stacked array:\n", stacked_array)
```

**Output:**

```

```

- **stack()** function arrays-ஐ புதிய axis-இல் stack செய்கிறது.

#### 9.13. numpy.hstack and numpy.vstack

**hstack()** மற்றும் **vstack()** functions-ஐ பயன்படுத்தி arrays-ஐ horizontal மற்றும் vertical-ஆக stack செய்யலாம்.

```python
# Horizontal stacking
hstacked_array = np.hstack((array1, array2))
print("Horizontally stacked array:", hstacked_array)

# Vertical stacking
vstacked_array = np.vstack((array1, array2))
print("Vertically stacked array:\n", vstacked_array)
```

**Output:**

```

```

- **hstack()** function arrays-ஐ horizontal-ஆக stack செய்கிறது.
- **vstack()** function arrays-ஐ vertical-ஆக stack செய்கிறது.

#### 9.14.numpy.split

**split()** function-ஐ பயன்படுத்தி ஒரு array-ஐ பல துண்டுகளாக பிரிக்கலாம்.

```python
# Array-ஐ split செய்தல்
array = np.array([1, 2, 3, 4, 5, 6])
split_array = np.split(array, 3)
print("Split arrays:", split_array)
```

**Output:**

```

```

- **split()** function array-ஐ n துண்டுகளாக பிரிக்க உதவுகிறது.

#### 9.15. numpy.hsplit and numpy.vsplit

**hsplit()** மற்றும் **vsplit()** functions-ஐ horizontal மற்றும் vertical-ஆக arrays-ஐ பிரிக்க பயன்படுத்தலாம்.

```python
# Horizontal split
harray = np.array([[1, 2, 3], [4, 5, 6]])
hsplit_array = np.hsplit(harray, 3)
print("Horizontally split arrays:", hsplit_array)

# Vertical split
vsplit_array = np.vsplit(harray, 2)
print("Vertically split arrays:", vsplit_array)
```

**Output:**

```

```

- **hsplit()** function arrays-ஐ horizontal-ஆக பிரிக்க உதவுகிறது.
- **vsplit()** function arrays-ஐ vertical-ஆக பிரிக்க உதவுகிறது.

#### 9.16. numpy.resize

**resize()** function-ஐ பயன்படுத்தி array-ஐ புதிய shape-க்கு மாற்றலாம். 

```python
# Array-ஐ resize செய்தல்
array = np.array([1, 2, 3, 4])
resized_array = np.resize(array, (2, 3))
print("Resized array:\n", resized_array)
```

**Output:**

```

```

- **resize()** function array-இன் shape-ஐ மாற்றுகிறது.

#### 9.17. numpy.append

**append()** function-ஐ பயன்படுத்தி array-இன் முடிவில் values-ஐ சேர்க்கலாம்.

```python
# Array-இல் values-ஐ append செய்தல்
array = np.array([1, 2, 3])
appended_array = np.append(array, [4, 5, 6])
print("Appended array:", appended_array)
```

**Output:**

```

```

- **append()** function array-இன் முடிவில் values-ஐ சேர்க்க உதவுகிறது.

#### 9.18. numpy.insert

**insert()** function array-இன் குறிப்பிட்ட இடத்தில் values-ஐ சேர்க்கும்.

```python
# Array-இல் values-ஐ insert செய்தல்
array = np.array([1, 2, 3])
inserted_array = np.insert(array, 1, [7, 8])
print("Inserted array:", inserted_array)
```

**Output:**

```

```

- **insert()** function array-இல் குறிப்பிட்ட இடத்தில் values-ஐ சேர்க்க உதவுகிறது.

#### 9.19. numpy.delete

**delete()** function array-இல் உள்ள values-ஐ நீக்க உதவுகிறது.

```python
# Array-இல் values-ஐ delete செய்தல்
array = np.array([1, 2, 3, 4, 5])
deleted_array = np.delete(array, [1, 3])
print("Deleted array:", deleted_array)
```

**Output:**

```

```

- **delete()** function array-இல் உள்ள values-ஐ அகற்ற உதவுகிறது.

#### 9.20. numpy.unique

**unique()** function array-இல் உள்ள unique values-ஐ பெற்றுத் தரும்.

```python
# Array-இல் unique values-ஐ பெறுதல்
array = np.array([1, 2, 2, 3, 4, 4, 5])
unique_values = np.unique(array)
print("Unique values:", unique_values)
```

**Output:**

```

```

- **unique()** function array-இல் உள்ள repeating elements-ஐ அகற்றி unique values-ஐ மட்டும் பெற உதவுகிறது.

இந்த array manipulation methods-அனைத்தும் data-ஐ organize செய்யவும், memory-யை சிக்கனமாக பயன்படுத்தவும் மிக முக்கியமானவை. Numpy-யின் array operations எளிதாகவும் computationally efficient-ஆகவும் இருக்கின்றன.

### 13. NUMPY – BINARY OPERATORS

Numpy-யில் **binary operators** உபயோகப்படுத்தி bitwise operations செய்யலாம். இது binary (இரும) அளவிலான data-களில் செயல்பட பயன்படுகின்றது.

#### 13.1. bitwise_and
**bitwise_and** operator இரண்டு arrays-இன் bitwise AND operation-ஐ return செய்கிறது.

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

```

- **bitwise_and** operation மூலம் இரண்டு binary values-இன் AND operation-ஐ செய்கிறது.

#### 13.2. bitwise_or
**bitwise_or** operator இரண்டு arrays-இன் bitwise OR operation-ஐ return செய்கிறது.

```python
# Bitwise OR operation
a = np.array([0b1100])
b = np.array([0b1010])
result = np.bitwise_or(a, b)
print("Bitwise OR:", result)
```

**Output:**

```

```

- **bitwise_or** operation மூலம் இரண்டு binary values-இன் OR operation-ஐ செய்கிறது.

#### 13.3. numpy.invert()
**invert()** function array-இன் bitwise NOT operation-ஐ செய்கிறது, அதாவது, ஒவ்வொரு bit-ஐ எதிர்மறையாக மாற்றுகிறது.

```python
# Bitwise NOT operation
a = np.array([0b1100])
result = np.invert(a)
print("Bitwise NOT:", result)
```

**Output:**

```

```

- **invert()** operation ஒவ்வொரு bit-ஐ எதிர்மறையாக மாற்றுகிறது (1-ஐ 0 ஆகவும், 0-ஐ 1 ஆகவும்).

#### 13.4. left_shift
**left_shift** operator array-இன் bits-ஐ இடது பக்கம் நகர்த்துகிறது.

```python
# Left shift operation
a = np.array([0b0010])
result = np.left_shift(a, 2)
print("Left Shift:", result)
```

**Output:**

```

```

- **left_shift** operation array-இன் bits-ஐ குறிப்பிட்ட அளவிற்கு இடது பக்கம் நகர்த்துகிறது.

#### 13.5. right_shift
**right_shift** operator array-இன் bits-ஐ வலது பக்கம் நகர்த்துகிறது.

```python
# Right shift operation
a = np.array([0b1000])
result = np.right_shift(a, 2)
print("Right Shift:", result)
```

**Output:**

```

```

- **right_shift** operation array-இன் bits-ஐ குறிப்பிட்ட அளவிற்கு வலது பக்கம் நகர்த்துகிறது.

### 14. NUMPY − STRING FUNCTIONS

Numpy-ல் **string functions** பயன்படுவது arrays-இல் உள்ள string values-ஐ நேரடியாக manipulate செய்ய உதவுகிறது.

```python
# String functions example
string_array = np.array(['hello', 'world'])
upper_case = np.char.upper(string_array)
print("Uppercase Strings:", upper_case)
```

**Output:**

```

```

- **char.upper()** function string-ஐ uppercase-ஆக மாற்றுகிறது.

### 15. NUMPY − MATHEMATICAL FUNCTIONS

Numpy-ல் பல்வேறு **mathematical functions** உள்ளது, இது arrays-இல் கணித கணக்கீடுகளை எளிதாக செய்ய உதவுகிறது.

#### 15.1. Trigonometric Functions
Numpy-ல் **trigonometric functions** sin, cos, tan போன்றவற்றை எளிதாக கணக்கிட முடியும்.

```python
# Trigonometric functions
angles = np.array([0, np.pi/2, np.pi])
sine_values = np.sin(angles)
print("Sine Values:", sine_values)
```

**Output:**

```

```

- **sin()** function கொடுக்கப்பட்ட angles-இன் sine values-ஐ return செய்கிறது.

#### 15.2. Functions for Rounding
Numpy-ல் rounding operations-ஐ செய்ய பல functions உள்ளன, எடுத்துக்காட்டாக **round, floor, ceil**.

```python
# Rounding functions
float_array = np.array([1.2, 2.5, 3.8])
rounded_values = np.round(float_array)
print("Rounded Values:", rounded_values)
```

**Output:**

```

```

- **round()** function float values-ஐ nearest whole number-ஆக rounding செய்கிறது.

இந்த binary operators, string functions மற்றும் mathematical functions-அனைத்தும் data analysis மற்றும் numerical computing-ல் மிக முக்கியமானவை. Numpy-ஐ பயன்படுத்தி தரவுகளை எளிதாக manipulate செய்யலாம்.

### 16. NUMPY − ARITHMETIC OPERATIONS

Numpy-யில் **arithmetic operations** மிக எளிமையானவை, மற்றும் array-களின் values-ஐ நேரடியாக மாற்றிக்கொள்ள முடியும். இதனால் data analysis-ஐ வேகமாகவும் திறமையாகவும் செய்யலாம்.

#### 16.1. numpy.reciprocal()
**reciprocal()** function-ஐ பயன்படுத்தி array-இல் உள்ள values-ஐ reciprocal values-ஆக மாற்றலாம்.

```python
import numpy as np

# Reciprocal operation
array = np.array([1, 2, 4])
reciprocal_values = np.reciprocal(array)
print("Reciprocal values:", reciprocal_values)
```

**Output:**

```

```

- **reciprocal()** function ஒவ்வொரு element-ஐ reciprocal-ஆக மாற்றுகிறது (எ.கா., 1/x).

#### 16.2. numpy.power()
**power()** function-ஐ பயன்படுத்தி array-இல் உள்ள values-ஐ exponentiation செய்யலாம்.

```python
# Power operation
base = np.array([2, 3, 4])
exponent = np.array([2, 3, 2])
power_values = np.power(base, exponent)
print("Power values:", power_values)
```

**Output:**

```

```

- **power()** function base array-இன் values-ஐ exponent array-வுடன் power calculation செய்கிறது.

#### 16.3. numpy.mod()
**mod()** function-ஐ பயன்படுத்தி array-இல் உள்ள values-ஐ modulus operation செய்யலாம்.

```python
# Modulus operation
a = np.array([10, 20, 30])
b = np.array([3, 5, 7])
mod_values = np.mod(a, b)
print("Modulus values:", mod_values)
```

**Output:**

```

```

- **mod()** function இரண்டு arrays-இன் values-ஐ division operation செய்து, மீதி values-ஐ return செய்கிறது.

### 17. NUMPY − STATISTICAL FUNCTIONS

Numpy-யில் பல **statistical functions** உள்ளன, இது data-யை எளிதாக புள்ளிவிவரமாக பரிசோதிக்க உதவுகிறது.

#### 17.1. numpy.amin() and numpy.amax()
**amin()** மற்றும் **amax()** functions array-இல் உள்ள குறைந்த மற்றும் அதிகமான values-ஐ return செய்கிறது.

```python
# Finding min and max values
array = np.array([10, 20, 30, 40, 50])
min_value = np.amin(array)
max_value = np.amax(array)
print("Minimum value:", min_value)
print("Maximum value:", max_value)
```

**Output:**

```

```

- **amin()** array-இல் உள்ள குறைந்த value-ஐ return செய்கிறது.
- **amax()** array-இல் உள்ள அதிகமான value-ஐ return செய்கிறது.

#### 17.2. numpy.ptp()
**ptp()** function array-இன் maximum மற்றும் minimum values-இன் range-ஐ return செய்கிறது.

```python
# Range of values using ptp()
range_value = np.ptp(array)
print("Range (ptp):", range_value)
```

**Output:**

```

```

- **ptp()** function maximum value மற்றும் minimum value இடையே உள்ள difference-ஐ return செய்கிறது.

#### 17.3. numpy.percentile()
**percentile()** function array-இல் உள்ள values-இன் percentile-ஐ கண்டறிய உதவுகிறது.

```python
# Percentile calculation
percentile_value = np.percentile(array, 50)
print("50th Percentile:", percentile_value)
```

**Output:**

```

```

- **percentile()** function array-இல் உள்ள values-இன் குறிப்பிட்ட percentile-ஐ return செய்கிறது.

#### 17.4. numpy.median()
**median()** function array-இல் உள்ள values-இன் median value-ஐ return செய்கிறது.

```python
# Median calculation
median_value = np.median(array)
print("Median value:", median_value)
```

**Output:**

```

```

- **median()** function array-இன் center value-ஐ return செய்கிறது, values-ஐ arrange செய்த பிறகு.

#### 17.5. numpy.mean()
**mean()** function array-இல் உள்ள values-இன் arithmetic mean (average) value-ஐ return செய்கிறது.

```python
# Mean calculation
mean_value = np.mean(array)
print("Mean value:", mean_value)
```

**Output:**

```

```

- **mean()** function array-இல் உள்ள values-இன் average value-ஐ return செய்கிறது.

#### 17.6. numpy.average()
**average()** function-ஐ பயன்படுத்தி array-இல் உள்ள values-இன் weighted average value-ஐ கணக்கிடலாம்.

```python
# Weighted average calculation
weights = np.array([1, 2, 3, 4, 5])
weighted_average = np.average(array, weights=weights)
print("Weighted average:", weighted_average)
```

**Output:**

```

```

- **average()** function array values-இன் weighted average-ஐ கணக்கிடுகிறது.

#### 17.7. Standard Deviation
**std()** function array-இல் உள்ள values-இன் standard deviation-ஐ return செய்கிறது.

```python
# Standard deviation calculation
std_value = np.std(array)
print("Standard Deviation:", std_value)
```

**Output:**

```

```

- **std()** function array-இல் values-இன் standard deviation-ஐ return செய்கிறது, இது values எவ்வளவு விநியோகமாக இருக்கின்றன என்பதைக் காட்டுகிறது.

#### 17.8. Variance
**var()** function array-இல் உள்ள values-இன் variance-ஐ return செய்கிறது.

```python
# Variance calculation
variance_value = np.var(array)
print("Variance:", variance_value)
```

**Output:**

```

```

- **var()** function array-இல் values-இன் variance-ஐ return செய்கிறது, இது values எவ்வளவு பரவலாக இருக்கின்றன என்பதைக் காட்டுகிறது.

இந்த arithmetic மற்றும் statistical functions-ஐ பயன்படுத்தி Numpy array values-ஐ எளிதாக கணக்கிடவும், பரிசோதிக்கவும் முடியும், இது data analysis மற்றும் scientific computing-ல் மிகவும் பயனுள்ளதாக இருக்கும்.

### 18. NUMPY − SORT, SEARCH & COUNTING FUNCTIONS

Numpy-யில் **sort, search மற்றும் counting** functions-ஐ பயன்படுத்தி array-களின் values-ஐ வரிசைப்படுத்தவும், தேடவும் மற்றும் எண்ணிக்கையிடவும் முடியும். இவை data analysis மற்றும் manipulation-ல் மிகவும் பயன்படும்.

#### 18.1. numpy.sort()
**sort()** function array-இல் உள்ள values-ஐ ascending order-ல் வரிசைப்படுத்தும்.

```python
import numpy as np

# Array sort operation
array = np.array([5, 2, 8, 1, 9])
sorted_array = np.sort(array)
print("Sorted array:", sorted_array)
```

**Output:**

```

```

- **sort()** function array-இன் values-ஐ ascending order-ல் வரிசைப்படுத்துகிறது.

#### 18.2. numpy.argsort()
**argsort()** function array-இன் values-ஐ வரிசைப்படுத்துவதற்கான indices-ஐ return செய்கிறது.

```python
# Argsort operation
indices = np.argsort(array)
print("Indices of sorted array:", indices)
```

**Output:**

```

```

- **argsort()** function array-இல் values-ஐ வரிசைப்படுத்த indices-ஐ return செய்கிறது.

#### 18.3. numpy.lexsort()
**lexsort()** function ஒரு அல்லது அதற்கும் அதிகமான keys-இன் அடிப்படையில் data-ஐ வரிசைப்படுத்த உதவுகிறது.

```python
# Lexsort operation
names = ['banana', 'apple', 'cherry']
prices = [40, 10, 30]
sorted_indices = np.lexsort((prices, names))
print("Sorted indices based on names and prices:", sorted_indices)
```

**Output:**

```

```

- **lexsort()** function multiple keys-ஐ அடிப்படையாக கொண்டு data-ஐ வரிசைப்படுத்துகிறது.

#### 18.4. numpy.argmax() and numpy.argmin()
**argmax()** மற்றும் **argmin()** functions array-இல் உள்ள மிகப் பெரிய மற்றும் சிறிய values-ஐ அடையக்கூடிய indices-ஐ return செய்கின்றன.

```python
# Argmax and Argmin operations
max_index = np.argmax(array)
min_index = np.argmin(array)
print("Index of maximum value:", max_index)
print("Index of minimum value:", min_index)
```

**Output:**

```

```

- **argmax()** function மிகப் பெரிய value-ஐ கொண்ட இடத்தை return செய்கிறது.
- **argmin()** function மிகச் சிறிய value-ஐ கொண்ட இடத்தை return செய்கிறது.

#### 18.5. numpy.nonzero()
**nonzero()** function array-இல் 0 அல்லாத values-இருக்கும் இடங்களை return செய்கிறது.

```python
# Non-zero indices
nonzero_indices = np.nonzero(array)
print("Indices of non-zero elements:", nonzero_indices)
```

**Output:**

```

```

- **nonzero()** function array-இல் 0 அல்லாத values-இருக்கும் indices-ஐ return செய்கிறது.

#### 18.6. numpy.where()
**where()** function ஒரு condition அடிப்படையில் array-இல் values-இருக்கும் இடங்களை return செய்கிறது.

```python
# Where operation
condition_indices = np.where(array > 4)
print("Indices where values > 4:", condition_indices)
```

**Output:**

```

```

- **where()** function ஒரு condition அடிப்படையில் array-இல் values-ஐ கண்டறிய உதவுகிறது.

#### 18.7. numpy.extract()
**extract()** function ஒரு condition அடிப்படையில் array-இல் values-ஐ எடுத்துக் காட்டும்.

```python
# Extract operation
extracted_values = np.extract(array > 4, array)
print("Extracted values greater than 4:", extracted_values)
```

**Output:**

```

```

- **extract()** function condition அடிப்படையில் array-இல் values-ஐ return செய்கிறது.

### 19. NUMPY − BYTE SWAPPING

Numpy-ல் **byteswap()** function array-இன் byte-order-ஐ மாற்றுகிறது, இது big-endian மற்றும் little-endian format-களுக்குள் மாற்ற உதவுகிறது.

```python
# Byte swapping operation
array = np.array([1, 256, 8755], dtype=np.int16)
swapped_array = array.byteswap()
print("Byte swapped array:", swapped_array)
```

**Output:**

```

```

- **byteswap()** function array-இன் byte-order-ஐ மாற்ற உதவுகிறது.

### 20. NUMPY − COPIES & VIEWS

Numpy-ல் data-ஐ manage செய்வதற்கு மூன்று விதமான copies உள்ளன: **No Copy, View அல்லது Shallow Copy, Deep Copy**.

#### 20.1. No Copy
ஒரு array-ஐ மற்றொரு variable-க்கு assign செய்தால், அது original data-ஐ reference செய்து கொண்டிருக்கும். இதற்கு copy உருவாகாது.

```python
# No copy operation
array = np.array([1, 2, 3])
no_copy_array = array
no_copy_array[0] = 10
print("Original array after modification:", array)
```

**Output:**

```

```

- **No Copy**-இல், original array-ஐ மாற்றினால், modified array-யும் மாற்றம் அடையும்.

#### 20.2. View or Shallow Copy
**view()** method-ஐ பயன்படுத்தி ஒரு shallow copy உருவாக்கலாம், இது data-இல் உள்ள changes-ஐ reflect செய்யும்.

```python
# Shallow copy operation
view_array = array.view()
view_array[1] = 20
print("Original array after view modification:", array)
print("View array:", view_array)
```

**Output:**

```

```

- **Shallow Copy**-இல், view array-ஐ மாற்றினாலும், original array-யில் மாற்றங்கள் இருக்கும்.

#### 20.3. Deep Copy
**copy()** method-ஐ பயன்படுத்தி ஒரு deep copy உருவாக்கலாம், இது data-ஐ முழுமையாக independent-ஆக வைத்திருக்க உதவுகிறது.

```python
# Deep copy operation
deep_copy_array = array.copy()
deep_copy_array[2] = 30
print("Original array after deep copy modification:", array)
print("Deep copy array:", deep_copy_array)
```

**Output:**

```

```

- **Deep Copy**-இல், copy-ஐ மாற்றினாலும், original array-யில் எந்த மாற்றமும் நிகழாது.

இந்த sort, search, counting functions, byte swapping மற்றும் copies & views methods-அனைத்தும் Numpy array-களை organize செய்யவும், memory-யை திறமையாக பயன்படுத்தவும் மிகவும் பயனுள்ளதாக இருக்கும்.

### 21. NUMPY − MATRIX LIBRARY

Numpy-யில் **matrix library** என்பது matrix-களை உருவாக்கவும், நிர்வகிக்கவும் உதவும் functions-களை வழங்குகிறது. Numpy.matlib functions மூலம் நீங்கள் மாறிலி (matrix) operations செய்யலாம்.

#### 21.1. matlib.empty()
**matlib.empty()** function-ஐ பயன்படுத்தி, uninitialized values கொண்ட ஒரு matrix-ஐ உருவாக்கலாம். இது memory-யை சிக்கனமாக பயன்படுத்தி, values-ஐ முன்னதாக initialize செய்யாமல் matrix-ஐ உருவாக்குகிறது.

```python
import numpy.matlib as matlib

# Empty matrix உருவாக்கல்
empty_matrix = matlib.empty((2, 3))
print("Empty matrix:\n", empty_matrix)
```

**Output:**

```

```

- **matlib.empty()** function uninitialized values கொண்ட matrix-ஐ உருவாக்குகிறது.

#### 21.2. numpy.matlib.zeros()
**matlib.zeros()** function-ஐ பயன்படுத்தி, எல்லா elements-னும் zeros ஆக உள்ள ஒரு matrix-ஐ உருவாக்கலாம்.

```python
# Zeros matrix உருவாக்கல்
zeros_matrix = matlib.zeros((3, 3))
print("Zeros matrix:\n", zeros_matrix)
```

**Output:**

```

```

- **matlib.zeros()** function zeros கொண்ட matrix-ஐ உருவாக்குகிறது.

#### 21.3. numpy.matlib.ones()
**matlib.ones()** function-ஐ பயன்படுத்தி, எல்லா elements-னும் ones ஆக உள்ள ஒரு matrix-ஐ உருவாக்கலாம்.

```python
# Ones matrix உருவாக்கல்
ones_matrix = matlib.ones((2, 4))
print("Ones matrix:\n", ones_matrix)
```

**Output:**

```

```

- **matlib.ones()** function ones கொண்ட matrix-ஐ உருவாக்குகிறது.

#### 21.4. numpy.matlib.eye()
**matlib.eye()** function-ஐ பயன்படுத்தி, diagonal values-ல் ones மற்றும் மற்ற இடங்களில் zeros கொண்ட ஒரு identity matrix-ஐ உருவாக்கலாம்.

```python
# Eye matrix (identity matrix) உருவாக்கல்
eye_matrix = matlib.eye(n=3, M=4, k=0, dtype=int)
print("Eye matrix:\n", eye_matrix)
```

**Output:**

```

```

- **matlib.eye()** function diagonal-ல் ones மற்றும் மற்ற இடங்களில் zeros கொண்ட identity matrix-ஐ உருவாக்குகிறது.

#### 21.5. numpy.matlib.identity()
**matlib.identity()** function square matrix-ஐ உருவாக்குவதற்காக பயன்படுத்தப்படுகிறது, diagonal-ல் மட்டும் ones values-ஐ கொண்டு.

```python
# Identity matrix உருவாக்கல்
identity_matrix = matlib.identity(4, dtype=float)
print("Identity matrix:\n", identity_matrix)
```

**Output:**

```

```

- **matlib.identity()** function square identity matrix-ஐ diagonal-ல் ones values-ஐ கொண்டு உருவாக்குகிறது.

#### 21.6. numpy.matlib.rand()
**matlib.rand()** function-ஐ பயன்படுத்தி, uniform distribution அடிப்படையில் random values கொண்ட ஒரு matrix-ஐ உருவாக்கலாம்.

```python
# Random matrix உருவாக்கல்
random_matrix = matlib.rand(3, 3)
print("Random matrix:\n", random_matrix)
```

**Output:**

```

```

- **matlib.rand()** function random values கொண்ட matrix-ஐ uniform distribution அடிப்படையில் உருவாக்குகிறது.

இந்த Numpy-யின் matrix library functions-கள் scientific computing மற்றும் data analysis-ல் matrix-களை எளிமையாக உருவாக்கவும், manipulate செய்யவும் மிகவும் பயனுள்ளதாக இருக்கும்.

### 22. NUMPY − LINEAR ALGEBRA

Numpy-யில் **linear algebra** operations செய்ய பல முக்கியமான functions உள்ளன, இது matrix multiplication, inner products, determinants, மற்றும் equations-ஐ solve செய்ய உதவுகின்றது.

#### 22.1. numpy.dot()
**dot()** function-ஐ பயன்படுத்தி, இரண்டு arrays-இன் dot product-ஐ கணக்கிடலாம்.

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

```

- **dot()** function இரண்டு arrays-இன் dot product-ஐ return செய்கிறது.

#### 22.2. numpy.vdot()
**vdot()** function-ஐ பயன்படுத்தி, flattened arrays-இன் dot product-ஐ கணக்கிடலாம்.

```python
# Vdot product operation
vdot_product = np.vdot(a, b)
print("Vdot product:", vdot_product)
```

**Output:**

```

```

- **vdot()** function flattened arrays-இன் dot product-ஐ return செய்கிறது.

#### 22.3. numpy.inner()
**inner()** function-ஐ பயன்படுத்தி, arrays-இன் inner product-ஐ கண்டறியலாம்.

```python
# Inner product operation
inner_product = np.inner(a, b)
print("Inner product:", inner_product)
```

**Output:**

```

```

- **inner()** function இரண்டு vectors-இன் inner product-ஐ return செய்கிறது.

#### 22.4. numpy.matmul()
**matmul()** function-ஐ matrix multiplication செய்ய பயன்படுத்தலாம்.

```python
# Matrix multiplication operation
matrix1 = np.array([[1, 2], [3, 4]])
matrix2 = np.array([[5, 6], [7, 8]])
matrix_product = np.matmul(matrix1, matrix2)
print("Matrix product:\n", matrix_product)
```

**Output:**

```

```

- **matmul()** function matrix multiplication செய்ய பயன்படுத்தப்படுகிறது.

#### 22.5. Determinant
Numpy-யின் **det()** function-ஐ பயன்படுத்தி, square matrix-இன் determinant-ஐ கணக்கிடலாம்.

```python
# Determinant calculation
det_value = np.linalg.det(matrix1)
print("Determinant:", det_value)
```

**Output:**

```

```

- **det()** function square matrix-இன் determinant value-ஐ return செய்கிறது.

#### 22.6. numpy.linalg.solve()
**solve()** function-ஐ பயன்படுத்தி, linear equations-இன் solution-ஐ கண்டறியலாம்.

```python
# Solving linear equations
coefficients = np.array([[3, 1], [1, 2]])
constants = np.array([9, 8])
solutions = np.linalg.solve(coefficients, constants)
print("Solutions:", solutions)
```

**Output:**

```

```

- **solve()** function linear equations-இன் solutions-ஐ கண்டறிய உதவுகிறது.

### 23. NUMPY − MATPLOTLIB

Numpy-யுடன் **Matplotlib**-ஐ பயன்படுத்தி data-ஐ visualizations செய்வது மிகவும் எளிமையானது. இது plotting graphs மற்றும் data visualization-ஐ அடிப்படையாக கொண்டது.

#### 23.1. Sine Wave Plot
Sine wave plot-ஐ உருவாக்கி data-ஐ visualize செய்யலாம்.

```python
import matplotlib.pyplot as plt
import numpy as np

# Sine wave plot
x = np.linspace(0, 10, 100)
y = np.sin(x)
plt.plot(x, y)
plt.title("Sine Wave")
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.show()
```

**Output:**

```

```

- **Sine wave plot** data-ஐ visualize செய்ய ஒரு graph-ஐ உருவாக்குகிறது.

#### 23.2. subplot()
**subplot()** function-ஐ பயன்படுத்தி ஒரே figure-இல் பல plots-ஐ உருவாக்கலாம்.

```python
# Subplots creation
plt.subplot(2, 1, 1)
plt.plot(x, np.sin(x))
plt.subplot(2, 1, 2)
plt.plot(x, np.cos(x))
plt.show()
```

**Output:**

```

```

- **subplot()** function ஒரே figure-இல் multiple plots-ஐ உருவாக்க உதவுகிறது.

#### 23.3. bar()
**bar()** function-ஐ data-ஐ bar chart-ஆக plot செய்ய பயன்படுத்தலாம்.

```python
# Bar chart creation
categories = ['A', 'B', 'C']
values = [3, 7, 5]
plt.bar(categories, values)
plt.title("Bar Chart")
plt.show()
```

**Output:**

```

```

- **bar()** function data-ஐ bar chart-ஆக visualize செய்ய உதவுகிறது.

### 24. NUMPY – HISTOGRAM USING MATPLOTLIB

Numpy-யுடன் **Matplotlib**-ஐ histogram உருவாக்க data distribution-ஐ காணலாம்.

#### 24.1. numpy.histogram()
**histogram()** function array-இன் data distribution-ஐ கண்டறிய உதவுகிறது.

```python
# Histogram creation
data = np.random.randn(1000)
plt.hist(data, bins=30, alpha=0.7, color='blue')
plt.title("Histogram")
plt.show()
```

**Output:**

```

```

- **histogram()** function data-இன் frequency distribution-ஐ bar chart வடிவில் காட்டுகிறது.

### 25. NUMPY − I/O WITH NUMPY

Numpy-யில் data-ஐ save மற்றும் load செய்ய பல functions உள்ளன. இதன் மூலம் data-ஐ எளிதாக file format-ல் சேமிக்கலாம்.

#### 25.1. numpy.save()
**save()** function-ஐ array-ஐ binary format-ல் (.npy) சேமிக்க பயன்படுத்தலாம்.

```python
# Saving array to file
array = np.array([1, 2, 3, 4, 5])
np.save('my_array', array)
```

**Output:**

```

```

- **save()** function array-ஐ binary file format-ல் சேமிக்கிறது.

#### 25.2. savetxt()
**savetxt()** function-ஐ text file format-ல் array-ஐ சேமிக்க பயன்படுத்தலாம்.

```python
# Saving array to text file
np.savetxt('my_array.txt', array, delimiter=',')
```

**Output:**

```

```

- **savetxt()** function array-ஐ text file format-ல் (.txt) சேமிக்க உதவுகிறது.

இந்த functions அனைத்தும் data-ஐ manage செய்யவும், visualize செய்யவும் மற்றும் store செய்யவும் Numpy-யுடன் சேர்ந்து மிக முக்கியமானவையாகும்.
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
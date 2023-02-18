# Notes for programming in Python

## None vs np.nan
How to detect `None` and `np.nan` in a numpy array?
```Python
# datatype
A = np.array([1, 4, None])   # dtype = Object
B = np.array([1, 4, np.nan]) # dtype = float

# Option 1: equal to itself
print(A != A) # False for None
print(B != B) # True for np.nan

# Option 2: equal to None
print(A == None) # True for None
print(B == None) # False for np.nan

# Option 3: np.isnan
print(np.isnan(A)) # Error for None
print(np.isnan(B)) # True for np.nan

# Option 4: greater than 0
print(A >= 0) # Error for None
print(B >= 0) # False for np.nan

# Option 5: convert to int
A.astype(int) # Error
B.astype(int) # -9223372036854775808
```

In summary, `None` and `np.nan` are very different in detection. If you know which is used, you can choose the effective way.
If you don't know which is used, you may consider using both `Option 1` & `Option 2`, without causing errors.

If you want to use `NA` value, `None` might be safer given it will raise an error if not used properly (just my own opinion).

Author: Dilan Fernando
Email: dilan.fd@gmail.com

# Coding tips and tricks in Machine Learning and Deep Learning.

### This is a growing list...
    
If you have any tips and tricks to share send me a pull request. I will add it 
to the list and give you the credit.
	
	
1. Avoid for loop and vectorize your code as much as you can.
   With a bit of Linear algebra most for loops in ML/DL can be vectorized.
   -Example:
		... TODO: Write example
		
2. Avoid 1D `numpy.arrays`. If you are dealing with a row vector explicitely
   make the dimension match that of the desired vector. Arrays of type 
   `(n,)` are bad for vectorization and will give unexpected erros and nasty
   bugs.
   -Example (Suppose you're looking for a 1 x 3 row vector):
	   
	   ```python
	   import numpy as np
	   
	   a = np.array([1,2,3])
	   a.shape = (1, 3)
	   ```
	   
3. Use `assert` statements to insist `type` and `shape` etc. `assert` has
   constant time complexity and so it is cheap. Use it.
   - Example.
	 ```python
	 assert (isinstance(num, float))
	 
	 assert matrix.shape == (m , n)
	 ```

3. Use python broadcasting to your advantage.
   - Example:
	 ...
 
 4. When using `numpy.sum` use the `axis=1` sums over the rows.
	`axis=0` sums over the columns. 
	
5. When using `numpy.sum` use the `keepdims=True` to keep the
   desired dimensions after the summation.
 
6. use `numpy.multiply` for elementwise multiplication of matrices
   or vectors.

#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) This code is quadratic--O(n^2)--because the value that `a` has to reach is
   multiplied by `n` each time. Therefore, it will take much longer for the
   while loop to finish with a larger `n`.


b) This code is linearithmic--O(n*Log n)--because it contains a logarithmic loop
   within a linear loop. `for i in range(n)` runs `n` times, making it O(n).
   `while j < n` runs 1/2`n` times, making the number of times it runs increase
   at a slower rate as `n` increases, making it O(Log n). A logarithmic loop
   within a linear loop is linearithmic.


c) This function is linear--O(n)--because it will always run `n+1` times. The
   number of times that it runs will increase at a steady rate as `n` increases.

## Exercise II
```python
f = ?

def is_egg_broken(floor):
  if floor >= f:
    return true
  else:
    return false

def egg_toss(n):
  max_floor = n
  min_floor = 0
  current_floor = n // 2
  while max_floor > min_floor:
    if is_egg_broken(current_floor):
      max_floor = current_floor
      current_floor = min_floor + (max_floor - min_floor)//2
    else:
      min_floor = current_floor
      current_floor = min_floor + (max_floor - min_floor)//2
  return current_floor
```
This is a binary search. As such, it is logarithmic--O(Log n)--complexity

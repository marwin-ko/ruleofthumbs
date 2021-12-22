# ruleofthumbs


## Software Engineering
- Never set input argument as instance of data type and use that data type as the return.
  - This can result in all elements pointing to the same "last value" used in the function.
  - It can also result in recursion hell depending on your implementation the function.
      ```def test(x,y=list()):
          y.append(x)
          return(y)
      z = []
      for i in range(3):
          x = test(i)
          z.append((x))
      print(z)```

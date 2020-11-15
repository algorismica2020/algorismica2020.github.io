```python
a =  "abcd"
def cadena(a):
  l = len(a)
  while l >= 1:
    for j in range(0,len(a)+1-l):
      print(a[j:l+j])
    l -= 1
   
cadena(a)
>>> abcd
>>> abc
>>> bcd
>>> ab
>>> bc
>>> cd
>>> a
>>> b
>>> c
>>> d

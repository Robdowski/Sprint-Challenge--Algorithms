#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a)
O(n ^ 2)

b)
O(n log n) .. Reason why I gave this rating is because first loop is O(n).. Second loop is O(log n)

c)
O(n)..  this one doesn't seem to scale with a higher input

```python
a)  a = 0
    while (a < n * n * n):
      a = a + n * n
```


```
b)  sum = 0
    for i in range(n):
      j = 1
      while j < n:
        j *= 2
        sum += 1
```

```
c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)
```

## Exercise II

## I am assuming that the top floor will most likely break the egg in most cases, and that the bottom floor will almost always not break the egg.

## I would write a recursive solution that will split the height of the building in half and drop the egg from the midpoint. If the egg breaks, use the lower half of the building and split it in half again. If the egg does not break, use the higher split of the building and drop it from the halfway point on the higher split. Repeat until I have the highest floor upon which the egg does not break. 

## I think that this would run in O(log n) time, because with higher inputs, it could find the breakpoint faster than checking n each time.

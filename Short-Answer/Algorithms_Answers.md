#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a)
O(n) the algorithm runs until a >= n^3. But as a increases with n^2 with every step the runtime is n^3/n^2 = n

 

b)

O(n log n)

the outer loop runs n times. The inner loop runs log n times since the counter j gets doubled with every step. 

c)

O(n)

the function calls itself recursively n times. The constants can be ignored.

## Exercise II

Since an egg that breaks on floor x will also break on any floor above we can 
consider the house to be a sorted array. Then we can apply binary searhc to it 
which will run with O(log n) time complexity. 

The procedure would look like this:

0. We drop the egg in the middle of the building. 

1. If it breaks we are too high, so we find a new middle point between the current middle and the ground and drop the egg another time. 

2. If it does not break we might be too low so we find a new middle point between the current middle and the top of the building and drop the egg another time etc.

3. We will continue with this until we find a spot where the egg does not break while it did break one floor above. 

4. then we return the floor where it did not break. 


To give an example. Say our house has 10 floors: 1 to 10:

We drop the egg in the middle so on floor 5. It breaks, which means we are too high.

So we find a new middle which is floor 2. Here it does not break. So now we know that the floor we are looking for is either 2, 3 or 4.

We find a new middle which is floor 3. Here the egg breaks and therefore we can conclude that the floor we are looking for is floor 2. 









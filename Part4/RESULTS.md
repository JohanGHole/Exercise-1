## GO Result

First iteration: the magic number is: -956069. After running the program several times, we see that the "magic" value differs significantly.
We see that removing the runtime.GOMAXPROCS function does not have an apparent effect on our program.  
By adding a small delay between the goroutines, we get the desired magic number 0, but this in turn makes the program nonconcurrent. 

## C result

We see that the result differs significantly here also, but sometimes we get the expected value (0).

## Python result

The results differ between 1000000 and 999998.

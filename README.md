# Mage2 Module Genaker Profiler

MAgento profiling profiling is the analysis of various metrics related to code performance and efficiency.

If a Magento Layout Block is taking too much time to complete, it’s a good idea to profile the block to find out the cause.

A very easy and straightforward way to perform this analysis is to use the time() and microtime() functions.

Both these functions return the current Unix Timestamp. time() returns it in seconds, while microtime() returns a float with microseconds too.

To check the execution time of a piece of code you need to:

Save the current time with time() or with microtime() before the code you want to profile.
After the code, call time() or microtime() again and calculate the difference from the previously saved value.
That is the execution time in seconds

# Install composer 

```
composer require genaker/profiler
```

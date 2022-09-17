# Code Optimization (C++)

### An optimized and improved version of a C++ histogram filter program for localization.

This program runs each of the histogram filter functions ten-thousand times and then prints out the time taken to run each function. This compares the execution speeds between `original` vs. `optimized` code.

This workspace contains two folders:
- Original: Histogram filter code translated from Python into C++ as seen in this [repository](https://github.com/jacobsayono/robot-localization). 
- Optimized: This folder also contains Andy's Histogram filter code. You will optimize the code in these files to see how fast you can get main.cpp to run.

There are eight C++ files and seven header files. Each file other than main.cpp contains a function that carries out a specific part of a histogram filter. I have separated each function into its own unique file name.

`main.cpp` - prints out how long it takes to run each function

`initialize_beliefs.cpp` - converts a 2D char vector to a 2D float vector containing initial probabilities

`sense.cpp` - the robot senses the color of the current grid point and calculates the resulting beliefs

`blur.cpp` - blur the resulting 2D vector

`normalize.cpp` - normalize the results to represent a probability

`move.cpp` - move the robot by (x,y) and calculate the new beliefs

`zeros.cpp` - outputs a 2D vector with zero for all elements

`print.cpp` - contains two different functions for printing out a 2D vector. 

### main.cpp starts off with a 2D char vector representing a discrete color grid. Then the code: 
- initializes the belief matrix
- senses the color grid
- blurs the results
- normalizes the results to calculate probabilities
- moves the robot

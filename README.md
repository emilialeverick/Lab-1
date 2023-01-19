#Lab-1
#Introduction to Python and Github

%matplotlib inline
import numpy as np
from sklearn import datasets
import matplotlib.pyplot as plt

#(1) Write a function that stores the first 1000 numbers of the Fibonacci sequence in a numpy array.
#Then write two assertions as tests of your function.
def fibonacci_sequence(n):
    sequence = np.empty(n)   #initiate a placeholder empty array
    sequence[0] = 0 sequence[1] = 1
    for i in range(2, n):
        sequence[i] = sequence[i-1] + sequence[i-2]
    return sequence

#testing assertions
def test_fibonacci_sequence():
    sequence = fibonacci_sequence(1000)
    assert sequence[1] == 1
    assert sequence[-5] == sequence[994] + sequence[993]


[fibonacci_of(n) for n in range(20)]

#(2) Plot the data that is imported below, labeling the X and Y axes.

boston = datasets.load_boston()
y = boston.target
x = boston.data[:, 0]
plt.ylabel = "Home Prices"
plt.xlabel = "Crime"
plt.plot(x, y)
plt.title('Home Prices Vs. Crime')
plt.show()


#(3) Write a function that satisfies the assertions below.
#The function can just multiply each of the number pairs together for the assertions to hold true.
def func(a, b):
    return a*b

assert(func(0, 20) == 0)
assert(func(1, 10) == 10)
assert(func(2, 5) == 10)
assert(func(3, 2) == 6)
assert(func(4, 1) == 4)

#(4) Briefly describe one skill and/or ability you would like to take away from this class.
#I would like to become more proficient in Python.

#(5) Describe your previous experience with programming, statistics, and modeling, including courses and which languages you've used. There is no wrong answer here—this will help us better tailor the class.
#I took a MatLab course last summer. I also have some experience with Python since I had to learn some of it for a research internship at UCI this past summer. 

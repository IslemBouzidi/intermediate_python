# Welcome to counters in python


``` python
####################                             Counters in python                              ####################

from collections import Counter

# Example with a list of integers
list_of_int = [1, 3, 5, 8, 9, 8, 8]
c = Counter(list_of_int)
print(c)  # Counter({8: 3, 1: 1, 3: 1, 5: 1, 9: 1})

# Example with a string
c1 = Counter("data science")
print(c1)  # Counter({'a': 2, 'c': 2, 'e': 2, 'd': 1, 't': 1, ' ': 1, 's': 1, 'i': 1, 'n': 1})

# Example with keyword arguments
c2 = Counter(sunny_Days=4, claudy_days=2)
print(c2)  # Counter({'sunny_Days': 4, 'claudy_days': 2})
print(c2['sunny_Days'])  # 4

# Accessing a key that doesn't exist
print(c['partly_cloudy'])  # 0

# Listing elements
c3 = Counter("Data")
print(list(c2.elements()))

# Most common elements
print(c1.most_common(2))  # [('a', 2), ('c', 2)]

# Subtracting two counters
c1.subtract(c3)
print(c1)  # Counter({'c': 2, 'e': 2, 'd': 0, ' ': 0, 's': 0, 'i': 0, 'n': 0, 'a': 1, 't': 1, 'D': -1})

# Updating by adding two counters
c1.update(c3)
print(c1)  # Counter({'a': 2, 'c': 2, 'e': 2, 'd': 1, 't': 1, ' ': 1, 's': 1, 'i': 1, 'n': 1, 'D': 0})

# Clearing a counter
c.clear()
print(c)  # Counter()

# Counting unique elements
print(len(c2))  # 2

# Combining counters using addition
combined_counter = c1 + c2
print(combined_counter)  # Counter({'a': 2, 'c': 2, 'e': 2, 'd': 1, 't': 1, ' ': 1, 's': 1, 'i': 1, 'n': 1, 'D': 0, 'sunny_Days': 4, 'claudy_days': 2})

# Retrieving the minimum and maximum elements
print(min(combined_counter))  # ' '
print(max(combined_counter))  # 's'

# Checking if two counters are equal
c4 = Counter("example")
c5 = Counter("example")
print(c4 == c5)  # True

```

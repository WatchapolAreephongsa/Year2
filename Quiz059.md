```py
from colorama import Fore, Back, Style
class time: #class to create square grid of numbers
    def __init__(self,n,z):
        self.n = n #attribute for the total number



    def grid(self):
        for i in range(self.n//5): # loop for the number of row as there will be 5 columns per row
            row = ""   # empty string for each row
            for k in range(5): # add number to each column (5 columns in each row)
                row += str((k+1)+(i*5)).center(5) #add the number into the row variable and use center to make the distance between each number equal
            print(row) # print row




t = time(25) # testing
t.grid()

```

# Test

<img width="866" alt="q59" src="https://user-images.githubusercontent.com/82266864/194757555-948e7a88-8296-4f9c-af5c-b608fc94870b.png">

## Code
```py
class reverse:
    def __init__(self,row,symbol): #define attributes in initializer
        self.row =row #attribute for number of rows
        self.symbol = symbol # attribute for the symbol
    #symbol
    def create(self): #method to create the symbol in each row
        for i in range(self.row): #loop for the number of row
            print(" "*i + self.symbol) #same amount space as the number of row and with symbol after

test1 = reverse(5,"-")
test2 = reverse(3,"+")
test3 = reverse(4,"$")
print("Test 1")
test1.create()
print("Test 2")
test2.create()
print("Test 3")
test3.create()


```


## Test
<img width="857" alt="Quiz65" src="https://user-images.githubusercontent.com/82266864/200314354-52ce9caa-f497-48d6-a417-64a7420c9d5f.png">

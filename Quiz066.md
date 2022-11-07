## Code
```py
class square:
    def __init__(self,length):
        self.length = length # attribute for length of square

    def plussquare(self): #create square of plus with each side has inputted numbers of +
        for i in range(self.length): #loop to create self.length rows
            print(("+"*self.length))#print the same amount of + as number of row in each row to create square

print("Test1")
test1 =square(3)
test1.plussquare()
print("Test2")
test2 =square(5)
test2.plussquare()
print("Test3")
test3 = square(10)
test3.plussquare()
```

## Test

<img width="835" alt="quiz66" src="https://user-images.githubusercontent.com/82266864/200316158-a5f6000e-8e33-4809-bb5f-f6f171fa213f.png">

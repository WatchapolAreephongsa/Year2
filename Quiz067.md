## Code
```py

class connect:
    def __init__(self,num1,num2): #attributes
        self.num1 = num1 #first number
        self.num2 = num2 #second number
    def concatenate(self): #method to concatenate the different and sum of the two numbers
        return str(abs(self.num1-self.num2))+str(self.num1+self.num2)
test1 = connect(6,4)
test2 = connect(5,9)
test3 = connect(1000,1)
test4 = connect(100,100)
print(test1.concatenate())#expect 210
print(test2.concatenate())#expect 414
print(test3.concatenate())#expect 9991001
print(test4.concatenate()) #expect 0100
```

## Test
<img width="738" alt="quiz67" src="https://user-images.githubusercontent.com/82266864/200317606-269b5242-9378-402a-b365-11c72c311d55.png">

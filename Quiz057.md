```py
class converter: #class that input decimal number and convert to the inputted base
    def __init__(self,number,base): # attributes for the class
        self.number = number
        self.base = base

    def build(self): #converting
        letter = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
        if self.base<37: # if base cannot be presented by number or letter(base more than 37) or not

                output = "" #create empty string for output
                while self.number!=0: # while the number is not 0
                    remainder = self.number%self.base # find remainder after dividing number by base
                    if remainder>9: #if the remainder more than 9
                        remainder = letter[remainder-10] #the remainder will be subtracted by 10 and will be used to get the letter from that index from letter variable
                    output += str(remainder)# add remainder to output
                    self.number = self.number//self.base #make number equal number divide by base without remainder
                return output[::-1] # reverse the output so the first remainder will be the first in the output
        else: # if base more than 36 output base off limit
            return "base off limit"


#testing
test1 = converter(10,16)
test2 = converter(10987,20)
test3 = converter(10987,36)
print(test1.build())
print(test2.build())
print(test3.build())

```

# Test

<img width="1368" alt="57" src="https://user-images.githubusercontent.com/82266864/194761521-1e893d32-0d10-46a7-b83f-b8ef9b9f03e6.png">


# Python
```py

class converter: #create class to convert the decimal number(for ip) less than 256 to binary
    def __init__(self,num):
        self.num = num #attribute for number
    def binirize(self): #converting method
        if self.num<=255: # check if number is less than 256
            binary = "" #create empty string for binary
            for i in range (8):
                n = 7-i #set n which will be the power of 2 in the divider
                binary += str((self.num//2**n)%2) #divide the number by 2 to the power of n and put remainder into binary
            return binary

        else:
            return "number over limit" #return number over limit for number more than 255

n = converter(10)
print(n.binirize())

```

# Java

```js

class converter{
    constructor(num) {
        this.num = num
    }
    binirize(){
        if (this.num<=255){
            let binary ="";
            for (let i =0; i<8;i++){
                let n = 7-i;
                let divider = Math.pow(2,n);
                binary += str(Math.floor(self.num/divider)%2)
            }
            return binary
        }
        else{
             return "Number over limit"
        }
    }
}

n = converter(10)
n.binirize()

```


# Test
<img width="1440" alt="quiz51 result" src="https://user-images.githubusercontent.com/82266864/187098847-93146836-f079-493a-abbd-769466db1134.png">



# Python
```py

class converter:
    def __init__(self,num):
        self.num = num
    def binirize(self):
        if self.num<=255:
            binary = ""
            for i in range (8):
                n = 7-i
                binary += str((self.num//2**n)%2)
            return binary

        else:
            return "number over limit"

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


# 70(a)
## Code 

```py
def truth_table(equation):
    print("|A|B|C|not B+C|") #print the first line which are the columns titles and equation
    for i in range(8): #repeat 8 times as there are 3 binary number spots which can represent 8 decimal from 0-7
        binary = bin(i)[2:] #convert the number of iteration to binary
        while len(binary)<3: #and make that binary number 3 digits by adding 0 in front when the binary is not 3 digits yet using while loop
            binary = "0"+binary

        A, B,C = binary[0]=="1",binary[1]=="1",binary[2]=="1" #convert integer to boolean
        result = int(not B or C) #solve equation and convert back to integer

        print(f"|{binary[0]}|{binary[1]}|{binary[2]}|",end="")
        print(f"{result}".center(7),end="") #print with space
        print("|")

truth_table("not B+C") #activate function
```

## Test

<img width="892" alt="test q70" src="https://user-images.githubusercontent.com/82266864/200971554-ebe94541-f8bc-4925-8d8b-cd02130fdb60.png">

# 70(b)

![IMG_C9BB0BD40D2D-1](https://user-images.githubusercontent.com/82266864/200971637-a576eb83-9503-40b0-b81e-86940434a310.jpeg)

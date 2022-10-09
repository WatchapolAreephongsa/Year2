```py
class timetrial:
    def __init__(self,n): # attributes
        self.n = n

    def color(self): # method to create grid
        color = ["red","blue","green","black"] #create list of color
        for i in range(self.n // 5): #calculate number of row
            for k in range(5):
                row = color[((k) + (i * 5))%4] # set the row to be the number of object of the row from 1 to 5

                #print the text with the corresponding color using if statement
                if row == "red":
                    print(f"\33[0;31m{row}\033[0m",end=' ') #make it in same row with end command
                if row == "blue":
                    print(f"\33[0;34m{row}\033[0m",end=' ')
                if row == "green":
                    print(f"\33[0;32m{row}\033[0m",end=' ')
                if row == "black":
                    print(f"\33[0;30m{row}\033[0m",end=' ')
            print() #move to new row

test = timetrial(25) # create 5*5 grid
test.color()
```
# Test

<img width="1440" alt="060" src="https://user-images.githubusercontent.com/82266864/194755156-b51ff5fb-9aff-4119-851e-56547a4f2a56.png">

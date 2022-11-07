## Code
```py
class mars:
    def __init__(self,distance,time,velocity,fuel,fuel_consumption):
        self.distance = distance #distance to mars
        self.time = time #time takes to got to mars
        self.velocity = velocity #distance travel per unit of time
        self.fuel = fuel #distance per fuel consumption
        self.fuel_consumption =fuel_consumption #per time unit
    def travel(self): #check status what will happen if goes to mar with this rocket details
        condition1 =self.velocity*self.time<self.distance #fail if velocity times time is less than distance
        condition2 = self.fuel*self.fuel_consumption<self.distance #if fuel not enough
        if condition1:
            return("Failure, Not enough time.") # if not enough time or not enough time and fuel print not enough time only
        if condition2 and not condition1:
            return("Failure, Not enough fuel.") # not enough fuel only
        if not condition1 and not condition2:
            return("Welcome to Mars!") # success

test1 = mars(1000,50,10,50,30) #expect not enough time
print("Test 1 : " + test1.travel())
test2 = mars(10000,1,1,1,1) # both not enough,so expect not enough time
print("Test 2 : " + test2.travel())
test3=mars(40,4,12,12,3) #expect not enough fuel
print("Test 3 : " + test3.travel())
test4 = mars(2000,400,55,900,3) # expect Welcome to Mars
print("Test 4 : " + test4.travel())
```

## Test
<img width="761" alt="quiz68" src="https://user-images.githubusercontent.com/82266864/200320517-1a3894c1-74fb-4b80-96a6-b75283eb02ef.png">

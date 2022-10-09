```py
class open_doors:
    '''
     create class to make student open and close the door that is the number is divisible by the number of that student
    '''
    def __init__(self,num_students):
        self.num_students = num_students #attributes
    def count_open(self): # method to count numbers of open door
        door = [] # list for all door
        for i in range(self.num_students):
            door.append(False) # Make all door close or false
        for j in range(1,self.num_students+1): #create new for loop to flip the door for each student
            for k in range(1,self.num_students+1): # check if the number of door is divisible by the number of that student
                if k%j == 0:
                    door[k-1] = not door[k-1] #use not door to flip the door that is divisible
        count_open = 0 # set the number of open door to 0
        for l in door: #read the information in the door list
            if l == True: # true mean open, so it will add 1 to number of open door
                count_open +=1
        return f"\33[0;34m{count_open}\033[0m" # return total numbers of open doors with color


test = open_doors(10)
print(test.count_open())
test2 = open_doors(100)
print(test2.count_open())
test3 = open_doors(5390)
print(test3.count_open())
test4 = open_doors(3)
print(test4.count_open())

```


# Test

<img width="826" alt="63" src="https://user-images.githubusercontent.com/82266864/194755031-cd335bb1-75ae-48f5-a663-059fe87cc32c.png">

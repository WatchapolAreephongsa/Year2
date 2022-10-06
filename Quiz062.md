```py

class stack: # class to create stack
    def __init__(self):
        self.stack = [] # set stack as list

    def pop(self):# take last one out
        output = self.stack[-1]
        self.stack = self.stack[:-1]
        return output

    def push(self,new):# insert
        self.stack.append(new) # append new element to stack

    def empty(self):
       return(len(self.stack) == 0)
    
    def __repr__(self): # print out the stack 
        output = ""
        for i in self.stack:
            output += i
        return output



class adder:
    def __init__(self,text):
        self.text = text #set attribute
    def sum(self):
        result = 0 # initial result will be 0 

        while self.text.empty()== False:#check that the stack is not empty
            letter = self.text.pop() # take the last element out
            if letter != " ": # check that the letter selected is not space
                result += ord(letter.lower()) - 96 
                '''
                convert the letter to lower case and compare with its ASCII number, then convert to number of alphabet 
                and add in the result variable
                '''
        return result # return the result

text1 = stack() #set text to be the stack class
for i in "Math":
    text1.push(i) # push each character into the stack 

text2 = stack()
for i in "maTH":
    text2.push(i)
text3 = stack()
for i in "Hello world":
    text3.push(i)
text4 = stack()
for i in "Computer SCIENCE":
    text4.push(i)

# testing
test = adder(text1)
print(test.sum())
test2 = adder(text2)
print(test2.sum())
test3 = adder(text3)
print(test3.sum())
test4 = adder(text4)
print(test4.sum())


<img width="957" alt="62 RESULT" src="https://user-images.githubusercontent.com/82266864/194219881-a258e210-a7d8-4b8c-84a2-f30d796b8d24.png">

```

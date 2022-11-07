## Code 

```py
class reverse_sentence:
    def __init__(self,sentence):
        self.sentence = sentence
    #Method to reverse the phase/sentence
    def reversing(self):
        return " ".join(self.sentence.split(" ")[::-1]) #split the string at the space to list and reverse it before joining it back and return it

test1 = reverse_sentence("Hello World!")
print( "Test 1: "+test1.reversing()) #expect: World! Hello
test2 = reverse_sentence("Computer Science")
print("Test 2: " +test2.reversing())#expect: Science Computer
test3 = reverse_sentence("Computer Science IA is going to due today.") #expect: today. due to going is IA Science Computer
print("Test 3:" +test3.reversing())
```

## Test
<img width="813" alt="quiz69" src="https://user-images.githubusercontent.com/82266864/200321998-b582f1ba-95f9-486f-9e29-291686ad06e7.png">

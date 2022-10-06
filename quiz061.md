```py
#function that replace vowels with number in the order of a ,i ,u, e and o
def vowels(msg:str):
    x = ["a","i","u","e","o"] # list to create order for vowels
    output = "" #empty list for result
    for letter in msg: #loop for all letter
        if letter in x: # if the letter is in the list for vowel
            output+=str(x.index(letter)+1) #find the index in list x and replace it in the message
        else:
            output+= letter# if not vowel, the original character will be added
    return output # return the output


print(vowels("foxie"))
print(vowels("ComSci"))
print(vowels("aeiou"))
print(vowels("aiueo"))
```

# Result

<img width="871" alt="resyk61" src="https://user-images.githubusercontent.com/82266864/194221433-1dc2eac1-d254-4f9d-9d66-4a81ef9dee25.png">

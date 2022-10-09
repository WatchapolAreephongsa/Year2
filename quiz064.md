```py
from adts import stack, queue #import class for queue and stack
import random #import random to create random numbers

def sort_q2s(scores:queue)->stack: #function to order queue from max to min and output as stack
    output = stack() # make the output stack class
    while not scores.ismepty(): # while the score or the input list has something inside, the code will repeat the process
        copy = queue() #create new queue
        min = 10  #set the amount to find the minimum in the queue
        while not scores.ismepty():
            item = scores.dequeue() #create variable to get the amount of the item that is eliminated from the queue(score) by dequeue
            if item<min: # change the minimum if the item is less than the minimum
                min = item
            copy.enqueue(item) #insert the amount dequeue into the new queue
        #remove the min from original queue
        scores = copy #Copy the information in the backup queue to the main queue
        copy = queue() #empty queue

        while not scores.ismepty():
            item = scores.dequeue() # push in the minimum value when the item dequeued is the minimum value
            if item == min:
                output.push(item)
            else:
                copy.enqueue(item)
        scores = copy #reset queue

    return output # return the result


scores = queue() #make input become queue
for _ in range(10): #insert 10 random numbers into the queue
    scores.enqueue(random.randint(1,7))

print(f"original: {scores} output:{sort_q2s(scores)}") # print the result


```




# Test
<img width="1357" alt="64res" src="https://user-images.githubusercontent.com/82266864/194754841-07694f47-d877-46f8-957a-ee1e3012d2f6.png">


# Flowchart for function
![DF2E4A13-B511-4596-A1E7-7AA3772BDC70](https://user-images.githubusercontent.com/82266864/194754941-88f42813-7c66-471a-8613-5ac6d2331252.jpeg)

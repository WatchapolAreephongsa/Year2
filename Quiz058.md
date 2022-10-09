```py
class route:
    def __init__(self,nodes:int,connection:list): # attributes for nodes and connections(between nodes)
        self.nodes = nodes
        self.connection = connection
    #method
    def neighbours(self): # function to find the list of neighbours for all the nodes.
        output = [] #empty list for output
        for i in range (self.nodes): #create loop for as many times as number of nodes to check connection of each node
            output.append([]) # create list equal to number of nodes
            for k in range(len(self.connection)): #loop for the numbers of connections
                if i in self.connection[k]: #if the specific node is in that connection or not
                    if self.connection[k][0]!=i: #if the first node in that connection is not the selected node then it will be append in the output
                        output[i].append(self.connection[k][0])
                    else: # if it is then the second node will be appended
                        output[i].append(self.connection[k][1])
        return output # return the output list
    
# test
test = route(4,[(0,1),(0,2),(1,2),(2,3)])
test2 = route(6,[(0,3),(2,1),(2,5),(4,3),(5,1),(3,5)])
print(test.neighbours())
print(test2.neighbours())
```

# Test

<img width="841" alt="58 result" src="https://user-images.githubusercontent.com/82266864/194762568-3bb2c9dc-a1a3-4520-a102-f7a931ccc954.png">

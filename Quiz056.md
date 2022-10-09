```py
class ippacket:
    '''
    tx = sender , rx = receiver
    port = integer 0-2^16
    max: BA:AA:09:82 so it is string
    ip : string
    '''
    def __init__(self,port_tx:int,port_rx:int,mac_tx:str,mac_rx:str,ip_tx:str,ip_rx:str): #attributes
        self.port_tx = self.binirizer(port_tx)  #binary form of port of sender and reciever
        self.port_rx = self.binirizer(port_rx)
        self.mac_tx = self.maclist2binary(mac_tx.split(":")) #binary form of mac
        self.mac_rx = self.maclist2binary(mac_rx.split(":"))
        self.ip_tx = self.iplist2binary(ip_tx.split(".")) #binary form of ip
        self.ip_rx = self.iplist2binary(ip_rx.split("."))

    def binirizer(self,number:int)->str:
        "receives an integer produces a string with the binary rep"
        result = "" #emptty string for result
        while number>0:
            result += str(number%2) # get the remainder and add into the result
            number = number//2 # divide 2 without remainder
        return result[::-1].rjust(8,"0") 
        #return the reverse order andmake it 8 digits(by filling in front of number with 0 in the case the numbe does not require 8 difits)

    def hex2dex(self,num:str)->int: #converting hexadecimal tp decimal
        symbols = {'A':10,'B':11,'C':12,'D':13,"E":14,"F":15} #extra symbol in the dictionary form
        result = 0 #result variable in integer form 
        for index,digit in enumerate(num): # give index of element
            if digit in "0123456789": #check if the specific digit is number
                digit_dec = int(digit) #if it is, it will be saved in new variable
            else:
                digit_dec = symbols[digit] #if not convert the digit to number instead of letter
            result+= 16**(len(num)-1-index)*digit_dec #times the number to 16 to the power of the specific index from backward(last = 0 and so on)
        return result #return result in decimal
    def maclist2binary(self,mac): #converting mac address to binary form
        "mac = ['A0','BB',.....]"
        result = "" # empty string
        for element in mac: #use binirizer to convert decimal(converted from hexa) in mac to binary
            binary = self.binirizer(self.hex2dex(element))
            result += binary#add it to the result
        return result # return result
    def iplist2binary(self,ip): #converting ip address from decimal to binary with binirizer
        result = ""
        for element in ip:
            result +=  self.binirizer(int(element))
        return result

    def build(self): # put ip,mac,port of sender with ip,mac,port of reciever 
        return self.ip_tx + self.mac_tx + self.port_tx +self.ip_rx + self.mac_rx + self.port_rx

 #testing
test1 = ippacket(ip_rx="10.10.0.1",ip_tx="10.10.0.2",
                 mac_rx="BA:AA:09:89:0A:00",mac_tx="BA:AA:09:89:0A:00",
                 port_rx=80 , port_tx=80)
print(test1.binirizer(10)) #test binirizer
print(test1.hex2dex(num="B3")) #test converting hexa to decimal
print(test1.build( )) #function build test

```

# Test 
<img width="1407" alt="converter" src="https://user-images.githubusercontent.com/82266864/194765035-e78cb0c5-dbcf-4820-8795-9e3e4bb6e0f3.png">

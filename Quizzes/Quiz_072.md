## Quiz 072
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/Quiz072text.png)
### Classwork
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/quiz072notes.jpg)
### Code 
```.py
from random import randint
import time
class macGenerator():
    def __init__(self,n:int):
        self.n=n
        self.mac_list=[]
    def get_addresses(self):
        dict={1:'1',2:'2',3:'3',4:'4',5:'5',6:'6',7:'7',8:'8',9:'9',10:"A",11:"B",12:"C",13:"D",14:"E",15:"F"}
        cnt=0
        address=""
        while len(self.mac_list)!=self.n:
            for digits in range(0,12):
                address+=f"{dict[randint(1,15)]}"
                cnt+=1
                if cnt==2:
                    address+=":"
                    cnt=0
            if address not in self.mac_list:
                self.mac_list.append(address)
            address=""

        return self.mac_list
start_time = time.time()
print(macGenerator(n=10000).get_addresses())
end_time = time.time()

execution_time = end_time - start_time
print("Execution time:", execution_time, "seconds")
```
### Proof of work
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/Quiz072proof.png)

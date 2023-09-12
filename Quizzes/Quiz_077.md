## Quiz 077
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/Quiz077text.png)
### Classwork
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/Quiz077classwork.jpg)
### Code
```.py
class parity():
    def __init__(self,data:str):
        self.data = data

    def check_parity(self):
        cntr = 0
        for i in range(1,len(self.data)):
            cntr += int(self.data[i])
        if bool(cntr%2) != bool(int(self.data[0])):
            return False
        else:
            return True


test1 = parity("100111001011001110010110011100101")
test2 = parity("011101111101110111110111001111")
# True that error is present or False which means that there isn't an error
print(test1.check_parity())
print(test2.check_parity())
```
### Proof of work
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/Quiz077proof.png)

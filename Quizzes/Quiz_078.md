## Quiz 078
### Classwork
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/Quiz078classwork.jpg)
### Code
```.py
class firewall:
    def __init__(self,data):
        self.data=data
    def binary_convert(self,n:int)->str:
        a,binary=n,""
        for i in range(16):
            if a%2:
                binary="1"+binary
            else:
                binary="0"+binary
            a=a//2
        return binary
    def layer_4_firewall(self):
        if self.data[:16]== self.binary_convert(n=22123) or self.data[:16]== self.binary_convert(n=80):
            return(f"Allowed  {self.data[16:]}")
        else:
            return(f"Filtered {False}")
```
### Proof of work

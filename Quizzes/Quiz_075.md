## Quiz 075
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/Quiz075text.png)
### Classwork
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/Quiz075Classwork.jpg)
### Code
```.py
class osi_phsyical():
    def __init__(self, input:str):
        self.unprocessed = input

    def dec2bin(self,letter):
        temp = ord(letter)
        bin = ""
        while temp != 0:
            bin = f"{temp % 2}" + bin
            temp= temp // 2
        if len(bin) != 8:
            bin = "0"*(8-len(bin))+bin

        return bin

    def get_output(self):
        out_str =  ""
        for letter in self.unprocessed:
            out_str += self.dec2bin(letter) + " "
        return out_str[:-1]

msg_test1="Hello World!"
print(f"Message {msg_test1} ----> Binary {osi_phsyical(msg_test1).get_output()}")
msg_test2="ABC123"
print(f"Message {msg_test2} ---->Binary {osi_phsyical(msg_test2).get_output()}")
```
### Proof of work
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/Quiz075proof.png)

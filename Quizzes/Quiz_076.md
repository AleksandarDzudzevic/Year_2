## Quiz 076
### Classwork
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/Quiz076Classwork.jpg)
### Code
```.py
class ErrorChecker():
    def __init__(self, input:str):
        self.data_input = input

    def error_check(self):
        out = True
        correct = ""
        for i in range(len(self.data_input)//3):
            length = int(len(self.data_input)//3)
            if self.data_input[i] == self.data_input[i+length] == self.data_input[i+2*length]:
                correct += self.data_input[i]
                pass
            else:
                out = False
                if self.data_input[i] == self.data_input[i+length] or self.data_input[i] == self.data_input[i+2*length]:
                    correct += self.data_input[i]
                elif self.data_input[i+length] == self.data_input[i+2*length]:
                    correct += self.data_input[i+length]
        return out, correct


data = "011101111101110111110111"
data_test2="011101110111011101110111"
print(ErrorChecker(data).error_check())
print(ErrorChecker(data_test2).error_check())

```
### Proof of work
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/Quiz076proof.png)

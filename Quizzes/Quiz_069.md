## Quiz 069
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/Quiz069text.png)
### Classwork
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/Quiz069.jpg)
### Code
```.py
import sys
sales=[38,100,150,1,10,28,35]
min=sys.maxsize
max=0
for i in sales:
    if i>max:
        max=i
    if i<min:
        min=i
print(f"Weekly sale profit is {max-min} yen")
```
### Proof of work
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/Quiz069proof.png)

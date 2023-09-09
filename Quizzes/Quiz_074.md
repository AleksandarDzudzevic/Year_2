## Quiz 074
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/Quiz074text.png)
### Classwork
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/Quiz074Classwork.jpg)
### Code
```.py
class packages():
    def __init__(self, mac_rx: str, ip_rx: str, mac_sx: str, ip_sx: str, data: str) -> None:
        self.mac_rx = mac_rx
        self.ip_rx = ip_rx
        self.mac_sx = mac_sx
        self.ip_sx = ip_sx
        self.data = data
        self.head = f"{self.mac_rx}|{self.ip_rx}|{self.mac_sx}|{self.ip_sx}|"
        self.pck_list = []

    def build_data_pckg(self) -> list:
        cnt = 0
        for i in range(len(self.data) // 4):
            pckg = self.head + f"{i}|{self.data[cnt:cnt+4]}"
            self.pck_list.append(pckg)
            cnt += 4
        pckg = self.head + f"{len(self.data) // 4 + 1}|{self.data[cnt:]}"
        self.pck_list.append(pckg)
        return self.pck_list

# Create an instance of the packages class
pkg_instance = packages(mac_rx="192:112L121212", ip_rx="12312331D", mac_sx="E1232123", ip_sx="F13123", data="hello world")

# Call the method and print the result
print(pkg_instance.build_data_pckg())

```
### Proof of work
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/Quiz074proof.png)

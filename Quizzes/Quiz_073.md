## Quiz 073
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/Quiz073text.png)
### Classwork
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/Quiz073Classwork.jpg)
### Code
```.py
class ip_tables():
    def __init__(self):
        self.routing_table = {}
        self.used_ips = set()
        self.ip_ending = 1

    def check_mac(self, mac):
        return len(mac) == 17 and mac.count(":") == 5

    def get_ip(self, mac):
        if self.check_mac(mac):
            if mac in self.routing_table:
                return self.routing_table[mac]  # Return the existing IP address
            else:
                while True:
                    ip = f"192.168.0.{self.ip_ending}"
                    self.ip_ending += 1
                    if ip not in self.used_ips:
                        self.used_ips.add(ip)
                        self.routing_table[mac] = ip  # Add the new MAC-IP pair to the routing table
                        return ip

    def display_routing_table(self):
        print("Table:")
        for mac, ip in self.routing_table.items():
            print(f"MAC: {mac}  IP: {ip}")


ipt = ip_tables()
while True:
    mac_address = input("Enter a MAC address (or 'q' to quit): ")
    if mac_address == 'q':
        break

    if ipt.check_mac(mac_address):
        ip_address = ipt.get_ip(mac_address)
        print(f"{mac_address} : {ip_address}")
        ipt.display_routing_table()
    else:
        print(f"Invalid MAC address")

```
### Proof of work
![](https://github.com/AleksandarDzudzevic/Year_2/blob/main/Quiz073proof.png)

# tcp_data_change
HTTP data change program(only http!)

# Environments setting
Set up the iptables so that the packets sent and received go through the netfilter queue.
```
iptables -F
iptables -A OUTPUT -p tcp -j NFQUEUE --queue-num 0
iptables -A INPUT -p tcp -j NFQUEUE --queue-num 0
```
```
$ apt install libmnl-dev
$ apt install libnfnetlink-dev
$ apt install libnetfilter-queue-dev
```

# How to use
```
$ git clone https://github.com/kongbiji/tcp_data_change
$ cd tcp_data_change
$ make
$ sudo ./tcp_data_change <from string> <to string>
```

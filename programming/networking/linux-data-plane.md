# Linux Data Plane

Very high level:

```
Device Drivers (connect to network cards)
|
Recv function (parse headers)
|
| if local
|
TCP, ICMP, IPsec
|
| else
|
forward
|
Queueing discipline
|
arp
|
transmit
|
driver

Also todo (ingres):
bridge
vlan
arp
```

## Netlink

Netlink is a protocol for user space utilities to interact with the kernel data
plane.

Based on berkeley [sockets](./socket.md).

Each application is a client - servers run in kernel. Supports multicast.

# Internet Protocol

Internet Protocol provides host to host addressing and routing. Versions 1-3
were revised. IPV4 is the one we all know and love. IPV5 was called Internet
Stream Protocol (SP) and never took off. And IPV6 is what happens when you run
out of addresses in IPV4 lol.

The specification can be found [here](https://www.ietf.org/rfc/rfc791.txt).

The IP exists one level above "local networks" to pass data between local
networks (nets or gateways). There are no acknowledgments either end-to-end or hop-by-hop.

## Datagram

The IP layer sends a 20 byte packet, roughly:

```cpp
struct ipv4_header {
    uint8_t version_and_header_length;
    uint8_t DSCP_and_ECN;
    uint16_t total_length;
    uint16_t identification;
    uint16_t flags_and_fragment_offset;
    uint8_t time_to_live;
    uint8_t protocol;
    uint16_t header_checksum;
    uint32_t source_ip_address;
    uint32_t destination_ip_address;
    uint32_t options;
    // ...payload
};
```

This packet is sent as a datagram, so there is no guarentee the message will be
delivered. Layers above IP can detect dropped packets and recover if they wish.

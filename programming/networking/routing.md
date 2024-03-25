# Routing

## Router Data Plane

A router is a gateway between different networks (can have different link layers).
They also forward the traffic to the correct destination.

### Forwarding vs routing

- Forwarding: data plane

Direct a data packet to an output port/link by use of a forwarding table.

- Routing: Control plane

Compute paths by communicating with neighbors. Creates the forwarding table.

### Packet forwarding

Control plane (route processor) calculates the forwarding table

Data plane - life of packet

- received at ingress of line card
- lookup destination in forwarding table
- send packet over switch fabric to output port
- line card transmits packet

Key computing work: lookup IP address really quickly. Also some updates to
packet headers.

### Longest Prefix Match (LPM)

Find the most specific IP prefix that matches the destination.

Good data structure for this: Trie

Each node has a 0 child to left and 1 child to right. Walk the tree to perform a
lookup (entirety of prefix length)

### Switch fabric

Each line card stores the forwarding table and has connections to other line
cards, or we just load into system memory and do the networking with cpu time.

- Link scheduling
- Dropping packets on congestion
- Traffic shaping to force traffic to conform to a policy

## Routing Control Plane



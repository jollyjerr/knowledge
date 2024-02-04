# The CAP Theorem

Any network shared data system can have at most two of the three properties:

1. Consistency: Data across nodes is the same

Each server returns the right response to every request. Also called atomic
consistency: Each operation appears to have been completed in a single instant.

2. Availability: Data is highly available for update operations

Each request eventually receives a response

3. Partition: The network infrastructure is tolerant to network partitions

The system tolerates communication failure and can handle nodes going down.

## Proof

By contradiction.

Assume G1 and G2 have an initial state of 0
Operation alpha writes 0 -> 1, then reads the value
Because g1 and g2 cannot talk, alpha writes 1 but reads 0

## Resources

https://users.ece.cmu.edu/~adrian/731-sp04/readings/GL-cap.pdf

# Consistency Models

## Overview
Consistency models define the rules for how data is viewed and updated across a distributed system. They determine the guarantees provided to the users regarding the visibility and ordering of updates.

## Key Consistency Models
- **Strong Consistency**: Guarantees that all nodes see the same data at the same time after a write operation.
- **Eventual Consistency**: Guarantees that, given enough time, all nodes will converge to the same value.
- **Causal Consistency**: Guarantees that operations that are causally related are seen by all nodes in the same order.
- **Read-Your-Writes Consistency**: Guarantees that a node will always see its own writes.

## Example: Eventual Consistency
Here is an example of how eventual consistency works in a distributed system.

### Pseudocode
```pseudocode
if write request:
    write data to local node
    propagate data to other nodes asynchronously
else if read request:
    read data from local node


Explanation
Write Request: Data is written to the local node and then propagated to other nodes asynchronously.
Read Request: Data is read from the local node, which may not have the most recent update.
Additional Resources
Consistency Models in Distributed Systems
Distributed Systems: Principles and Paradigms
# Memory Hierarchy

## Overview
Memory hierarchy is a structure that uses multiple levels of memory with different speeds and sizes to optimize performance and cost. The goal is to provide a balance between fast access times and large storage capacity.

## Key Components
- **Registers**: The fastest and smallest type of memory located within the CPU.
- **Cache**: A small, fast memory located close to the CPU to store frequently accessed data.
- **Main Memory (RAM)**: Larger and slower than cache, used to store data and instructions currently in use.
- **Secondary Storage**: Non-volatile storage such as hard drives and SSDs, used for long-term data storage.

## Example: Memory Access
Here is an example of how data might be accessed in a memory hierarchy.

### Pseudocode
```pseudocode
if data in registers:
    access data from registers
else if data in cache:
    access data from cache
else if data in main memory:
    load data into cache
    access data from cache
else:
    load data into main memory
    load data into cache
    access data from cache
```

### Explanation
- `Registers`: Checked first for the fastest access.
- `Cache`: Checked next if data is not in registers.
- `Main Memory`: Loaded into cache if data is not in cache.
- `Secondary Storage`: Loaded into main memory if data is not in main memory.

## Additional Resources
- [Memory Hierarchy in Computer Architecture](https://www.geeksforgeeks.org/memory-hierarchy-in-computer-architecture/)
- [Computer Architecture: A Quantitative Approach](https://www.elsevier.com/books/computer-architecture/hennessy/978-0-12-383872-8)
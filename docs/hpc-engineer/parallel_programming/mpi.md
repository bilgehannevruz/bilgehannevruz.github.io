# MPI (Message Passing Interface)

## Description
MPI is a standardized and portable message-passing system designed to function on a wide variety of parallel computing architectures. It allows multiple processes to communicate with one another by sending and receiving messages.

## Key Concepts
- **Point-to-Point Communication**: Direct communication between two processes.
- **Collective Communication**: Communication involving a group of processes.
- **Synchronization**: Mechanisms to coordinate the execution of processes.

## Example Code

### C Example
This example demonstrates a simple MPI program where each process prints its rank.

```c
#include <mpi.h>
#include <stdio.h>

int main(int argc, char** argv) {
    MPI_Init(NULL, NULL);

    int world_size;
    MPI_Comm_size(MPI_COMM_WORLD, &world_size);

    int world_rank;
    MPI_Comm_rank(MPI_COMM_WORLD, &world_rank);

    printf("Hello world from rank %d out of %d processors\n", world_rank, world_size);

    MPI_Finalize();
    return 0;
}
```


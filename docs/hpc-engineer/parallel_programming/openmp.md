# Parallel Programming Fundamentals

## OpenMP

### Description
OpenMP (Open Multi-Processing) is an API that supports multi-platform shared memory multiprocessing programming in C, C++, and Fortran. It consists of a set of compiler directives, library routines, and environment variables that influence run-time behavior.

OpenMP is designed for parallel programming on shared memory architectures. It allows developers to write parallel code by adding simple compiler directives to their existing code. These directives tell the compiler how to parallelize the code.

### Key Concepts
- **Parallel Regions**: Blocks of code that are executed by multiple threads in parallel.
- **Work Sharing**: Distributes the execution of code across multiple threads.
- **Synchronization**: Mechanisms to control the access to shared resources.

### Example Code

#### C Example
This example demonstrates a simple parallel region where multiple threads print a message.

```c
#include <omp.h>
#include <stdio.h>

int main() {
    #pragma omp parallel
    {
        int thread_id = omp_get_thread_num();
        printf("Hello from thread %d\n", thread_id);
    }
    return 0;
}
```


#### Explanation
- `#pragma omp parallel`: This directive tells the compiler to execute the following block of code in parallel.
- `omp_get_thread_num()`: This function returns the thread number of the current thread.
How to Compile and Run
To compile and run the OpenMP program, you need to use a compiler that supports OpenMP, such as `gcc`.
To compile and run the OpenMP program, you need to use a compiler that supports OpenMP, such as `gcc`.

```bash
gcc -fopenmp -o hello_omp hello_omp.c
./hello_omp
```



### Advanced Example: Parallel Loop
This example demonstrates how to parallelize a loop using OpenMP.


#### C Example
```c
#include <omp.h>
#include <stdio.h>

int main() {
    int n = 10;
    int a[n];

    #pragma omp parallel for
    for (int i = 0; i < n; i++) {
        a[i] = i * i;
        printf("Thread %d: a[%d] = %d\n", omp_get_thread_num(), i, a[i]);
    }

    return 0;
}
```


#### Explanation
Explanation
- #pragma omp parallel for: This directive tells the compiler to parallelize the following for loop.
- Each iteration of the loop is executed by a different thread.

##### How to Compile and Run

```bash
gcc -fopenmp -o parallel_loop parallel_loop.c
./parallel_loop
```

### Additional Resources
- [OpenMP Official Website](https://www.openmp.org)
- [OpenMP API Specification](https://www.openmp.org/specifications/)
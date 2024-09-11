## Overview
Batch scheduling is a method of job scheduling where jobs are collected into batches and executed sequentially. This approach is commonly used in environments where jobs can be processed without immediate user interaction, such as in batch processing systems and high-performance computing clusters.

## Key Features
- **Job Collection**: Jobs are collected into batches before execution.
- **Sequential Execution**: Jobs in a batch are executed one after another.
- **Resource Optimization**: Resources are allocated efficiently to maximize throughput.

## Example: Batch Scheduler
Here is an example of a simple batch scheduler using a queue.

### Pseudocode
```pseudocode
queue = []

function add_job(job):
    queue.append(job)

function run_jobs():
    while queue is not empty:
        job = queue.pop(0)
        execute(job)
```

## Additional Resources

 - [Batch Processing](https://en.wikipedia.org/wiki/Batch_processing)
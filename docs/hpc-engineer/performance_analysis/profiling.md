## Overview
Profiling is the process of measuring the performance of a program, identifying which parts of the program consume the most resources. This helps in optimizing the code to improve performance.

## Tools for Profiling
- **Gprof**: A profiling program that collects and displays runtime performance data.
- **Valgrind**: An instrumentation framework for building dynamic analysis tools, including a profiler.

## Standard Operating Procedure (SOP) for Profiling

### Using Gprof

#### Step 1: Compile the Program with Profiling Enabled
1. **Compile the Program**:
    - Use the `-pg` flag to compile your program:
    ```bash
    gcc -pg -o my_program my_program.c
    ```

#### Step 2: Run the Program
1. **Execute the Program**:
    - Run the compiled program to generate profiling data:
    ```bash
    ./my_program
    ```

#### Step 3: Generate the Profiling Report
1. **Analyze Profiling Data**:
    - Use Gprof to analyze the profiling data and generate a report:
    ```bash
    gprof my_program gmon.out > analysis.txt
    ```

#### Step 4: Review the Report
1. **Open the Report**:
    - Open the `analysis.txt` file to review the profiling report and identify performance bottlenecks.

### Using Valgrind

#### Step 1: Run the Program with Valgrind
1. **Execute the Program**:
    - Use Valgrind to execute your program and collect profiling data:
    ```bash
    valgrind --tool=callgrind ./my_program
    ```

#### Step 2: Analyze the Profiling Data
1. **Annotate Profiling Data**:
    - Use `callgrind_annotate` to analyze the collected data:
    ```bash
    callgrind_annotate callgrind.out.<pid>
    ```

#### Step 3: Review the Analysis
1. **Review the Output**:
    - Review the output to identify performance bottlenecks and memory issues.

## Additional Resources
- [Gprof Documentation](https://sourceware.org/binutils/docs/gprof/)
- [Valgrind Documentation](http://valgrind.org/docs/manual/manual.html)
## Overview
Slurm is an open-source workload manager designed for high-performance computing (HPC) environments. It is used to allocate resources, schedule jobs, and manage job queues.

## Key Features
- **Resource Allocation**: Efficiently allocates resources to jobs.
- **Job Scheduling**: Schedules jobs based on various policies and priorities.
- **Queue Management**: Manages job queues and ensures fair resource distribution.

## Installation and Configuration

### Installing Slurm
To install Slurm on an HPC environment, follow these steps:

1. **Install Slurm**:
    - For Ubuntu, you can use the following commands:
    ```sh
    sudo apt-get update
    sudo apt-get install -y slurm-wlm
    ```

2. **Configure Slurm**:
    - Edit the Slurm configuration file `/etc/slurm-llnl/slurm.conf`:
    ```sh
    sudo nano /etc/slurm-llnl/slurm.conf
    ```

    - Example configuration:
    ```conf
    ControlMachine=slurm-controller
    MpiDefault=none
    ProctrackType=proctrack/linuxproc
    ReturnToService=2
    SlurmdPort=6818
    SlurmdSpoolDir=/var/spool/slurmd
    SlurmUser=slurm
    StateSaveLocation=/var/spool/slurmctld
    SwitchType=switch/none
    TaskPlugin=task/affinity

    # SCHEDULING
    SchedulerType=sched/backfill
    SelectType=select/cons_res
    SelectTypeParameters=CR_Core

    # LOGGING AND ACCOUNTING
    AccountingStorageType=accounting_storage/slurmdbd
    AccountingStorageHost=slurmdbd
    JobAcctGatherType=jobacct_gather/linux
    JobAcctGatherFrequency=30

    # COMPUTE NODES
    NodeName=slurm-node[0-9] CPUs=4 State=UNKNOWN
    PartitionName=debug Nodes=slurm-node[0-9] Default=YES MaxTime=INFINITE State=UP
    ```

3. **Start Slurm Services**:
    ```sh
    sudo systemctl start slurmctld
    sudo systemctl start slurmd
    ```

### Submitting a Job with Slurm
Here is an example of how to submit a job using Slurm.

### Command
```sh
sbatch my_job_script.sh
```

### Example Job Script
```bash
#!/bin/bash
#SBATCH --job-name=test_job
#SBATCH --output=result.out
#SBATCH --error=result.err
#SBATCH --time=01:00:00
#SBATCH --qos=normal
#SBATCH --partition=debug
#SBATCH --ntasks=1
#SBATCH --cpus-per-task=4

srun hostname
```

### Configuring QoS and Limits
```bash
# QoS settings
QOSDef=normal
QOS=normal
QOS=high

# Limits
GrpTRES=cpu=1000
GrpJobs=100
GrpSubmitJobs=200
```
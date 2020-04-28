# cc-slurm

This profile configures Snakemake to run on Compute Canada with SLURM (e.g. graham).


## Setup

### Install cookiecutter

Install cookiecutter on your system (make sure you have python3 loaded):

    pip install cookiecutter --user

### Deploy profile

To deploy this profile, run the following on the login node (e.g. graham)

    cookiecutter gh:akhanf/cc-slurm -o ~/.config/snakemake -f

NOTE: If you are using graham with the `ctb-akhanf` account then all the default options can be used. 



Then, you can run Snakemake with:

    snakemake --profile cc-slurm ...


### Parameters

The following resources are supported by on a per-rule basis:

**mem_mb** - set the memory resource request (megabytes).  
**time** - set the walltime resource (minutes).  
**gpus** - set the number of gpus (defaults to 0).  

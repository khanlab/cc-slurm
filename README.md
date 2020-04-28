# cc-slurm

This profile configures Snakemake to run on Compute Canada with SLURM (e.g. graham).

## Setup

### Deploy profile

To deploy this profile, run

    mkdir -p ~/.config/snakemake
    cd ~/.config/snakemake
    cookiecutter https://github.com/akhanf/cc-slurm.git

Then, you can run Snakemake with

    snakemake --profile cc-slurm ...


### Parameters

The following resources are supported by on a per-rule basis:

**mem_mb** - set the memory resource request (megabytes).  
**time** - set the walltime resource (minutes).  
**gpus** - set the number of gpus (defaults to 0).  

# cc-slurm

This profile configures Snakemake to run on Compute Canada with SLURM (e.g. graham).

Note: the default options already use the `--use-singularity` and `--use-envmodules` flags, and the `ctb-akhanf` compute allocation account. 

## Setup

### Install cookiecutter

Install cookiecutter on your system (make sure you have python3 loaded):

    pip install cookiecutter --user

### Deploy profile

To deploy this profile, run the following on the login node (e.g. graham):

    cookiecutter gh:khanlab/cc-slurm -o ~/.config/snakemake -f --no-input

If you are not using the `ctb-akhanf` account, or want to customize the options, use this instead:

    cookiecutter gh:khanlab/cc-slurm -o ~/.config/snakemake -f



Then, you can run Snakemake with:

    snakemake --profile cc-slurm ...


### Parameters

The following resources are supported by on a per-rule basis:

**mem_mb** - set the memory resource request (megabytes).  
**time** - set the walltime resource (minutes).  
**gpus** - set the number of gpus (defaults to 0).  

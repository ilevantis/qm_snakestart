# qm_snakestart
Usage: `qm_snakestart path/to/PROJECTNAME`

A script to initialise a snakemake project to be run on the QMUL cluster.

conda and conda-env are required for this script.

Creates a basic directory structure for a snakemake project and an accompanying conda environment for use on Apocrita.
The produced directory structure looks like this:

    PROJECTNAME
    ├── bin/
    ├── docs/
    ├── input_data/
    ├── manual_steps/
    ├── scripts/
    ├── .gitignore
    ├── README.md
    ├── Snakefile
    ├── runsnake
    └── environment.yml

The conda environment will be named `PROJECTNAME`.
`runsnake` holds the parameters for successfully running snakemake on Apocrita and can be used to launch snakemake.
It defaults to using autoScratch/monthly as a working directory.


# agetouch
Usage `agetouch path\to\dir`

Script to recursively touch all non-hidden files/directories in a directory but retain the order of relative ages between files.
This is useful for preventing autoScratch from deleting older files while still allowing snakemake to figure out which output files do not need to be recreated.

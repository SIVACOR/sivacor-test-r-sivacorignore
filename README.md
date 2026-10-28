# Test file for R with `.sivacorignore`

Combines [sivacor-test-r](https://github.com/SIVACOR/sivacor-test-r) with the
[`.sivacorignore` tutorial](https://github.com/SIVACOR/documentation/blob/main/docs/tutorial-removing-data.md).

- set up with R 4.3.1 (`rocker/r-ver:4.3.1`) and `renv`
- main file: `main.R`
- import [`sivacorignore-workflow.yaml`](sivacorignore-workflow.yaml) into the submission form

After the run, [`.sivacorignore`](.sivacorignore) removes `data/raw/` and all `*.tmp` files from the replication package.

# Test file for R with `.sivacorignore`

Combines [sivacor-test-r](https://github.com/SIVACOR/sivacor-test-r) with the
[`.sivacorignore` tutorial](https://github.com/SIVACOR/documentation/blob/main/docs/tutorial-removing-data.md).

- set up with R 4.3.1 (`rocker/r-ver:4.3.1`) and `renv`
- main file: `main.R`
- requires a [FRED API key](https://fred.stlouisfed.org/docs/api/api_key.html) as environment secret `FRED_APIKEY`
- import [`sivacorignore-workflow.yaml`](sivacorignore-workflow.yaml) into the submission form (after adding your API key)

After the run, [`.sivacorignore`](.sivacorignore) removes `data/raw/`, the API-obtained `data/api/`, and all `*.tmp` files from the replication package.

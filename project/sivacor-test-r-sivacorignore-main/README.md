# Test file for R with `.sivacorignore`

![Palmer penguins](data/raw/lter_penguins.png)


Assume that the `penguins` are a super-confidential biological dataset.


After the run, [`.sivacorignore`](.sivacorignore) removes

-  `data/raw/` (which includes the original penguin data)
- all `*.tmp` files which might still contain penguin data.

Because the penguins are "confidential", we also need to remove the above picture of the "confidential penguins"! Since it is  stored in `data/raw/`, `.sivacorignore` removes it.

## Steps

- set up with R 4.3.1 (`rocker/r-ver:4.3.1`) and `renv`
- main file: `main.R`
- all output is written to `results/`
- import [`sivacorignore-workflow.yaml`](sivacorignore-workflow.yaml) into the submission form

## Expected output

```
main.R
linux-system-info.sh
renv/
renv.lock
.Rprofile
.gitignore
README.md
sivacorignore-workflow.yaml
results/
  penguins_summary_table.tex
  penguins_grouped_table.tex
  penguins_bill_length_histogram.pdf
.sivacorignore
```

Note that `data/raw/` (data and picture) and `results/penguins_clean.tmp` are gone.

The output of a reference run is on the [`reference-output`](https://github.com/SIVACOR/sivacor-test-r-sivacorignore/tree/reference-output/project/sivacor-test-r-sivacorignore-main) branch.

## Credits


*Artwork by @allison_horst, from [palmerpenguins](https://github.com/allisonhorst/palmerpenguins).*
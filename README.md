# Test file for R with `.sivacorignore`

![Palmer penguins](data/raw/lter_penguins.png)


Assume that the `penguins` are a super-confidential biological dataset.


After the run, [`.sivacorignore`](.sivacorignore) removes

-  `data/raw/` (which includes the original penguin data)
- all `*.tmp` files which might still contain penguin data.

The picture of the confidential penguins is stored in `data/raw/` as well, so it is removed along with the data, without needing an additional line in `.sivacorignore`.

## Steps

- set up with R 4.3.1 (`rocker/r-ver:4.3.1`) and `renv`
- main file: `main.R`
- all output is written to `results/`
- import [`sivacorignore-workflow.yaml`](sivacorignore-workflow.yaml) into the submission form

## Expected output

```
main.R
run.sh
linux-system-info.sh
renv/
renv.lock
.Rprofile
README.md
sivacorignore-workflow.yaml
results/
  penguins_summary_table.tex
  penguins_grouped_table.tex
  penguins_bill_length_histogram.pdf
.sivacorignore
```

Note that `data/raw/` (data and picture) and `results/penguins_clean.tmp` are gone.

## Credits


*Artwork by @allison_horst, from [palmerpenguins](https://github.com/allisonhorst/palmerpenguins).*
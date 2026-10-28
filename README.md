# Test file for R with `.sivacorignore`

![Palmer penguins](images/lter_penguins.png)


Assume that the `penguins` are a super-confidential biological dataset.


After the run, [`.sivacorignore`](.sivacorignore) removes

-  `data/raw/` (which includes the original penguin data)
- all `*.tmp` files which might still contain penguin data.

## Steps

- set up with R 4.3.1 (`rocker/r-ver:4.3.1`) and `renv`
- main file: `main.R`
- import [`sivacorignore-workflow.yaml`](sivacorignore-workflow.yaml) into the submission form

## Expected output

```
code/
  main.R
output/
  figure.png
  ...
.sivacorignore
```

## Credits


*Artwork by @allison_horst, from [palmerpenguins](https://github.com/allisonhorst/palmerpenguins).*
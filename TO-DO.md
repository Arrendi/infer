## For upcoming CRAN version

- Add warning when theoretical distribution is used that 
  assumptions should be checked  
- Remove commented out `calculate()` for theoretical distributions in vignettes
- Remove hypothesis test for standard deviation (Mine will fix)
- Change `method = "randomization"` to `method = "simulation"`
- Change `type = "simulate"` to `type = "probability model"`
  
## For future versions

- Consider re-working how p-values can be calculated (both for computational and theoretical)
- Shift to list-columns in `generate()`
- Implement check of `stat` in theoretical `visualize()`
- Write test to check that bootstrapped values are centered near the 
  hypothesized value in `specify()`
- Check that assumptions have been met for the theoretical distribution and `"both"`
- Write vignettes on how NOT to use infer (strange errors, funky results, etc.)
- Implement theoretical distributions for bootstrap distributions
- Create `references.md` with links to slides/talks/workshops given about `infer`
- Add Lionel's vis checking package ([`vdiffr`](https://github.com/lionel-/vdiffr)) to `visualize()` tests
- Produce error if `mu` is given in `specify()` but `stat = "median"` provided in `calculate()`
- Shading for Confidence Intervals in `visualize()` (Mine would prefer green
for CI and red for p-values)
- Determine whether `calculate()` should be where the `set_params()` function is called
instead of in `specify()`
- Need to also add parameters to wrapper functions so that randomization
methods can be implemented by practitioners looking to skip the longer pipe syntax
- Determine if other wrapper functions should be created 
    - `z_test()`? 
    - Add implementation of one sample `t_test()`?
- Create easy functions to determine observed statistics like the implemented
`t_stat`: e.g., `mean_stat`?
- Tweak `pkgdown` page to include ToDo's. [{dplyr}](https://github.com/tidyverse/dplyr/blob/master/_pkgdown.yml) example

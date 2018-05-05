## For future CRAN releases

- Check that `specify() %>% calculate()` works for `stat = "z"` and `stat = "t"`
  - Modify wrapper functions like `t_stat()` and `chisq_stat()` to wrap 
  `specify() %>% calculate()`. Maybe create `mean_stat()`, etc. as well?
  - Determine if other wrapper functions should be created 
    - `z_test()`? 
    - Add implementation of one sample `t_test()`?
    - Add `order` argument to `t_test()`, `t_stat()`, and similar
- Consider re-working how p-values can be calculated (both for computational and theoretical)
  - Create a `p_value()` function?
  - Similarly, create a `conf_int()` function?
- Check that `stat` is calculated appropriately if `generate()` is not called
  - `order` of the arguments into the standardized statistics should be checked again
  - May require moving of `set_params()` to be after `specify()`
  - Update `visualize()` tests to include `calculate()` step for `method = "theoretical"`
- Add `add_obs_stat` toggle into `visualize()` and p-value calculation?
- Shift to list-columns in `generate()`
- Implement check of `stat` in theoretical `visualize()`
- Write test to check that bootstrapped values are centered near the 
  hypothesized value in `specify()`
- Check that assumptions have been met for the theoretical distribution and `"both"`
- Write vignettes on how NOT to use infer (strange errors, funky results, etc.)
- Implement theoretical distributions for bootstrap distributions
- Create `references.md` with links to slides/talks/workshops given about `infer`
- Add Lionel's vis checking package ([`vdiffr`](https://github.com/lionel-/vdiffr)) to `visualize()` tests
- Shading for Confidence Intervals in `visualize()` (Mine would prefer green
for CI and red for p-values)
- Determine whether `calculate()` should be where the `set_params()` function is called
instead of in `specify()`
- Need to also add parameters to wrapper functions so that randomization
methods can be implemented by practitioners looking to skip the longer pipe syntax
- Find a better word than `"simulate"` for `type` in `generate()`
- Tweak `pkgdown` page to include ToDo's. [{dplyr}](https://github.com/tidyverse/dplyr/blob/master/_pkgdown.yml) example

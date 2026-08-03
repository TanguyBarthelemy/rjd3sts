# Title

Title

## Usage

``` r
sts_outliers(
  y,
  period = NA,
  X = NULL,
  X.td = NULL,
  level = 1,
  slope = 1,
  noise = 1,
  seasonal = c("Trigonometric", "Dummy", "Crude", "HarrisonStevens", "Fixed", "Unused"),
  ao = TRUE,
  ls = TRUE,
  so = FALSE,
  cv = 0,
  tcv = 0,
  estimation.forward = c("Score", "Point", "Full"),
  estimation.backward = c("Point", "Score", "Full")
)
```

## Arguments

- y:

  input time series.

- period:

  annual frequency.

- X:

  Regression variables (same length as y) or NULL

- X.td:

  Groups of days for trading days regressors. The length of the array
  must be 7. It indicates to what group each week day belongs. The first
  item corresponds to Mondays and the last one to Sundays. The group
  used for contrasts (usually Sundays) is identified by 0. The other
  groups are identified by 1, 2,... n (\<= 6). For instance, usual
  trading days are defined by `c(1,2,3,4,5,6,0)`, week days by
  `c(1,1,1,1,1,0,0)`, etc...

- level:

  -1 = no level, 0 = fixed level, 1 = sotchastic level

- seasonal:

  Seasonal model

- ao, ls, so:

  boolean indicating if additive outliers (`ao`), level shift (`ls`) and
  seasonal outliers (`so`) should be detected.

- estimation.backward:

## Examples

``` r
 x<-rjd3toolkit::Retail$BookStores
 sts_outliers(x)
#> Error in .jcheck(silent = FALSE): java.lang.NoSuchMethodError: 'jdplus.toolkit.base.core.ssf.akf.SmoothingOutput jdplus.toolkit.base.core.ssf.akf.AkfToolkit.robustSmooth(jdplus.toolkit.base.core.ssf.univariate.ISsf, jdplus.toolkit.base.core.ssf.univariate.ISsfData, boolean, boolean)'
```

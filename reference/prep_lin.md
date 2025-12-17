# Preparation For Linearization

Adapt the effort table before linearization. It replace the LegID column
with new section and add status when needed.

## Usage

``` r
prep_lin(effort_table, variable, unique_column)
```

## Arguments

- effort_table:

  dataframe. Effort table prepared with check_brut_effort().

- variable:

  character. Variable of interest to keep in the linearisation and
  segmentation.

- unique_column:

  character. Column which describe a group of unique effort condition.

## Value

Effort table with new LegID names and "NEW" status.

## Examples

``` r
prep_lin(effort_table = test_prep_line,
         variable = c("Beaufort", "plateform", "n_obs"), 
         unique_column = "LegID")
#> Redefinig LegID columnn according to Beaufort, plateform and n_obs
#> # A tibble: 580 × 12
#>    Survey plateform     routeType status LegID speed Beaufort Latitude Longitude
#>    <chr>  <chr>         <chr>     <chr>  <chr> <dbl>    <dbl>    <dbl>     <dbl>
#>  1 PELGAS upper_bridge… prospect… BEGIN  3004…    10        2     48.3     -4.54
#>  2 PELGAS upper_bridge… prospect… ADD    3004…    11        2     48.3     -4.62
#>  3 PELGAS upper_bridge… prospect… END    3004…    11        2     48.2     -4.71
#>  4 PELGAS upper_bridge… prospect… BEGIN  3004…    10        3     48.0     -4.71
#>  5 PELGAS upper_bridge… prospect… ADD    3004…    11        3     47.9     -4.68
#>  6 PELGAS upper_bridge… prospect… ADD    3004…    11        3     47.8     -4.62
#>  7 PELGAS upper_bridge… prospect… ADD    3004…    12        3     47.7     -4.50
#>  8 PELGAS upper_bridge… prospect… ADD    3004…    12        3     47.5     -4.39
#>  9 PELGAS upper_bridge… prospect… ADD    3004…    12        3     47.3     -4.27
#> 10 PELGAS upper_bridge… prospect… ADD    3004…    11        3     47.1     -4.16
#> # ℹ 570 more rows
#> # ℹ 3 more variables: n_obs <dbl>, DateTime <dttm>, TransectID <chr>


prep_lin(effort_table = test_prep_line,
         variable = "Beaufort", 
         unique_column = "LegID")
#> Redefinig LegID columnn according to Beaufort
#> # A tibble: 572 × 12
#>    Survey plateform     routeType status LegID speed Beaufort Latitude Longitude
#>    <chr>  <chr>         <chr>     <chr>  <chr> <dbl>    <dbl>    <dbl>     <dbl>
#>  1 PELGAS upper_bridge… prospect… BEGIN  3004…    10        2     48.3     -4.54
#>  2 PELGAS upper_bridge… prospect… ADD    3004…    11        2     48.3     -4.62
#>  3 PELGAS upper_bridge… prospect… END    3004…    11        2     48.2     -4.71
#>  4 PELGAS upper_bridge… prospect… BEGIN  3004…    10        3     48.0     -4.71
#>  5 PELGAS upper_bridge… prospect… ADD    3004…    11        3     47.9     -4.68
#>  6 PELGAS upper_bridge… prospect… ADD    3004…    11        3     47.8     -4.62
#>  7 PELGAS upper_bridge… prospect… ADD    3004…    12        3     47.7     -4.50
#>  8 PELGAS upper_bridge… prospect… ADD    3004…    12        3     47.5     -4.39
#>  9 PELGAS upper_bridge… prospect… ADD    3004…    12        3     47.3     -4.27
#> 10 PELGAS upper_bridge… prospect… ADD    3004…    11        3     47.1     -4.16
#> # ℹ 562 more rows
#> # ℹ 3 more variables: n_obs <dbl>, DateTime <dttm>, TransectID <chr>

```

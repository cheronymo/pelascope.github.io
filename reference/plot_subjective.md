# Plot Subjective

Create a table and a stackle bar, to get information regarding the
subjective condition in the effort table.

## Usage

``` r
plot_subjective(effort_table_brut)
```

## Arguments

- effort_table_brut:

  dataframe. Effort table brut before any cleaning.

## Value

plot. Stack bar counting the number of subjective value in the effort
table

## Examples

``` r
plot_subjective(effort_table_brut = data_effort_brut)
#> $table_subjective
#> # A tibble: 8 × 2
#> # Groups:   Subjective [8]
#>   Subjective Count
#>   <chr>      <int>
#> 1 EE            22
#> 2 EG             6
#> 3 GG           356
#> 4 GM            98
#> 5 GP             9
#> 6 MM           213
#> 7 MP            66
#> 8 PP            46
#> 
#> $figure_subjective

#> 
```

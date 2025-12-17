# Estimate Effective Strip Width (ESW)

Estimate ESW values based on half-normal (hn) detection function. The
function needs dataframe created from 'sight_bindSegID' (AmbiDSM) and
'sightings_to_effort' (pelascope).

## Usage

``` r
estimate_esw(
  data_sight,
  data_effort,
  species = "DELDEL",
  variable = "Beaufort",
  var_factor = FALSE
)
```

## Arguments

- data_sight:

  dataframe. Sightings dataset created with 'sight_bindSegID'

- data_effort:

  sf dataframe. Effort table created with 'sightings_to_effort'

- species:

  character. Species selected to calculated ESW.

- variable:

  character. Variable to consider in the ESW calculation.

- var_factor:

  TRUE/FULSE. If TRUE, all variable are concidered as factor.

## Value

Dataframe with ESW values per variables for the selected species

## Examples

``` r
estimate_esw(data_sight = pelascope::Sigthings_with_SegID, 
             data_effort = pelascope::data_effort_with_sightings,
             species = "FULGLA", 
             variable = c("Beaufort"), 
             var_factor = FALSE)
#> Calling Distance package, for more information visit:
#> <https://www.st-andrews.ac.uk/mathematics-statistics/research/impact/distance/>.
#> 
#> ── Data cleaning ──
#> 
#> There are 127 sightings in the dataset selected.
#> 
#> ── Model selection ──
#> 
#> Fitting half-normal key function
#> AIC= -138.218
#> ── Best model prediction ──
#> 
#> Fitting half-normal key function
#> AIC= -138.218
#> ESW values estimated, please check units.
#> 
#> ── Update Effort Table ──
#> 
#> $plot_esw

#> 
#> $data_esw
#>   Beaufort      mean         sd       Q_25      Q_97
#> 1        0 0.2301667 0.10558769 0.07567276 0.4634014
#> 2        1 0.2635680 0.08785667 0.12022430 0.4416732
#> 3        2 0.3053290 0.06416382 0.18967137 0.4308413
#> 4        3 0.3547418 0.03820593 0.28164019 0.4282815
#> 5        4 0.4047816 0.03576154 0.32567692 0.4714620
#> 6        5 0.4463421 0.05518480 0.32008774 0.5355391
#> 7        6 0.4767562 0.07199874 0.30144820 0.5734886
#> 
#> $model_selection
#>          model       AIC det_fun
#> 1 1 + Beaufort -138.2179      hn
#> 
#> $effort_output
#> Simple feature collection with 390 features and 16 fields
#> Geometry type: POINT
#> Dimension:     XY
#> Bounding box:  xmin: -5.657199 ymin: 43.66589 xmax: -1.253505 ymax: 48.31222
#> Geodetic CRS:  WGS 84
#> # A tibble: 390 × 17
#>    Beaufort TransectID         plateform         n_obs LegID Start_time         
#>       <dbl> <chr>              <chr>             <dbl> <chr> <dttm>             
#>  1        0 TR_Pelgas_25052023 upper_bridge_out…     2 2505… 2023-05-25 04:57:07
#>  2        1 TR_Pelgas_04052023 upper_bridge_out…     2 0405… 2023-05-04 11:42:53
#>  3        1 TR_Pelgas_05052023 upper_bridge_out…     2 0505… 2023-05-05 13:56:44
#>  4        1 TR_Pelgas_05052023 upper_bridge_out…     2 0505… 2023-05-05 13:56:44
#>  5        1 TR_Pelgas_05052023 upper_bridge_out…     2 0505… 2023-05-05 13:56:44
#>  6        1 TR_Pelgas_05052023 upper_bridge_out…     2 0505… 2023-05-05 13:56:44
#>  7        1 TR_Pelgas_05052023 upper_bridge_out…     2 0505… 2023-05-05 16:09:17
#>  8        1 TR_Pelgas_18052023 upper_bridge_out…     2 1805… 2023-05-18 11:33:05
#>  9        1 TR_Pelgas_22052023 upper_bridge_out…     2 2205… 2023-05-22 15:03:10
#> 10        1 TR_Pelgas_27052023 upper_bridge_out…     2 2705… 2023-05-27 13:24:10
#> # ℹ 380 more rows
#> # ℹ 11 more variables: DateTime <dttm>, End_time <dttm>, SegID <chr>,
#> #   Effort <dbl>, geometry <POINT [°]>, det.FULGLA <dbl>, ind.FULGLA <dbl>,
#> #   mean_esw_FULGLA <dbl>, sd_esw_FULGLA <dbl>, Q25_esw_FULGLA <dbl>,
#> #   Q75_esw_FULGLA <dbl>
#> 

estimate_esw(data_sight = pelascope::Sigthings_with_SegID, 
             data_effort = pelascope::data_effort_with_sightings,
             species = c("DELDEL", "DELSPP") , 
             variable = c("Beaufort", "plateform"), 
             var_factor = FALSE)
#> Calling Distance package, for more information visit:
#> <https://www.st-andrews.ac.uk/mathematics-statistics/research/impact/distance/>.
#> 
#> ── Data cleaning ──
#> 
#> There are 295 sightings in the dataset selected.
#> 
#> ── Model selection ──
#> 
#> Fitting half-normal key function
#> AIC= -422.815
#> Fitting half-normal key function
#> AIC= -415.657
#> Fitting half-normal key function
#> AIC= -424.395
#> ── Best model prediction ──
#> 
#> Fitting half-normal key function
#> AIC= -424.395
#> ESW values estimated, please check units.
#> 
#> ── Update Effort Table ──
#> 
#> $plot_esw

#> 
#> $data_esw
#>   Beaufort      mean         sd      Q_25      Q_97
#> 1        0 0.4371519 0.04455027 0.3434456 0.5149842
#> 2        1 0.4002283 0.03687308 0.3242841 0.4678914
#> 3        2 0.3595816 0.02661658 0.3054443 0.4098677
#> 4        3 0.3174917 0.01631235 0.2854706 0.3505644
#> 5        4 0.2768489 0.01277467 0.2527529 0.3032643
#> 6        5 0.2399920 0.01798416 0.2072472 0.2760395
#> 7        6 0.2078533 0.02427721 0.1637518 0.2582694
#> 
#> $model_selection
#>                      model       AIC det_fun
#> 1             1 + Beaufort -424.3949      hn
#> 2 1 + Beaufort + plateform -422.8151      hn
#> 3            1 + plateform -415.6568      hn
#> 
#> $effort_output
#> Simple feature collection with 390 features and 20 fields
#> Geometry type: POINT
#> Dimension:     XY
#> Bounding box:  xmin: -5.657199 ymin: 43.66589 xmax: -1.253505 ymax: 48.31222
#> Geodetic CRS:  WGS 84
#> # A tibble: 390 × 21
#>    Beaufort TransectID         plateform         n_obs LegID Start_time         
#>       <dbl> <chr>              <chr>             <dbl> <chr> <dttm>             
#>  1        0 TR_Pelgas_25052023 upper_bridge_out…     2 2505… 2023-05-25 04:57:07
#>  2        1 TR_Pelgas_04052023 upper_bridge_out…     2 0405… 2023-05-04 11:42:53
#>  3        1 TR_Pelgas_05052023 upper_bridge_out…     2 0505… 2023-05-05 13:56:44
#>  4        1 TR_Pelgas_05052023 upper_bridge_out…     2 0505… 2023-05-05 13:56:44
#>  5        1 TR_Pelgas_05052023 upper_bridge_out…     2 0505… 2023-05-05 13:56:44
#>  6        1 TR_Pelgas_05052023 upper_bridge_out…     2 0505… 2023-05-05 13:56:44
#>  7        1 TR_Pelgas_05052023 upper_bridge_out…     2 0505… 2023-05-05 16:09:17
#>  8        1 TR_Pelgas_18052023 upper_bridge_out…     2 1805… 2023-05-18 11:33:05
#>  9        1 TR_Pelgas_22052023 upper_bridge_out…     2 2205… 2023-05-22 15:03:10
#> 10        1 TR_Pelgas_27052023 upper_bridge_out…     2 2705… 2023-05-27 13:24:10
#> # ℹ 380 more rows
#> # ℹ 15 more variables: DateTime <dttm>, End_time <dttm>, SegID <chr>,
#> #   Effort <dbl>, geometry <POINT [°]>, det.DELDEL <int>, ind.DELDEL <int>,
#> #   det.DELSPP <int>, ind.DELSPP <int>, ind.DELDEL_DELSPP <dbl>,
#> #   det.DELDEL_DELSPP <dbl>, mean_esw_DELDEL_DELSPP <dbl>,
#> #   sd_esw_DELDEL_DELSPP <dbl>, Q25_esw_DELDEL_DELSPP <dbl>,
#> #   Q75_esw_DELDEL_DELSPP <dbl>
#> 

```

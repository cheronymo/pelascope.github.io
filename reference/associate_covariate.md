# Associate Covariates

Associate environmental covariates to effort table, based on monthly
raster store in unique folder.

## Usage

``` r
associate_covariate(
  effort_table,
  raster_folder,
  temporal = "month",
  check_sources = FALSE
)
```

## Arguments

- effort_table:

  sf dataframe. SF object produce in the pelascope workflow.

- raster_folder:

  path. Path leading to folder with monthly raster.

- temporal:

  character. "month", "week or "day". Inform the temporal definition set
  in the rasters.

- check_sources:

  boolean. Use to check sources for each effort raw. Add a column with
  raster of origin.

## Value

effort table with covariates

## Examples

``` r

list_file_tif <- system.file(package = "pelascope", "tif_covariables")

associate_covariate(effort_table = pelascope::data_effort_with_sightings,
                    raster_folder = list_file_tif,
                    temporal = "month", 
                    check_sources = FALSE)
#> Simple feature collection with 390 features and 228 fields
#> Geometry type: POINT
#> Dimension:     XY
#> Bounding box:  xmin: -5.657199 ymin: 43.66589 xmax: -1.253505 ymax: 48.31222
#> Geodetic CRS:  WGS 84
#> # A tibble: 390 × 229
#>    Beaufort TransectID         plateform         n_obs LegID Start_time         
#>  *    <dbl> <chr>              <chr>             <dbl> <chr> <dttm>             
#>  1        2 TR_Pelgas_30042023 upper_bridge_out…     2 3004… 2023-04-30 06:37:02
#>  2        3 TR_Pelgas_30042023 upper_bridge_out…     2 3004… 2023-04-30 09:10:20
#>  3        3 TR_Pelgas_30042023 upper_bridge_out…     2 3004… 2023-04-30 09:10:20
#>  4        3 TR_Pelgas_30042023 upper_bridge_out…     2 3004… 2023-04-30 09:10:20
#>  5        3 TR_Pelgas_30042023 upper_bridge_out…     2 3004… 2023-04-30 09:10:20
#>  6        3 TR_Pelgas_30042023 upper_bridge_out…     2 3004… 2023-04-30 09:10:20
#>  7        3 TR_Pelgas_30042023 upper_bridge_out…     2 3004… 2023-04-30 09:10:20
#>  8        3 TR_Pelgas_30042023 upper_bridge_out…     2 3004… 2023-04-30 09:10:20
#>  9        3 TR_Pelgas_30042023 upper_bridge_out…     2 3004… 2023-04-30 09:10:20
#> 10        3 TR_Pelgas_30042023 upper_bridge_out…     2 3004… 2023-04-30 09:10:20
#> # ℹ 380 more rows
#> # ℹ 223 more variables: DateTime <dttm>, End_time <dttm>, SegID <chr>,
#> #   Effort <dbl>, geometry <POINT [°]>, det.PHACAR <int>, ind.PHACAR <int>,
#> #   det.BUOY <int>, ind.BUOY <int>, det.MOTOBO <int>, ind.MOTOBO <int>,
#> #   det.LARFUS <int>, ind.LARFUS <int>, det.SULBAS <int>, ind.SULBAS <int>,
#> #   det.SAILBO <int>, ind.SAILBO <int>, det.LARGUL <int>, ind.LARGUL <int>,
#> #   det.PHAARI <int>, ind.PHAARI <int>, det.LARMAR <int>, ind.LARMAR <int>, …

```

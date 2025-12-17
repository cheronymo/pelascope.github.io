# Associate Sightings To Effort

Allows to count the number of sightings per species in each segment.

## Usage

``` r
sightings_to_effort(effort_segmented, sightings_with_SegID)
```

## Arguments

- effort_segmented:

  dataframe. The segmented effort table needs to be produce with
  'eff_segment' function from AmbiDSM. It must be an SF object.

- sightings_with_SegID:

  dataframe. The Sitghings table needs to be produce with
  'sight_bindSegID' function from AmbiDSM. It must contain the SegiID
  column.

## Value

Effort table with the number of detection (det.) and individual (ind.)
per species for each segment.

## Examples

``` r
data(data_effort_Segmented)
data(Sigthings_with_SegID)

sightings_to_effort(effort_segmented = data_effort_Segmented,
                    sightings_with_SegID = Sigthings_with_SegID)
#> Simple feature collection with 390 features and 214 fields
#> Geometry type: POINT
#> Dimension:     XY
#> Bounding box:  xmin: -5.657199 ymin: 43.66589 xmax: -1.253505 ymax: 48.31222
#> Geodetic CRS:  WGS 84
#> # A tibble: 390 × 215
#>    Beaufort TransectID         plateform         n_obs LegID Start_time         
#>  *    <dbl> <chr>              <chr>             <dbl> <chr> <dttm>             
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
#> # ℹ 209 more variables: DateTime <dttm>, End_time <dttm>, SegID <chr>,
#> #   Effort <dbl>, geometry <POINT [°]>, det.PHACAR <int>, ind.PHACAR <int>,
#> #   det.BUOY <int>, ind.BUOY <int>, det.MOTOBO <int>, ind.MOTOBO <int>,
#> #   det.LARFUS <int>, ind.LARFUS <int>, det.SULBAS <int>, ind.SULBAS <int>,
#> #   det.SAILBO <int>, ind.SAILBO <int>, det.LARGUL <int>, ind.LARGUL <int>,
#> #   det.PHAARI <int>, ind.PHAARI <int>, det.LARMAR <int>, ind.LARMAR <int>, …
```

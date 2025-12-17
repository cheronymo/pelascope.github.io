# Remove Attractor

Remove attractor behaviors from sighting table.

## Usage

``` r
remove_attractor(sighting_table, behavior = TRUE, direction = FALSE)
```

## Arguments

- sighting_table:

  dataframe. Sightings table cleaned and checked.

- behavior:

  boolean. TRUE or FALSE if needs to remove attractor behavior.

- direction:

  boolean. TRUE or FALSE if needs to remove direction 0° and 360°.

## Value

Sightings table without attractor and some stats

## Examples

``` r
remove_attractor(pelascope::Sigthings_with_SegID, 
                 behavior = TRUE, 
                 direction = FALSE)
#> → 637 attraction behaviour have been removed from the sighting table.
#> $sightings_table
#> # A tibble: 2,265 × 25
#>    survey session routeType LegID Species speciesLatin GroupSize behaviour Side 
#>    <chr>  <chr>   <chr>     <chr> <chr>   <chr>            <int> <chr>     <chr>
#>  1 PELGAS LEG1    prospect… 3004… PHACAR  Phalacrocor…         1 moving    left 
#>  2 PELGAS LEG1    prospect… 3004… PHACAR  Phalacrocor…         1 moving    left 
#>  3 PELGAS LEG1    prospect… 3004… BUOY    Fishing buo…         1 NULL      right
#>  4 PELGAS LEG1    prospect… 3004… PHACAR  Phalacrocor…         1 moving    left 
#>  5 PELGAS LEG1    prospect… 3004… MOTOBO  Small motor…         2 stationa… left 
#>  6 PELGAS LEG1    prospect… 3004… LARFUS  Larus fuscus         2 moving    right
#>  7 PELGAS LEG1    prospect… 3004… MOTOBO  Small motor…         1 moving    right
#>  8 PELGAS LEG1    prospect… 3004… SULBAS  Morus bassa…         1 moving    left 
#>  9 PELGAS LEG1    prospect… 3004… BUOY    Fishing buo…         2 NULL      left 
#> 10 PELGAS LEG1    prospect… 3004… SAILBO  Sailing boat         1 moving    right
#> # ℹ 2,255 more rows
#> # ℹ 16 more variables: Longitude <dbl>, Latitude <dbl>, DateTime <dttm>,
#> #   distance <int>, angle <int>, PerpDist <dbl>, direction <dbl>,
#> #   TransectID <chr>, DupID <int>, Date <date>, Effort <dbl>, Beaufort <dbl>,
#> #   Start_time <dttm>, End_time <dttm>, SegID <chr>, geomeff <POINT [°]>
#> 
#> $table_behavior
#> # A tibble: 35 × 3
#> # Groups:   Species, behaviour [35]
#>    Species behaviour      n
#>    <chr>   <chr>      <int>
#>  1 DELDEL  attraction   253
#>  2 LARFUS  attraction   101
#>  3 SULBAS  attraction    72
#>  4 LARGUL  attraction    63
#>  5 FULGLA  attraction    28
#>  6 LARMIC  attraction    18
#>  7 LARARG  attraction    15
#>  8 STRDEC  attraction    14
#>  9 GREGUL  attraction     9
#> 10 HIRRUS  attraction     9
#> # ℹ 25 more rows
#> 
#> $table_direction
#> # A tibble: 22 × 3
#> # Groups:   Species, direction [22]
#>    Species direction     n
#>    <chr>       <dbl> <int>
#>  1 PUFPUF        360    11
#>  2 SULBAS        360     8
#>  3 FULGLA        360     5
#>  4 LARARG        360     5
#>  5 LARGUL        360     3
#>  6 SAILBO        360     3
#>  7 DELDEL        360     2
#>  8 MOLMOL        360     2
#>  9 RISTRI        360     2
#> 10 STEHIR        360     2
#> # ℹ 12 more rows
#> 
```

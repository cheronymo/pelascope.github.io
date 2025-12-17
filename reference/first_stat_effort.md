# Descriptive Statistics On Effort Table

Making some first statistics from effort table created after counting
the number of sightings per segment (Effort_withSightings).

## Usage

``` r
first_stat_effort(data_effort, species_blocking = NULL)
```

## Arguments

- data_effort:

  sf dataframe. Effort table created by using 'sightings_to_effort',
  with the nummber of observation per segment..

- species_blocking:

  character. Species selected for the blocking. By default, the most
  abundant species.

## Value

list with a blocking map and stats on table.

## Examples

``` r
data(data_effort_with_sightings)

first_stat_effort(data_effort = data_effort_with_sightings, 
                  species_blocking = NULL)
#> 
#> ── Effort per obs is calculating ──
#> 
#> ── Effort per obs is calculating for ind.DELDEL ──
#> 
#> $distance_effort
#> [1] 4637.259
#> 
#> $distance_travel_table
#> # A tibble: 9 × 4
#> # Groups:   Beaufort, n_obs [6]
#>   Beaufort n_obs plateform            `Km Effort`
#>      <dbl> <dbl> <chr>                      <dbl>
#> 1        1     2 upper_bridge_outside       92.1 
#> 2        2     2 bridge_inside               2.66
#> 3        2     2 upper_bridge_outside      754.  
#> 4        3     2 upper_bridge_outside     1779.  
#> 5        4     2 bridge_inside              64.0 
#> 6        4     2 upper_bridge_outside     1319.  
#> 7        5     2 bridge_inside             181.  
#> 8        5     2 upper_bridge_outside      384.  
#> 9        6     2 bridge_inside              61.9 
#> 
#> $stack_bar

#> 
#> $count_ind
#>        Species n_ind
#> 1   ind.DELDEL  2157
#> 2   ind.SULBAS  1749
#> 3   ind.LARGUL  1393
#> 4   ind.LARFUS   619
#> 5   ind.PUFPUF   391
#> 6   ind.PLASTR   254
#> 7   ind.PUFMAU   158
#> 8   ind.FULGLA   155
#> 9   ind.LARARG   149
#> 10    ind.BUOY   138
#> 11  ind.STEDEL   118
#> 12  ind.STESAN   110
#> 13  ind.SAILBO   101
#> 14  ind.LARMIC    99
#> 15  ind.STEHIR    96
#> 16  ind.TURTRU    80
#> 17  ind.MOLMOL    70
#> 18  ind.TRAWLB    68
#> 19  ind.URIAAL    60
#> 20  ind.PHAARI    42
#> 21  ind.LARMAR    41
#> 22  ind.RISTRI    40
#> 23  ind.DELSPP    36
#> 24  ind.GREGUL    36
#> 25  ind.STRDEC    33
#> 26  ind.MOTOBO    31
#> 27  ind.LIMICO    29
#> 28   ind.NETBO    24
#> 29  ind.WOODTR    24
#> 30  ind.FISHTR    21
#> 31  ind.HIRRUS    21
#> 32  ind.TANKER    21
#> 33   ind.TRASH    20
#> 34  ind.PASSBO    19
#> 35  ind.GLOMEL    18
#> 36  ind.OCESPP    18
#> 37  ind.SMASHE    17
#> 38  ind.PASSER    16
#> 39  ind.CATSKU    14
#> 40  ind.ALCURI    12
#> 41  ind.FISHBO    12
#> 42  ind.CALSPP    12
#> 43  ind.STESPP    10
#> 44  ind.STECOE     9
#> 45  ind.LARFIS     8
#> 46  ind.AREINT     7
#> 47  ind.APUAPU     7
#> 48   ind.PLANE     7
#> 49  ind.CALALP     7
#> 50  ind.ALCTOR     6
#> 51  ind.HIRSPP     6
#> 52  ind.GRAGRI     6
#> 53  ind.PHACAR     5
#> 54  ind.POLYTR     5
#> 55  ind.METATR     5
#> 56  ind.THUTHY     5
#> 57  ind.STRTUR     5
#> 58  ind.CONTBO     4
#> 59  ind.PUFGRI     4
#> 60  ind.BULKBO     4
#> 61  ind.MELNIG     4
#> 62  ind.HYDPEL     4
#> 63  ind.RIPRIP     4
#> 64  ind.FRAARC     3
#> 65  ind.DEADBI     3
#> 66  ind.BLAGUL     3
#> 67   ind.SHARK     3
#> 68  ind.STEPOM     3
#> 69  ind.CHAHIA     3
#> 70  ind.PHYCOL     2
#> 71  ind.LARSPP     2
#> 72  ind.BALSPP     2
#> 73  ind.FALSPP     2
#> 74  ind.COLPAL     2
#> 75  ind.PRIGLA     2
#> 76  ind.PLALEU     2
#> 77  ind.STEPAR     2
#> 78  ind.CARGOB     2
#> 79  ind.PUFSPP     2
#> 80  ind.LONGBO     2
#> 81  ind.COLLIV     2
#> 82  ind.FERRYB     2
#> 83  ind.CHLNIG     2
#> 84  ind.DELURB     2
#> 85  ind.PHASPP     1
#> 86   ind.POTBO     1
#> 87  ind.RESEBO     1
#> 88  ind.ALCSPP     1
#> 89  ind.COLSPP     1
#> 90  ind.REGIGN     1
#> 91  ind.ZIPSPP     1
#> 92  ind.CORCOR     1
#> 93  ind.PANHAL     1
#> 94  ind.MEDCET     1
#> 95   ind.JELLY     1
#> 96  ind.STERCO     1
#> 97  ind.LARMEL     1
#> 98  ind.MEDTER     1
#> 99    ind.BOAT     1
#> 100 ind.LARMIN     1
#> 101 ind.PHYSPP     1
#> 102 ind.NUMSPP     1
#> 103 ind.LARCAN     1
#> 
#> $count_det
#>        Species n_detection
#> 1   det.SULBAS         634
#> 2   det.DELDEL         349
#> 3   det.LARFUS         321
#> 4   det.PLASTR         234
#> 5   det.LARGUL         230
#> 6   det.PUFPUF         172
#> 7   det.FULGLA         135
#> 8     det.BUOY         114
#> 9   det.LARARG         101
#> 10  det.SAILBO          74
#> 11  det.MOLMOL          65
#> 12  det.TRAWLB          57
#> 13  det.LARMIC          52
#> 14  det.STESAN          50
#> 15  det.URIAAL          41
#> 16  det.PUFMAU          41
#> 17  det.LARMAR          39
#> 18  det.STEHIR          36
#> 19  det.RISTRI          30
#> 20  det.MOTOBO          27
#> 21  det.GREGUL          27
#> 22  det.PHAARI          26
#> 23   det.NETBO          24
#> 24  det.WOODTR          24
#> 25  det.FISHTR          21
#> 26   det.TRASH          20
#> 27  det.STRDEC          20
#> 28  det.PASSBO          19
#> 29  det.STEDEL          18
#> 30  det.SMASHE          15
#> 31  det.HIRRUS          15
#> 32  det.DELSPP          13
#> 33  det.FISHBO          12
#> 34  det.TANKER          12
#> 35  det.CATSKU          11
#> 36  det.PASSER          11
#> 37  det.LARFIS           8
#> 38  det.TURTRU           8
#> 39  det.OCESPP           7
#> 40  det.ALCURI           6
#> 41  det.STESPP           6
#> 42  det.POLYTR           5
#> 43  det.GLOMEL           5
#> 44  det.APUAPU           5
#> 45  det.METATR           5
#> 46  det.STRTUR           5
#> 47  det.PHACAR           4
#> 48  det.AREINT           4
#> 49  det.CONTBO           4
#> 50   det.PLANE           4
#> 51  det.HIRSPP           4
#> 52  det.PUFGRI           4
#> 53  det.BULKBO           4
#> 54  det.CALSPP           4
#> 55  det.ALCTOR           3
#> 56  det.DEADBI           3
#> 57   det.SHARK           3
#> 58  det.STECOE           3
#> 59  det.FRAARC           2
#> 60  det.PHYCOL           2
#> 61  det.LIMICO           2
#> 62  det.LARSPP           2
#> 63  det.FALSPP           2
#> 64  det.COLPAL           2
#> 65  det.BLAGUL           2
#> 66  det.PRIGLA           2
#> 67  det.STEPAR           2
#> 68  det.CARGOB           2
#> 69  det.PUFSPP           2
#> 70  det.LONGBO           2
#> 71  det.GRAGRI           2
#> 72  det.COLLIV           2
#> 73  det.HYDPEL           2
#> 74  det.FERRYB           2
#> 75  det.PHASPP           1
#> 76   det.POTBO           1
#> 77  det.RESEBO           1
#> 78  det.ALCSPP           1
#> 79  det.COLSPP           1
#> 80  det.REGIGN           1
#> 81  det.ZIPSPP           1
#> 82  det.BALSPP           1
#> 83  det.CORCOR           1
#> 84  det.PANHAL           1
#> 85  det.THUTHY           1
#> 86  det.PLALEU           1
#> 87  det.MEDCET           1
#> 88   det.JELLY           1
#> 89  det.STEPOM           1
#> 90  det.MELNIG           1
#> 91  det.STERCO           1
#> 92  det.LARMEL           1
#> 93  det.CHAHIA           1
#> 94  det.MEDTER           1
#> 95    det.BOAT           1
#> 96  det.LARMIN           1
#> 97  det.PHYSPP           1
#> 98  det.CHLNIG           1
#> 99  det.NUMSPP           1
#> 100 det.DELURB           1
#> 101 det.CALALP           1
#> 102 det.LARCAN           1
#> 103 det.RIPRIP           1
#> 
#> $plot_general_blocking

#> 
#> $gpkg_general_blocking
#> Simple feature collection with 2091 features and 1 field
#> Geometry type: POINT
#> Dimension:     XY
#> Bounding box:  xmin: -6 ymin: 44 xmax: -1 ymax: 48
#> Geodetic CRS:  WGS 84
#> First 10 features:
#>    Mean_value        geometry
#> 1          NA   POINT (-6 44)
#> 2          NA POINT (-5.9 44)
#> 3          NA POINT (-5.8 44)
#> 4          NA POINT (-5.7 44)
#> 5          NA POINT (-5.6 44)
#> 6          NA POINT (-5.5 44)
#> 7          NA POINT (-5.4 44)
#> 8          NA POINT (-5.3 44)
#> 9          NA POINT (-5.2 44)
#> 10         NA POINT (-5.1 44)
#> 
#> $blocking_per_species
#> $blocking_per_species$ind.DELDEL
#> $blocking_per_species$ind.DELDEL$data
#> Simple feature collection with 2091 features and 1 field
#> Geometry type: POINT
#> Dimension:     XY
#> Bounding box:  xmin: -6 ymin: 44 xmax: -1 ymax: 48
#> Geodetic CRS:  WGS 84
#> First 10 features:
#>    Mean_value        geometry
#> 1          NA   POINT (-6 44)
#> 2          NA POINT (-5.9 44)
#> 3          NA POINT (-5.8 44)
#> 4          NA POINT (-5.7 44)
#> 5          NA POINT (-5.6 44)
#> 6          NA POINT (-5.5 44)
#> 7          NA POINT (-5.4 44)
#> 8          NA POINT (-5.3 44)
#> 9          NA POINT (-5.2 44)
#> 10         NA POINT (-5.1 44)
#> 
#> $blocking_per_species$ind.DELDEL$map

#> 
#> 
#> 

first_stat_effort(data_effort = data_effort_with_sightings, 
                  species_blocking = c("DELDEL", "FULGLA"))
#> ── Effort per obs is calculating ──
#> 
#> ── Effort per obs is calculating for ind.DELDEL ──
#> 
#> ── Effort per obs is calculating for ind.FULGLA ──
#> 
#> $distance_effort
#> [1] 4637.259
#> 
#> $distance_travel_table
#> # A tibble: 9 × 4
#> # Groups:   Beaufort, n_obs [6]
#>   Beaufort n_obs plateform            `Km Effort`
#>      <dbl> <dbl> <chr>                      <dbl>
#> 1        1     2 upper_bridge_outside       92.1 
#> 2        2     2 bridge_inside               2.66
#> 3        2     2 upper_bridge_outside      754.  
#> 4        3     2 upper_bridge_outside     1779.  
#> 5        4     2 bridge_inside              64.0 
#> 6        4     2 upper_bridge_outside     1319.  
#> 7        5     2 bridge_inside             181.  
#> 8        5     2 upper_bridge_outside      384.  
#> 9        6     2 bridge_inside              61.9 
#> 
#> $stack_bar

#> 
#> $count_ind
#>        Species n_ind
#> 1   ind.DELDEL  2157
#> 2   ind.SULBAS  1749
#> 3   ind.LARGUL  1393
#> 4   ind.LARFUS   619
#> 5   ind.PUFPUF   391
#> 6   ind.PLASTR   254
#> 7   ind.PUFMAU   158
#> 8   ind.FULGLA   155
#> 9   ind.LARARG   149
#> 10    ind.BUOY   138
#> 11  ind.STEDEL   118
#> 12  ind.STESAN   110
#> 13  ind.SAILBO   101
#> 14  ind.LARMIC    99
#> 15  ind.STEHIR    96
#> 16  ind.TURTRU    80
#> 17  ind.MOLMOL    70
#> 18  ind.TRAWLB    68
#> 19  ind.URIAAL    60
#> 20  ind.PHAARI    42
#> 21  ind.LARMAR    41
#> 22  ind.RISTRI    40
#> 23  ind.DELSPP    36
#> 24  ind.GREGUL    36
#> 25  ind.STRDEC    33
#> 26  ind.MOTOBO    31
#> 27  ind.LIMICO    29
#> 28   ind.NETBO    24
#> 29  ind.WOODTR    24
#> 30  ind.FISHTR    21
#> 31  ind.HIRRUS    21
#> 32  ind.TANKER    21
#> 33   ind.TRASH    20
#> 34  ind.PASSBO    19
#> 35  ind.GLOMEL    18
#> 36  ind.OCESPP    18
#> 37  ind.SMASHE    17
#> 38  ind.PASSER    16
#> 39  ind.CATSKU    14
#> 40  ind.ALCURI    12
#> 41  ind.FISHBO    12
#> 42  ind.CALSPP    12
#> 43  ind.STESPP    10
#> 44  ind.STECOE     9
#> 45  ind.LARFIS     8
#> 46  ind.AREINT     7
#> 47  ind.APUAPU     7
#> 48   ind.PLANE     7
#> 49  ind.CALALP     7
#> 50  ind.ALCTOR     6
#> 51  ind.HIRSPP     6
#> 52  ind.GRAGRI     6
#> 53  ind.PHACAR     5
#> 54  ind.POLYTR     5
#> 55  ind.METATR     5
#> 56  ind.THUTHY     5
#> 57  ind.STRTUR     5
#> 58  ind.CONTBO     4
#> 59  ind.PUFGRI     4
#> 60  ind.BULKBO     4
#> 61  ind.MELNIG     4
#> 62  ind.HYDPEL     4
#> 63  ind.RIPRIP     4
#> 64  ind.FRAARC     3
#> 65  ind.DEADBI     3
#> 66  ind.BLAGUL     3
#> 67   ind.SHARK     3
#> 68  ind.STEPOM     3
#> 69  ind.CHAHIA     3
#> 70  ind.PHYCOL     2
#> 71  ind.LARSPP     2
#> 72  ind.BALSPP     2
#> 73  ind.FALSPP     2
#> 74  ind.COLPAL     2
#> 75  ind.PRIGLA     2
#> 76  ind.PLALEU     2
#> 77  ind.STEPAR     2
#> 78  ind.CARGOB     2
#> 79  ind.PUFSPP     2
#> 80  ind.LONGBO     2
#> 81  ind.COLLIV     2
#> 82  ind.FERRYB     2
#> 83  ind.CHLNIG     2
#> 84  ind.DELURB     2
#> 85  ind.PHASPP     1
#> 86   ind.POTBO     1
#> 87  ind.RESEBO     1
#> 88  ind.ALCSPP     1
#> 89  ind.COLSPP     1
#> 90  ind.REGIGN     1
#> 91  ind.ZIPSPP     1
#> 92  ind.CORCOR     1
#> 93  ind.PANHAL     1
#> 94  ind.MEDCET     1
#> 95   ind.JELLY     1
#> 96  ind.STERCO     1
#> 97  ind.LARMEL     1
#> 98  ind.MEDTER     1
#> 99    ind.BOAT     1
#> 100 ind.LARMIN     1
#> 101 ind.PHYSPP     1
#> 102 ind.NUMSPP     1
#> 103 ind.LARCAN     1
#> 
#> $count_det
#>        Species n_detection
#> 1   det.SULBAS         634
#> 2   det.DELDEL         349
#> 3   det.LARFUS         321
#> 4   det.PLASTR         234
#> 5   det.LARGUL         230
#> 6   det.PUFPUF         172
#> 7   det.FULGLA         135
#> 8     det.BUOY         114
#> 9   det.LARARG         101
#> 10  det.SAILBO          74
#> 11  det.MOLMOL          65
#> 12  det.TRAWLB          57
#> 13  det.LARMIC          52
#> 14  det.STESAN          50
#> 15  det.URIAAL          41
#> 16  det.PUFMAU          41
#> 17  det.LARMAR          39
#> 18  det.STEHIR          36
#> 19  det.RISTRI          30
#> 20  det.MOTOBO          27
#> 21  det.GREGUL          27
#> 22  det.PHAARI          26
#> 23   det.NETBO          24
#> 24  det.WOODTR          24
#> 25  det.FISHTR          21
#> 26   det.TRASH          20
#> 27  det.STRDEC          20
#> 28  det.PASSBO          19
#> 29  det.STEDEL          18
#> 30  det.SMASHE          15
#> 31  det.HIRRUS          15
#> 32  det.DELSPP          13
#> 33  det.FISHBO          12
#> 34  det.TANKER          12
#> 35  det.CATSKU          11
#> 36  det.PASSER          11
#> 37  det.LARFIS           8
#> 38  det.TURTRU           8
#> 39  det.OCESPP           7
#> 40  det.ALCURI           6
#> 41  det.STESPP           6
#> 42  det.POLYTR           5
#> 43  det.GLOMEL           5
#> 44  det.APUAPU           5
#> 45  det.METATR           5
#> 46  det.STRTUR           5
#> 47  det.PHACAR           4
#> 48  det.AREINT           4
#> 49  det.CONTBO           4
#> 50   det.PLANE           4
#> 51  det.HIRSPP           4
#> 52  det.PUFGRI           4
#> 53  det.BULKBO           4
#> 54  det.CALSPP           4
#> 55  det.ALCTOR           3
#> 56  det.DEADBI           3
#> 57   det.SHARK           3
#> 58  det.STECOE           3
#> 59  det.FRAARC           2
#> 60  det.PHYCOL           2
#> 61  det.LIMICO           2
#> 62  det.LARSPP           2
#> 63  det.FALSPP           2
#> 64  det.COLPAL           2
#> 65  det.BLAGUL           2
#> 66  det.PRIGLA           2
#> 67  det.STEPAR           2
#> 68  det.CARGOB           2
#> 69  det.PUFSPP           2
#> 70  det.LONGBO           2
#> 71  det.GRAGRI           2
#> 72  det.COLLIV           2
#> 73  det.HYDPEL           2
#> 74  det.FERRYB           2
#> 75  det.PHASPP           1
#> 76   det.POTBO           1
#> 77  det.RESEBO           1
#> 78  det.ALCSPP           1
#> 79  det.COLSPP           1
#> 80  det.REGIGN           1
#> 81  det.ZIPSPP           1
#> 82  det.BALSPP           1
#> 83  det.CORCOR           1
#> 84  det.PANHAL           1
#> 85  det.THUTHY           1
#> 86  det.PLALEU           1
#> 87  det.MEDCET           1
#> 88   det.JELLY           1
#> 89  det.STEPOM           1
#> 90  det.MELNIG           1
#> 91  det.STERCO           1
#> 92  det.LARMEL           1
#> 93  det.CHAHIA           1
#> 94  det.MEDTER           1
#> 95    det.BOAT           1
#> 96  det.LARMIN           1
#> 97  det.PHYSPP           1
#> 98  det.CHLNIG           1
#> 99  det.NUMSPP           1
#> 100 det.DELURB           1
#> 101 det.CALALP           1
#> 102 det.LARCAN           1
#> 103 det.RIPRIP           1
#> 
#> $plot_general_blocking

#> 
#> $gpkg_general_blocking
#> Simple feature collection with 2091 features and 1 field
#> Geometry type: POINT
#> Dimension:     XY
#> Bounding box:  xmin: -6 ymin: 44 xmax: -1 ymax: 48
#> Geodetic CRS:  WGS 84
#> First 10 features:
#>    Mean_value        geometry
#> 1          NA   POINT (-6 44)
#> 2          NA POINT (-5.9 44)
#> 3          NA POINT (-5.8 44)
#> 4          NA POINT (-5.7 44)
#> 5          NA POINT (-5.6 44)
#> 6          NA POINT (-5.5 44)
#> 7          NA POINT (-5.4 44)
#> 8          NA POINT (-5.3 44)
#> 9          NA POINT (-5.2 44)
#> 10         NA POINT (-5.1 44)
#> 
#> $blocking_per_species
#> $blocking_per_species$ind.DELDEL
#> $blocking_per_species$ind.DELDEL$data
#> Simple feature collection with 2091 features and 1 field
#> Geometry type: POINT
#> Dimension:     XY
#> Bounding box:  xmin: -6 ymin: 44 xmax: -1 ymax: 48
#> Geodetic CRS:  WGS 84
#> First 10 features:
#>    Mean_value        geometry
#> 1          NA   POINT (-6 44)
#> 2          NA POINT (-5.9 44)
#> 3          NA POINT (-5.8 44)
#> 4          NA POINT (-5.7 44)
#> 5          NA POINT (-5.6 44)
#> 6          NA POINT (-5.5 44)
#> 7          NA POINT (-5.4 44)
#> 8          NA POINT (-5.3 44)
#> 9          NA POINT (-5.2 44)
#> 10         NA POINT (-5.1 44)
#> 
#> $blocking_per_species$ind.DELDEL$map

#> 
#> 
#> $blocking_per_species$ind.FULGLA
#> $blocking_per_species$ind.FULGLA$data
#> Simple feature collection with 2091 features and 1 field
#> Geometry type: POINT
#> Dimension:     XY
#> Bounding box:  xmin: -6 ymin: 44 xmax: -1 ymax: 48
#> Geodetic CRS:  WGS 84
#> First 10 features:
#>    Mean_value        geometry
#> 1          NA   POINT (-6 44)
#> 2          NA POINT (-5.9 44)
#> 3          NA POINT (-5.8 44)
#> 4          NA POINT (-5.7 44)
#> 5          NA POINT (-5.6 44)
#> 6          NA POINT (-5.5 44)
#> 7          NA POINT (-5.4 44)
#> 8          NA POINT (-5.3 44)
#> 9          NA POINT (-5.2 44)
#> 10         NA POINT (-5.1 44)
#> 
#> $blocking_per_species$ind.FULGLA$map

#> 
#> 
#> 
```

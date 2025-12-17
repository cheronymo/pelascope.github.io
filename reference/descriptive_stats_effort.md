# Descriptive Statistics On Effort Table

Making some first statistics from effort table created after counting
the number of sightings per segment (Effort_withSightings).

## Usage

``` r
descriptive_stats_effort(data_effort, species_blocking = NULL)
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

descriptive_stats_effort(data_effort = data_effort_with_sightings, 
                  species_blocking = NULL)
#> 
#> ── Effort per obs is calculating ──
#> 
#> ── Effort per obs is calculating for ind.DELDEL ──
#> 
#> $distance_effort
#> 3988.769 [km]
#> 
#> $distance_travel_table
#> # A tibble: 11 × 4
#> # Groups:   Beaufort, n_obs [7]
#>    Beaufort n_obs plateform            `Km Effort`
#>       <dbl> <dbl> <chr>                      <dbl>
#>  1        0     2 upper_bridge_outside      14.6  
#>  2        1     2 upper_bridge_outside      71.7  
#>  3        2     2 bridge_inside              2.66 
#>  4        2     2 upper_bridge_outside     538.   
#>  5        3     2 upper_bridge_outside    1486.   
#>  6        4     2 bridge_inside             68.8  
#>  7        4     2 upper_bridge_outside    1249.   
#>  8        5     2 bridge_inside            127.   
#>  9        5     2 upper_bridge_outside     368.   
#> 10        6     2 bridge_inside             61.9  
#> 11        6     2 upper_bridge_outside       0.700
#> 
#> $stack_bar

#> 
#> $map_beaufort

#> 
#> $count_ind
#>        Species n_ind
#> 1   ind.DELDEL  1788
#> 2   ind.SULBAS  1690
#> 3   ind.LARGUL  1138
#> 4   ind.LARFUS   591
#> 5   ind.PUFPUF   333
#> 6   ind.PLASTR   218
#> 7   ind.LARARG   153
#> 8   ind.PUFMAU   147
#> 9   ind.FULGLA   142
#> 10    ind.BUOY   114
#> 11  ind.STESAN   106
#> 12  ind.SAILBO    97
#> 13  ind.STEDEL    96
#> 14  ind.STEHIR    77
#> 15  ind.TURTRU    72
#> 16  ind.LARMIC    69
#> 17  ind.TRAWLB    65
#> 18  ind.MOLMOL    60
#> 19  ind.URIAAL    58
#> 20  ind.LIMICO    49
#> 21  ind.RISTRI    42
#> 22  ind.PHAARI    39
#> 23  ind.LARMAR    37
#> 24  ind.GREGUL    34
#> 25  ind.MOTOBO    31
#> 26  ind.STRDEC    31
#> 27  ind.WOODTR    24
#> 28  ind.FISHTR    22
#> 29   ind.NETBO    22
#> 30  ind.DELSPP    20
#> 31  ind.GLOMEL    18
#> 32  ind.PASSBO    18
#> 33  ind.TANKER    17
#> 34  ind.SMASHE    15
#> 35  ind.PASSER    15
#> 36  ind.HIRRUS    15
#> 37   ind.TRASH    14
#> 38  ind.OCESPP    14
#> 39  ind.ALCURI    12
#> 40  ind.CATSKU    12
#> 41  ind.CALSPP    12
#> 42  ind.FISHBO    10
#> 43  ind.APUAPU     9
#> 44  ind.STESPP     9
#> 45  ind.LARFIS     8
#> 46   ind.PLANE     7
#> 47  ind.GRAGRI     7
#> 48  ind.CALALP     7
#> 49  ind.ALCTOR     6
#> 50  ind.PHACAR     5
#> 51  ind.METATR     5
#> 52  ind.THUTHY     5
#> 53  ind.HIRSPP     5
#> 54  ind.POLYTR     4
#> 55  ind.AREINT     4
#> 56  ind.CONTBO     4
#> 57  ind.CHLNIG     4
#> 58  ind.STRTUR     4
#> 59  ind.BULKBO     4
#> 60  ind.MELNIG     4
#> 61  ind.HYDPEL     4
#> 62  ind.RIPRIP     4
#> 63  ind.FRAARC     3
#> 64  ind.DEADBI     3
#> 65  ind.STEPOM     3
#> 66  ind.PUFGRI     3
#> 67  ind.CHAHIA     3
#> 68  ind.STECOE     3
#> 69  ind.COLSPP     2
#> 70  ind.PHYCOL     2
#> 71  ind.FALSPP     2
#> 72  ind.COLPAL     2
#> 73  ind.LARMEL     2
#> 74  ind.PLALEU     2
#> 75  ind.CARGOB     2
#> 76  ind.LONGBO     2
#> 77  ind.COLLIV     2
#> 78  ind.FERRYB     2
#> 79  ind.DELURB     2
#> 80  ind.PHASPP     1
#> 81   ind.POTBO     1
#> 82  ind.RESEBO     1
#> 83  ind.ALCSPP     1
#> 84  ind.REGIGN     1
#> 85  ind.ZIPSPP     1
#> 86  ind.CORCOR     1
#> 87  ind.PRIGLA     1
#> 88  ind.PANHAL     1
#> 89   ind.JELLY     1
#> 90  ind.STEPAR     1
#> 91  ind.STERCO     1
#> 92  ind.MEDTER     1
#> 93    ind.BOAT     1
#> 94  ind.LARSPP     1
#> 95  ind.LARMIN     1
#> 96  ind.PHYSPP     1
#> 97  ind.NUMPHA     1
#> 98  ind.PHYTRO     1
#> 99  ind.LARCAN     1
#> 100 ind.PUFSPP     1
#> 101 ind.LARRID     1
#> 102 ind.ACRSCI     1
#> 
#> $count_det
#>        Species n_detection
#> 1   det.SULBAS         580
#> 2   det.LARFUS         293
#> 3   det.DELDEL         286
#> 4   det.PLASTR         204
#> 5   det.LARGUL         203
#> 6   det.PUFPUF         157
#> 7   det.FULGLA         127
#> 8   det.LARARG          95
#> 9     det.BUOY          92
#> 10  det.SAILBO          70
#> 11  det.MOLMOL          56
#> 12  det.TRAWLB          54
#> 13  det.STESAN          47
#> 14  det.URIAAL          39
#> 15  det.LARMAR          36
#> 16  det.LARMIC          36
#> 17  det.PUFMAU          32
#> 18  det.RISTRI          31
#> 19  det.STEHIR          31
#> 20  det.MOTOBO          27
#> 21  det.GREGUL          25
#> 22  det.WOODTR          24
#> 23  det.PHAARI          23
#> 24  det.FISHTR          22
#> 25   det.NETBO          22
#> 26  det.STRDEC          20
#> 27  det.PASSBO          18
#> 28  det.STEDEL          15
#> 29   det.TRASH          14
#> 30  det.SMASHE          13
#> 31  det.HIRRUS          12
#> 32  det.PASSER          10
#> 33  det.FISHBO          10
#> 34  det.CATSKU           9
#> 35  det.DELSPP           9
#> 36  det.LARFIS           8
#> 37  det.TANKER           8
#> 38  det.TURTRU           7
#> 39  det.ALCURI           6
#> 40  det.APUAPU           6
#> 41  det.GLOMEL           5
#> 42  det.METATR           5
#> 43  det.OCESPP           5
#> 44  det.STESPP           5
#> 45  det.PHACAR           4
#> 46  det.POLYTR           4
#> 47  det.CONTBO           4
#> 48   det.PLANE           4
#> 49  det.STRTUR           4
#> 50  det.BULKBO           4
#> 51  det.CALSPP           4
#> 52  det.ALCTOR           3
#> 53  det.DEADBI           3
#> 54  det.LIMICO           3
#> 55  det.HIRSPP           3
#> 56  det.GRAGRI           3
#> 57  det.PUFGRI           3
#> 58  det.FRAARC           2
#> 59  det.COLSPP           2
#> 60  det.AREINT           2
#> 61  det.PHYCOL           2
#> 62  det.FALSPP           2
#> 63  det.COLPAL           2
#> 64  det.LARMEL           2
#> 65  det.CHLNIG           2
#> 66  det.CARGOB           2
#> 67  det.LONGBO           2
#> 68  det.STECOE           2
#> 69  det.COLLIV           2
#> 70  det.HYDPEL           2
#> 71  det.FERRYB           2
#> 72  det.PHASPP           1
#> 73   det.POTBO           1
#> 74  det.RESEBO           1
#> 75  det.ALCSPP           1
#> 76  det.REGIGN           1
#> 77  det.ZIPSPP           1
#> 78  det.CORCOR           1
#> 79  det.PRIGLA           1
#> 80  det.PANHAL           1
#> 81  det.THUTHY           1
#> 82  det.PLALEU           1
#> 83   det.JELLY           1
#> 84  det.STEPOM           1
#> 85  det.STEPAR           1
#> 86  det.MELNIG           1
#> 87  det.STERCO           1
#> 88  det.CHAHIA           1
#> 89  det.MEDTER           1
#> 90    det.BOAT           1
#> 91  det.LARSPP           1
#> 92  det.LARMIN           1
#> 93  det.PHYSPP           1
#> 94  det.NUMPHA           1
#> 95  det.DELURB           1
#> 96  det.PHYTRO           1
#> 97  det.CALALP           1
#> 98  det.LARCAN           1
#> 99  det.PUFSPP           1
#> 100 det.RIPRIP           1
#> 101 det.LARRID           1
#> 102 det.ACRSCI           1
#> 
#> $plot_general_blocking

#> 
#> $gpkg_general_blocking
#> Simple feature collection with 3800 features and 1 field
#> Geometry type: POLYGON
#> Dimension:     XY
#> Bounding box:  xmin: -5.749218 ymin: 43.57561 xmax: -1.16781 ymax: 48.37816
#> Geodetic CRS:  WGS 84
#> First 10 features:
#>    Mean_value                       geometry
#> 1          NA POLYGON ((-5.569555 43.7056...
#> 2          NA POLYGON ((-5.479723 43.7056...
#> 3          NA POLYGON ((-5.389892 43.7056...
#> 4          NA POLYGON ((-5.30006 43.70563...
#> 5          NA POLYGON ((-5.210229 43.7056...
#> 6          NA POLYGON ((-5.120397 43.7056...
#> 7          NA POLYGON ((-5.030566 43.7056...
#> 8          NA POLYGON ((-4.940734 43.7056...
#> 9          NA POLYGON ((-4.850903 43.7056...
#> 10         NA POLYGON ((-4.761071 43.7056...
#> 
#> $blocking_per_species
#> $blocking_per_species$ind.DELDEL
#> $blocking_per_species$ind.DELDEL$data
#> Simple feature collection with 3800 features and 1 field
#> Geometry type: POLYGON
#> Dimension:     XY
#> Bounding box:  xmin: -5.749218 ymin: 43.57561 xmax: -1.16781 ymax: 48.37816
#> Geodetic CRS:  WGS 84
#> First 10 features:
#>    Mean_value                       geometry
#> 1          NA POLYGON ((-5.569555 43.7056...
#> 2          NA POLYGON ((-5.479723 43.7056...
#> 3          NA POLYGON ((-5.389892 43.7056...
#> 4          NA POLYGON ((-5.30006 43.70563...
#> 5          NA POLYGON ((-5.210229 43.7056...
#> 6          NA POLYGON ((-5.120397 43.7056...
#> 7          NA POLYGON ((-5.030566 43.7056...
#> 8          NA POLYGON ((-4.940734 43.7056...
#> 9          NA POLYGON ((-4.850903 43.7056...
#> 10         NA POLYGON ((-4.761071 43.7056...
#> 
#> $blocking_per_species$ind.DELDEL$map

#> 
#> 
#> 

descriptive_stats_effort(data_effort = data_effort_with_sightings, 
                  species_blocking = c("DELDEL", "FULGLA"))
#> ── Effort per obs is calculating ──
#> 
#> ── Effort per obs is calculating for ind.DELDEL ──
#> 
#> ── Effort per obs is calculating for ind.FULGLA ──
#> 
#> $distance_effort
#> 3988.769 [km]
#> 
#> $distance_travel_table
#> # A tibble: 11 × 4
#> # Groups:   Beaufort, n_obs [7]
#>    Beaufort n_obs plateform            `Km Effort`
#>       <dbl> <dbl> <chr>                      <dbl>
#>  1        0     2 upper_bridge_outside      14.6  
#>  2        1     2 upper_bridge_outside      71.7  
#>  3        2     2 bridge_inside              2.66 
#>  4        2     2 upper_bridge_outside     538.   
#>  5        3     2 upper_bridge_outside    1486.   
#>  6        4     2 bridge_inside             68.8  
#>  7        4     2 upper_bridge_outside    1249.   
#>  8        5     2 bridge_inside            127.   
#>  9        5     2 upper_bridge_outside     368.   
#> 10        6     2 bridge_inside             61.9  
#> 11        6     2 upper_bridge_outside       0.700
#> 
#> $stack_bar

#> 
#> $map_beaufort

#> 
#> $count_ind
#>        Species n_ind
#> 1   ind.DELDEL  1788
#> 2   ind.SULBAS  1690
#> 3   ind.LARGUL  1138
#> 4   ind.LARFUS   591
#> 5   ind.PUFPUF   333
#> 6   ind.PLASTR   218
#> 7   ind.LARARG   153
#> 8   ind.PUFMAU   147
#> 9   ind.FULGLA   142
#> 10    ind.BUOY   114
#> 11  ind.STESAN   106
#> 12  ind.SAILBO    97
#> 13  ind.STEDEL    96
#> 14  ind.STEHIR    77
#> 15  ind.TURTRU    72
#> 16  ind.LARMIC    69
#> 17  ind.TRAWLB    65
#> 18  ind.MOLMOL    60
#> 19  ind.URIAAL    58
#> 20  ind.LIMICO    49
#> 21  ind.RISTRI    42
#> 22  ind.PHAARI    39
#> 23  ind.LARMAR    37
#> 24  ind.GREGUL    34
#> 25  ind.MOTOBO    31
#> 26  ind.STRDEC    31
#> 27  ind.WOODTR    24
#> 28  ind.FISHTR    22
#> 29   ind.NETBO    22
#> 30  ind.DELSPP    20
#> 31  ind.GLOMEL    18
#> 32  ind.PASSBO    18
#> 33  ind.TANKER    17
#> 34  ind.SMASHE    15
#> 35  ind.PASSER    15
#> 36  ind.HIRRUS    15
#> 37   ind.TRASH    14
#> 38  ind.OCESPP    14
#> 39  ind.ALCURI    12
#> 40  ind.CATSKU    12
#> 41  ind.CALSPP    12
#> 42  ind.FISHBO    10
#> 43  ind.APUAPU     9
#> 44  ind.STESPP     9
#> 45  ind.LARFIS     8
#> 46   ind.PLANE     7
#> 47  ind.GRAGRI     7
#> 48  ind.CALALP     7
#> 49  ind.ALCTOR     6
#> 50  ind.PHACAR     5
#> 51  ind.METATR     5
#> 52  ind.THUTHY     5
#> 53  ind.HIRSPP     5
#> 54  ind.POLYTR     4
#> 55  ind.AREINT     4
#> 56  ind.CONTBO     4
#> 57  ind.CHLNIG     4
#> 58  ind.STRTUR     4
#> 59  ind.BULKBO     4
#> 60  ind.MELNIG     4
#> 61  ind.HYDPEL     4
#> 62  ind.RIPRIP     4
#> 63  ind.FRAARC     3
#> 64  ind.DEADBI     3
#> 65  ind.STEPOM     3
#> 66  ind.PUFGRI     3
#> 67  ind.CHAHIA     3
#> 68  ind.STECOE     3
#> 69  ind.COLSPP     2
#> 70  ind.PHYCOL     2
#> 71  ind.FALSPP     2
#> 72  ind.COLPAL     2
#> 73  ind.LARMEL     2
#> 74  ind.PLALEU     2
#> 75  ind.CARGOB     2
#> 76  ind.LONGBO     2
#> 77  ind.COLLIV     2
#> 78  ind.FERRYB     2
#> 79  ind.DELURB     2
#> 80  ind.PHASPP     1
#> 81   ind.POTBO     1
#> 82  ind.RESEBO     1
#> 83  ind.ALCSPP     1
#> 84  ind.REGIGN     1
#> 85  ind.ZIPSPP     1
#> 86  ind.CORCOR     1
#> 87  ind.PRIGLA     1
#> 88  ind.PANHAL     1
#> 89   ind.JELLY     1
#> 90  ind.STEPAR     1
#> 91  ind.STERCO     1
#> 92  ind.MEDTER     1
#> 93    ind.BOAT     1
#> 94  ind.LARSPP     1
#> 95  ind.LARMIN     1
#> 96  ind.PHYSPP     1
#> 97  ind.NUMPHA     1
#> 98  ind.PHYTRO     1
#> 99  ind.LARCAN     1
#> 100 ind.PUFSPP     1
#> 101 ind.LARRID     1
#> 102 ind.ACRSCI     1
#> 
#> $count_det
#>        Species n_detection
#> 1   det.SULBAS         580
#> 2   det.LARFUS         293
#> 3   det.DELDEL         286
#> 4   det.PLASTR         204
#> 5   det.LARGUL         203
#> 6   det.PUFPUF         157
#> 7   det.FULGLA         127
#> 8   det.LARARG          95
#> 9     det.BUOY          92
#> 10  det.SAILBO          70
#> 11  det.MOLMOL          56
#> 12  det.TRAWLB          54
#> 13  det.STESAN          47
#> 14  det.URIAAL          39
#> 15  det.LARMAR          36
#> 16  det.LARMIC          36
#> 17  det.PUFMAU          32
#> 18  det.RISTRI          31
#> 19  det.STEHIR          31
#> 20  det.MOTOBO          27
#> 21  det.GREGUL          25
#> 22  det.WOODTR          24
#> 23  det.PHAARI          23
#> 24  det.FISHTR          22
#> 25   det.NETBO          22
#> 26  det.STRDEC          20
#> 27  det.PASSBO          18
#> 28  det.STEDEL          15
#> 29   det.TRASH          14
#> 30  det.SMASHE          13
#> 31  det.HIRRUS          12
#> 32  det.PASSER          10
#> 33  det.FISHBO          10
#> 34  det.CATSKU           9
#> 35  det.DELSPP           9
#> 36  det.LARFIS           8
#> 37  det.TANKER           8
#> 38  det.TURTRU           7
#> 39  det.ALCURI           6
#> 40  det.APUAPU           6
#> 41  det.GLOMEL           5
#> 42  det.METATR           5
#> 43  det.OCESPP           5
#> 44  det.STESPP           5
#> 45  det.PHACAR           4
#> 46  det.POLYTR           4
#> 47  det.CONTBO           4
#> 48   det.PLANE           4
#> 49  det.STRTUR           4
#> 50  det.BULKBO           4
#> 51  det.CALSPP           4
#> 52  det.ALCTOR           3
#> 53  det.DEADBI           3
#> 54  det.LIMICO           3
#> 55  det.HIRSPP           3
#> 56  det.GRAGRI           3
#> 57  det.PUFGRI           3
#> 58  det.FRAARC           2
#> 59  det.COLSPP           2
#> 60  det.AREINT           2
#> 61  det.PHYCOL           2
#> 62  det.FALSPP           2
#> 63  det.COLPAL           2
#> 64  det.LARMEL           2
#> 65  det.CHLNIG           2
#> 66  det.CARGOB           2
#> 67  det.LONGBO           2
#> 68  det.STECOE           2
#> 69  det.COLLIV           2
#> 70  det.HYDPEL           2
#> 71  det.FERRYB           2
#> 72  det.PHASPP           1
#> 73   det.POTBO           1
#> 74  det.RESEBO           1
#> 75  det.ALCSPP           1
#> 76  det.REGIGN           1
#> 77  det.ZIPSPP           1
#> 78  det.CORCOR           1
#> 79  det.PRIGLA           1
#> 80  det.PANHAL           1
#> 81  det.THUTHY           1
#> 82  det.PLALEU           1
#> 83   det.JELLY           1
#> 84  det.STEPOM           1
#> 85  det.STEPAR           1
#> 86  det.MELNIG           1
#> 87  det.STERCO           1
#> 88  det.CHAHIA           1
#> 89  det.MEDTER           1
#> 90    det.BOAT           1
#> 91  det.LARSPP           1
#> 92  det.LARMIN           1
#> 93  det.PHYSPP           1
#> 94  det.NUMPHA           1
#> 95  det.DELURB           1
#> 96  det.PHYTRO           1
#> 97  det.CALALP           1
#> 98  det.LARCAN           1
#> 99  det.PUFSPP           1
#> 100 det.RIPRIP           1
#> 101 det.LARRID           1
#> 102 det.ACRSCI           1
#> 
#> $plot_general_blocking

#> 
#> $gpkg_general_blocking
#> Simple feature collection with 3800 features and 1 field
#> Geometry type: POLYGON
#> Dimension:     XY
#> Bounding box:  xmin: -5.749218 ymin: 43.57561 xmax: -1.16781 ymax: 48.37816
#> Geodetic CRS:  WGS 84
#> First 10 features:
#>    Mean_value                       geometry
#> 1          NA POLYGON ((-5.569555 43.7056...
#> 2          NA POLYGON ((-5.479723 43.7056...
#> 3          NA POLYGON ((-5.389892 43.7056...
#> 4          NA POLYGON ((-5.30006 43.70563...
#> 5          NA POLYGON ((-5.210229 43.7056...
#> 6          NA POLYGON ((-5.120397 43.7056...
#> 7          NA POLYGON ((-5.030566 43.7056...
#> 8          NA POLYGON ((-4.940734 43.7056...
#> 9          NA POLYGON ((-4.850903 43.7056...
#> 10         NA POLYGON ((-4.761071 43.7056...
#> 
#> $blocking_per_species
#> $blocking_per_species$ind.DELDEL
#> $blocking_per_species$ind.DELDEL$data
#> Simple feature collection with 3800 features and 1 field
#> Geometry type: POLYGON
#> Dimension:     XY
#> Bounding box:  xmin: -5.749218 ymin: 43.57561 xmax: -1.16781 ymax: 48.37816
#> Geodetic CRS:  WGS 84
#> First 10 features:
#>    Mean_value                       geometry
#> 1          NA POLYGON ((-5.569555 43.7056...
#> 2          NA POLYGON ((-5.479723 43.7056...
#> 3          NA POLYGON ((-5.389892 43.7056...
#> 4          NA POLYGON ((-5.30006 43.70563...
#> 5          NA POLYGON ((-5.210229 43.7056...
#> 6          NA POLYGON ((-5.120397 43.7056...
#> 7          NA POLYGON ((-5.030566 43.7056...
#> 8          NA POLYGON ((-4.940734 43.7056...
#> 9          NA POLYGON ((-4.850903 43.7056...
#> 10         NA POLYGON ((-4.761071 43.7056...
#> 
#> $blocking_per_species$ind.DELDEL$map

#> 
#> 
#> $blocking_per_species$ind.FULGLA
#> $blocking_per_species$ind.FULGLA$data
#> Simple feature collection with 3800 features and 1 field
#> Geometry type: POLYGON
#> Dimension:     XY
#> Bounding box:  xmin: -5.749218 ymin: 43.57561 xmax: -1.16781 ymax: 48.37816
#> Geodetic CRS:  WGS 84
#> First 10 features:
#>    Mean_value                       geometry
#> 1          NA POLYGON ((-5.569555 43.7056...
#> 2          NA POLYGON ((-5.479723 43.7056...
#> 3          NA POLYGON ((-5.389892 43.7056...
#> 4          NA POLYGON ((-5.30006 43.70563...
#> 5          NA POLYGON ((-5.210229 43.7056...
#> 6          NA POLYGON ((-5.120397 43.7056...
#> 7          NA POLYGON ((-5.030566 43.7056...
#> 8          NA POLYGON ((-4.940734 43.7056...
#> 9          NA POLYGON ((-4.850903 43.7056...
#> 10         NA POLYGON ((-4.761071 43.7056...
#> 
#> $blocking_per_species$ind.FULGLA$map

#> 
#> 
#> 
```

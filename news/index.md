# Changelog

## pelascope 1.3

- prep_lin: structure modification in the function. Does not require
  {rlang} and “quos”” anymore, but just character in unique_column.

## pelascope 1.2

- descriptive_stats_effort: change blocking from 0.1 degree to 10km grid

## pelascope 1.1

- rename function : check_raw_effort
- rename function : check_raw_sighting
- rename function : descriptive_stat_effort
- rename function : estimate_esw
- rename function : make_soap
- rename function : test_prep_line
- change remove_attractor : remove also direction
- estimate_esw : change prediction calcualtion, only consider hn
  detection function
- fit_and_predict : change entrance
- descriptive_stat_effort : add beaufort plot

## pelascope 0.2.9

- Create: prep_lin to prepare linearization (replace fill_hole_effort)

## pelascope 0.2.8

- Create: Associate_covariate
- Update Vignette processing climato

## pelascope 0.2.7

- Update: fit_and_predict remove cycle possibility
- Update: calc_esw calculate on a group of species remove abunadnce

## pelascope 0.2.6

- Update: fit_and_predict

## pelascope 0.2.5

- Creation function: remove_attract
- Creation function: plot_subjective
- Update first_stats_effort table effort per beaufort and stack bar
  change blocking function
- Update check_brut_effort

## pelascope 0.2.4

- Creation function: fit_and_predict

## pelascope 0.2.3

- Creation function: create_soap

## pelascope 0.2.2

- Creation function: calc_esw

## pelascope 0.2.1

- Creation function: sightings_to_effort
- Creation function: first_stat_effort

## pelascope 0.1.4

- Update READ.ME

## pelascope 0.1.3

- Creation function: check_brut_sightings

## pelascope 0.1.2

- Creation function: fill_hole_effort

## pelascope 0.1.1

- First function: check_brut_effort

## pelascope 0.0.1

- Initial creation

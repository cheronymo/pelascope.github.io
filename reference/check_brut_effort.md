# Check Brut Effort From Data Base

Checking the Effort dataset extract directly from the Data base :
colnames, missing values, etc. And it renames them in order to enter in
the pelascope workflow.

## Usage

``` r
check_brut_effort(data_effort, only_prospection = TRUE, filter_speed = 8)
```

## Arguments

- data_effort:

  dataframe. Effort table extract from the data base.

- only_prospection:

  TRUE/FALSE. Needed to keep only the prospection route type (TRUE) or
  all of them (FALSE)

- filter_speed:

  numeric. Minimum speed limit.

## Value

Data effort table clean and ready for the pelascope workflow.

## Examples

``` r
data(data_effort_brut)

check_brut_effort(data_effort = data_effort_brut, 
                  only_prospection = TRUE, 
                  filter_speed = 8)
#> 
#> ── Information regarding the dataset ──
#> 
#>    Route Type Effort Point Count
#> 1       other                142
#> 2 prospection                558
#> 3    trawling                116
#> ── Dataset cleaned ──
#> 
#>     Survey            plateform   routeType status          LegID speed
#> 1   PELGAS upper_bridge_outside prospection  BEGIN  30042023_C_G1    10
#> 2   PELGAS upper_bridge_outside prospection    ADD  30042023_C_G1    11
#> 3   PELGAS upper_bridge_outside prospection    END  30042023_C_G1    11
#> 4   PELGAS upper_bridge_outside prospection  BEGIN  30042023_C_G3    10
#> 5   PELGAS upper_bridge_outside prospection    ADD  30042023_C_G3    11
#> 6   PELGAS upper_bridge_outside prospection    ADD  30042023_C_G3    11
#> 7   PELGAS upper_bridge_outside prospection    ADD  30042023_C_G3    12
#> 8   PELGAS upper_bridge_outside prospection    ADD  30042023_C_G3    12
#> 9   PELGAS upper_bridge_outside prospection    ADD  30042023_C_G3    12
#> 10  PELGAS upper_bridge_outside prospection    ADD  30042023_C_G3    11
#> 11  PELGAS upper_bridge_outside prospection    ADD  30042023_C_G3    12
#> 12  PELGAS upper_bridge_outside prospection    ADD  30042023_C_G3    11
#> 13  PELGAS upper_bridge_outside prospection    ADD  30042023_C_G3    11
#> 14  PELGAS upper_bridge_outside prospection    ADD  30042023_C_G3    11
#> 15  PELGAS upper_bridge_outside prospection    ADD  30042023_C_G3    12
#> 16  PELGAS upper_bridge_outside prospection    END  30042023_C_G3    12
#> 17  PELGAS upper_bridge_outside prospection  BEGIN  01052023_C_G1    11
#> 18  PELGAS upper_bridge_outside prospection    ADD  01052023_C_G1    10
#> 19  PELGAS upper_bridge_outside prospection    END  01052023_C_G1    10
#> 20  PELGAS upper_bridge_outside prospection  BEGIN  01052023_C_G3    11
#> 21  PELGAS upper_bridge_outside prospection    ADD  01052023_C_G3    11
#> 22  PELGAS upper_bridge_outside prospection    ADD  01052023_C_G3    11
#> 23  PELGAS upper_bridge_outside prospection    END  01052023_C_G3    11
#> 24  PELGAS upper_bridge_outside prospection  BEGIN  01052023_C_G5    10
#> 25  PELGAS upper_bridge_outside prospection    ADD  01052023_C_G5     9
#> 26  PELGAS upper_bridge_outside prospection    ADD  01052023_C_G5    11
#> 27  PELGAS upper_bridge_outside prospection    ADD  01052023_C_G5     9
#> 28  PELGAS upper_bridge_outside prospection    ADD  01052023_C_G5     9
#> 29  PELGAS upper_bridge_outside prospection    END  01052023_C_G5     9
#> 30  PELGAS upper_bridge_outside prospection    ADD  01052023_C_G7    11
#> 31  PELGAS upper_bridge_outside prospection    ADD  01052023_C_G7    11
#> 32  PELGAS upper_bridge_outside prospection    ADD  01052023_C_G7    11
#> 33  PELGAS upper_bridge_outside prospection    ADD  01052023_C_G7    10
#> 34  PELGAS upper_bridge_outside prospection    ADD  01052023_C_G7    10
#> 35  PELGAS upper_bridge_outside prospection    ADD  01052023_C_G7    10
#> 36  PELGAS upper_bridge_outside prospection    ADD  01052023_C_G7     9
#> 37  PELGAS upper_bridge_outside prospection    ADD  01052023_C_G7    11
#> 38  PELGAS upper_bridge_outside prospection    END  01052023_C_G7    11
#> 39  PELGAS upper_bridge_outside prospection  BEGIN  02052023_C_G1    10
#> 40  PELGAS upper_bridge_outside prospection    ADD  02052023_C_G1    10
#> 41  PELGAS upper_bridge_outside prospection    ADD  02052023_C_G1    10
#> 42  PELGAS upper_bridge_outside prospection    ADD  02052023_C_G1    11
#> 43  PELGAS upper_bridge_outside prospection    ADD  02052023_C_G1    11
#> 44  PELGAS upper_bridge_outside prospection    ADD  02052023_C_G1    11
#> 45  PELGAS upper_bridge_outside prospection    ADD  02052023_C_G1    11
#> 46  PELGAS upper_bridge_outside prospection    ADD  02052023_C_G1    11
#> 47  PELGAS upper_bridge_outside prospection    END  02052023_C_G1    11
#> 48  PELGAS upper_bridge_outside prospection  BEGIN  02052023_C_G3    10
#> 49  PELGAS upper_bridge_outside prospection    ADD  02052023_C_G3    10
#> 50  PELGAS upper_bridge_outside prospection  BEGIN  02052023_C_G4    11
#> 51  PELGAS upper_bridge_outside prospection    ADD  02052023_C_G4    10
#> 52  PELGAS upper_bridge_outside prospection    ADD  02052023_C_G4    10
#> 53  PELGAS upper_bridge_outside prospection    END  02052023_C_G4    10
#> 54  PELGAS upper_bridge_outside prospection  BEGIN  02052023_C_G6     9
#> 55  PELGAS upper_bridge_outside prospection    ADD  02052023_C_G6     8
#> 56  PELGAS upper_bridge_outside prospection    END  02052023_C_G6     8
#> 57  PELGAS upper_bridge_outside prospection  BEGIN  02052023_C_G8     8
#> 58  PELGAS upper_bridge_outside prospection    END  02052023_C_G8     8
#> 59  PELGAS upper_bridge_outside prospection    ADD  03052023_C_G3    11
#> 60  PELGAS upper_bridge_outside prospection    ADD  03052023_C_G3     9
#> 61  PELGAS upper_bridge_outside prospection    ADD  03052023_C_G3    10
#> 62  PELGAS upper_bridge_outside prospection    ADD  03052023_C_G3    10
#> 63  PELGAS upper_bridge_outside prospection    ADD  03052023_C_G3    11
#> 64  PELGAS upper_bridge_outside prospection    ADD  03052023_C_G3    10
#> 65  PELGAS upper_bridge_outside prospection    ADD  03052023_C_G3    11
#> 66  PELGAS upper_bridge_outside prospection    END  03052023_C_G1    11
#> 67  PELGAS upper_bridge_outside prospection    ADD  03052023_C_G1    10
#> 68  PELGAS upper_bridge_outside prospection    ADD  03052023_C_G1    10
#> 69  PELGAS upper_bridge_outside prospection  BEGIN  03052023_C_G1    10
#> 70  PELGAS upper_bridge_outside prospection    ADD  03052023_C_G7    11
#> 71  PELGAS upper_bridge_outside prospection    ADD  03052023_C_G7    11
#> 72  PELGAS upper_bridge_outside prospection    ADD  03052023_C_G7    11
#> 73  PELGAS upper_bridge_outside prospection    ADD  03052023_C_G7    10
#> 74  PELGAS upper_bridge_outside prospection    END  03052023_C_G7    10
#> 75  PELGAS upper_bridge_outside prospection  BEGIN  03052023_C_G3    10
#> 76  PELGAS upper_bridge_outside prospection  BEGIN  03052023_C_G5    10
#> 77  PELGAS upper_bridge_outside prospection    ADD  03052023_C_G5    10
#> 78  PELGAS upper_bridge_outside prospection    END  03052023_C_G5    10
#> 79  PELGAS upper_bridge_outside prospection  BEGIN  03052023_C_G7    10
#> 80  PELGAS upper_bridge_outside prospection    ADD  04052023_C_G5    10
#> 81  PELGAS upper_bridge_outside prospection    ADD  04052023_C_G5    10
#> 82  PELGAS upper_bridge_outside prospection  BEGIN  04052023_C_G5    10
#> 83  PELGAS upper_bridge_outside prospection    ADD  04052023_C_G3    10
#> 84  PELGAS upper_bridge_outside prospection    ADD  04052023_C_G3    10
#> 85  PELGAS upper_bridge_outside prospection    ADD  04052023_C_G3    10
#> 86  PELGAS upper_bridge_outside prospection    ADD  04052023_C_G3    11
#> 87  PELGAS upper_bridge_outside prospection    ADD  04052023_C_G3    11
#> 88  PELGAS upper_bridge_outside prospection    ADD  04052023_C_G3    11
#> 89  PELGAS upper_bridge_outside prospection    ADD  04052023_C_G3    11
#> 90  PELGAS upper_bridge_outside prospection    ADD  04052023_C_G3     9
#> 91  PELGAS upper_bridge_outside prospection  BEGIN  04052023_C_G3    10
#> 92  PELGAS upper_bridge_outside prospection    END  04052023_C_G1     9
#> 93  PELGAS upper_bridge_outside prospection    ADD  04052023_C_G1     9
#> 94  PELGAS upper_bridge_outside prospection    ADD  04052023_C_G1     9
#> 95  PELGAS upper_bridge_outside prospection  BEGIN  04052023_C_G1    10
#> 96  PELGAS upper_bridge_outside prospection  BEGIN 05052023_C_G14    11
#> 97  PELGAS upper_bridge_outside prospection    END 05052023_C_G12    10
#> 98  PELGAS upper_bridge_outside prospection    ADD 05052023_C_G12    10
#> 99  PELGAS upper_bridge_outside prospection    ADD 05052023_C_G12    10
#> 100 PELGAS upper_bridge_outside prospection    ADD 05052023_C_G12     9
#> 101 PELGAS upper_bridge_outside prospection    ADD 05052023_C_G12     9
#> 102 PELGAS upper_bridge_outside prospection  BEGIN 05052023_C_G12     9
#> 103 PELGAS upper_bridge_outside prospection    ADD 05052023_C_G10    10
#> 104 PELGAS upper_bridge_outside prospection    ADD 05052023_C_G10    10
#> 105 PELGAS upper_bridge_outside prospection    ADD 05052023_C_G10    10
#> 106 PELGAS upper_bridge_outside prospection    ADD 05052023_C_G10    11
#> 107 PELGAS upper_bridge_outside prospection  BEGIN 05052023_C_G10    10
#> 108 PELGAS upper_bridge_outside prospection    ADD  05052023_C_G8    10
#> 109 PELGAS upper_bridge_outside prospection    ADD  05052023_C_G8     9
#> 110 PELGAS upper_bridge_outside prospection    ADD  05052023_C_G8     9
#> 111 PELGAS upper_bridge_outside prospection    ADD  05052023_C_G8    10
#> 112 PELGAS upper_bridge_outside prospection  BEGIN  05052023_C_G8    10
#> 113 PELGAS upper_bridge_outside prospection    END 06052023_C_G20    10
#> 114 PELGAS upper_bridge_outside prospection    ADD 06052023_C_G20     9
#> 115 PELGAS upper_bridge_outside prospection    ADD 06052023_C_G20     9
#> 116 PELGAS upper_bridge_outside prospection    ADD 06052023_C_G20     9
#> 117 PELGAS        bridge_inside prospection    ADD 06052023_C_G20     9
#> 118 PELGAS upper_bridge_outside prospection    ADD 06052023_C_G20     9
#> 119 PELGAS upper_bridge_outside prospection  BEGIN 06052023_C_G20    10
#> 120 PELGAS upper_bridge_outside prospection    ADD 06052023_C_G18    11
#> 121 PELGAS upper_bridge_outside prospection    ADD 06052023_C_G18    10
#> 122 PELGAS upper_bridge_outside prospection    ADD 06052023_C_G18     9
#> 123 PELGAS upper_bridge_outside prospection    ADD 06052023_C_G18     9
#> 124 PELGAS upper_bridge_outside prospection    ADD 06052023_C_G18     9
#> 125 PELGAS upper_bridge_outside prospection    ADD 06052023_C_G18     9
#> 126 PELGAS upper_bridge_outside prospection    ADD 06052023_C_G18    10
#> 127 PELGAS upper_bridge_outside prospection    ADD 06052023_C_G18    10
#> 128 PELGAS upper_bridge_outside prospection    ADD 06052023_C_G18    10
#> 129 PELGAS upper_bridge_outside prospection    ADD 06052023_C_G18    12
#> 130 PELGAS upper_bridge_outside prospection    ADD 06052023_C_G18    11
#> 131 PELGAS upper_bridge_outside prospection  BEGIN 06052023_C_G18    10
#> 132 PELGAS upper_bridge_outside prospection  BEGIN 06052023_C_G16     9
#> 133 PELGAS upper_bridge_outside prospection  BEGIN 07052023_C_G21    10
#> 134 PELGAS upper_bridge_outside prospection    ADD 07052023_C_G21    10
#> 135 PELGAS upper_bridge_outside prospection    END 07052023_C_G21    10
#> 136 PELGAS upper_bridge_outside prospection  BEGIN 07052023_C_G23    10
#> 137 PELGAS upper_bridge_outside prospection    ADD 07052023_C_G23    10
#> 138 PELGAS upper_bridge_outside prospection    ADD 07052023_C_G23    10
#> 139 PELGAS upper_bridge_outside prospection    ADD 07052023_C_G23    10
#> 140 PELGAS upper_bridge_outside prospection    ADD 07052023_C_G23    10
#> 141 PELGAS upper_bridge_outside prospection    END 07052023_C_G23    10
#> 142 PELGAS upper_bridge_outside prospection  BEGIN 07052023_C_G25    10
#> 143 PELGAS upper_bridge_outside prospection    ADD 07052023_C_G25    11
#> 144 PELGAS upper_bridge_outside prospection    ADD 07052023_C_G25    11
#> 145 PELGAS upper_bridge_outside prospection    ADD 07052023_C_G25    10
#> 146 PELGAS upper_bridge_outside prospection  BEGIN 07052023_C_G27    10
#> 147 PELGAS upper_bridge_outside prospection    ADD 07052023_C_G27    10
#> 148 PELGAS upper_bridge_outside prospection    ADD 07052023_C_G27    11
#> 149 PELGAS upper_bridge_outside prospection    ADD 07052023_C_G27    10
#> 150 PELGAS upper_bridge_outside prospection    ADD 07052023_C_G27    11
#> 151 PELGAS upper_bridge_outside prospection    ADD 07052023_C_G27    11
#> 152 PELGAS upper_bridge_outside prospection    ADD 07052023_C_G27    10
#> 153 PELGAS upper_bridge_outside prospection    END 07052023_C_G27    10
#> 154 PELGAS upper_bridge_outside prospection    END 08052023_C_G35     8
#> 155 PELGAS upper_bridge_outside prospection  BEGIN 08052023_C_G37     8
#> 156 PELGAS upper_bridge_outside prospection    ADD 08052023_C_G37     8
#> 157 PELGAS upper_bridge_outside prospection    END 08052023_C_G37     8
#> 158 PELGAS upper_bridge_outside prospection  BEGIN 08052023_C_G35    10
#> 159 PELGAS upper_bridge_outside prospection    ADD 08052023_C_G35    10
#> 160 PELGAS upper_bridge_outside prospection    END 08052023_C_G30    10
#> 161 PELGAS upper_bridge_outside prospection  BEGIN 08052023_C_G32    11
#> 162 PELGAS upper_bridge_outside prospection    ADD 08052023_C_G32    10
#> 163 PELGAS upper_bridge_outside prospection    END 08052023_C_G32    10
#> 164 PELGAS upper_bridge_outside prospection  BEGIN 08052023_C_G28    10
#> 165 PELGAS upper_bridge_outside prospection    ADD 08052023_C_G28    11
#> 166 PELGAS upper_bridge_outside prospection    END 08052023_C_G28    11
#> 167 PELGAS upper_bridge_outside prospection  BEGIN 08052023_C_G30     9
#> 168 PELGAS upper_bridge_outside prospection    ADD 08052023_C_G30    10
#> 169 PELGAS        bridge_inside prospection    ADD 08052023_C_G30    10
#> 170 PELGAS upper_bridge_outside prospection    ADD 08052023_C_G30    11
#> 171 PELGAS        bridge_inside prospection  BEGIN  09052023_C_G3    11
#> 172 PELGAS        bridge_inside prospection    ADD  09052023_C_G3    13
#> 173 PELGAS        bridge_inside prospection    ADD  09052023_C_G3    12
#> 174 PELGAS        bridge_inside prospection    ADD  09052023_C_G3    12
#> 175 PELGAS upper_bridge_outside prospection  BEGIN  09052023_C_G5    10
#> 176 PELGAS        bridge_inside prospection    ADD  09052023_C_G5    10
#> 177 PELGAS        bridge_inside prospection    ADD  09052023_C_G5    11
#> 178 PELGAS        bridge_inside prospection    ADD  09052023_C_G5    11
#> 179 PELGAS        bridge_inside prospection    ADD  09052023_C_G5    10
#> 180 PELGAS        bridge_inside prospection    ADD  09052023_C_G5    10
#> 181 PELGAS        bridge_inside prospection    END  09052023_C_G5    10
#> 182 PELGAS        bridge_inside prospection  BEGIN  09052023_C_G7    10
#> 183 PELGAS        bridge_inside prospection    END  09052023_C_G7    10
#> 184 PELGAS        bridge_inside prospection    ADD  10052023_C_G8    10
#> 185 PELGAS        bridge_inside prospection    ADD  10052023_C_G8    10
#> 186 PELGAS        bridge_inside prospection    ADD  10052023_C_G8    11
#> 187 PELGAS        bridge_inside prospection    ADD  10052023_C_G8    11
#> 188 PELGAS        bridge_inside prospection    ADD  10052023_C_G8    10
#> 189 PELGAS        bridge_inside prospection    ADD  10052023_C_G8    10
#> 190 PELGAS        bridge_inside prospection    ADD  10052023_C_G8    10
#> 191 PELGAS        bridge_inside prospection  BEGIN  10052023_C_G8     9
#> 192 PELGAS upper_bridge_outside prospection    ADD 10052023_C_G10    10
#> 193 PELGAS upper_bridge_outside prospection    ADD 10052023_C_G10    10
#> 194 PELGAS upper_bridge_outside prospection    ADD 10052023_C_G10    11
#> 195 PELGAS upper_bridge_outside prospection  BEGIN 10052023_C_G10    11
#> 196 PELGAS upper_bridge_outside prospection    ADD  10052023_C_G8    10
#> 197 PELGAS        bridge_inside prospection    ADD  10052023_C_G8     9
#> 198 PELGAS upper_bridge_outside prospection  BEGIN  11052023_C_G1    11
#> 199 PELGAS upper_bridge_outside prospection    ADD  11052023_C_G1    10
#> 200 PELGAS upper_bridge_outside prospection    ADD  11052023_C_G1    11
#> 201 PELGAS upper_bridge_outside prospection    ADD  11052023_C_G1    11
#> 202 PELGAS upper_bridge_outside prospection    ADD  11052023_C_G1    11
#> 203 PELGAS upper_bridge_outside prospection    END  11052023_C_G1    11
#> 204 PELGAS upper_bridge_outside prospection  BEGIN  11052023_C_G3    10
#> 205 PELGAS upper_bridge_outside prospection    ADD  11052023_C_G3    10
#> 206 PELGAS upper_bridge_outside prospection    ADD  11052023_C_G3    10
#> 207 PELGAS        bridge_inside prospection    ADD  11052023_C_G3    10
#> 208 PELGAS        bridge_inside prospection    ADD  11052023_C_G3    10
#> 209 PELGAS upper_bridge_outside prospection    ADD  11052023_C_G3    10
#> 210 PELGAS upper_bridge_outside prospection    END  11052023_C_G3    10
#> 211 PELGAS upper_bridge_outside prospection  BEGIN  11052023_C_G5    10
#> 212 PELGAS upper_bridge_outside prospection    ADD  11052023_C_G5    10
#> 213 PELGAS upper_bridge_outside prospection    ADD  11052023_C_G5    10
#> 214 PELGAS upper_bridge_outside prospection    END  11052023_C_G5    10
#> 215 PELGAS upper_bridge_outside prospection  BEGIN  11052023_C_G7     8
#> 216 PELGAS upper_bridge_outside prospection    END  11052023_C_G7     8
#> 217 PELGAS        bridge_inside prospection  BEGIN  12052023_C_G1     9
#> 218 PELGAS        bridge_inside prospection    ADD  12052023_C_G1    10
#> 219 PELGAS        bridge_inside prospection    END  12052023_C_G1    10
#> 220 PELGAS        bridge_inside prospection  BEGIN  12052023_C_G3    10
#> 221 PELGAS upper_bridge_outside prospection    ADD  12052023_C_G3    10
#> 222 PELGAS upper_bridge_outside prospection    END  12052023_C_G3    10
#> 223 PELGAS upper_bridge_outside prospection  BEGIN  12052023_C_G5    10
#> 224 PELGAS upper_bridge_outside prospection    END  12052023_C_G5    10
#> 225 PELGAS upper_bridge_outside prospection  BEGIN  12052023_C_G7    10
#> 226 PELGAS upper_bridge_outside prospection    ADD  12052023_C_G7    10
#> 227 PELGAS upper_bridge_outside prospection    ADD  12052023_C_G7    11
#> 228 PELGAS upper_bridge_outside prospection    ADD  12052023_C_G7    10
#> 229 PELGAS upper_bridge_outside prospection    ADD  12052023_C_G7    11
#> 230 PELGAS upper_bridge_outside prospection    ADD  12052023_C_G7    11
#> 231 PELGAS upper_bridge_outside prospection    ADD  12052023_C_G7    10
#> 232 PELGAS upper_bridge_outside prospection    ADD  12052023_C_G7    10
#> 233 PELGAS upper_bridge_outside prospection    END  12052023_C_G7    10
#> 234 PELGAS upper_bridge_outside prospection  BEGIN  14052023_C_G7    10
#> 235 PELGAS upper_bridge_outside prospection  BEGIN 14052023_C_G11    10
#> 236 PELGAS upper_bridge_outside prospection    END  14052023_C_G9    10
#> 237 PELGAS upper_bridge_outside prospection    ADD  14052023_C_G9    10
#> 238 PELGAS upper_bridge_outside prospection    ADD  14052023_C_G9    11
#> 239 PELGAS upper_bridge_outside prospection  BEGIN  14052023_C_G9    10
#> 240 PELGAS upper_bridge_outside prospection    ADD  14052023_C_G7    10
#> 241 PELGAS upper_bridge_outside prospection    ADD  14052023_C_G5    10
#> 242 PELGAS upper_bridge_outside prospection  BEGIN  14052023_C_G5    11
#> 243 PELGAS upper_bridge_outside prospection    END  14052023_C_G3    10
#> 244 PELGAS upper_bridge_outside prospection  BEGIN  14052023_C_G3    10
#> 245 PELGAS upper_bridge_outside prospection    END  14052023_C_G2    10
#> 246 PELGAS upper_bridge_outside prospection  BEGIN  14052023_C_G2    11
#> 247 PELGAS upper_bridge_outside prospection    ADD  15052023_C_G5    10
#> 248 PELGAS upper_bridge_outside prospection    ADD  15052023_C_G5    11
#> 249 PELGAS upper_bridge_outside prospection    ADD  15052023_C_G5    11
#> 250 PELGAS upper_bridge_outside prospection    ADD  15052023_C_G5    10
#> 251 PELGAS upper_bridge_outside prospection  BEGIN  15052023_C_G5    10
#> 252 PELGAS upper_bridge_outside prospection    ADD  15052023_C_G3     9
#> 253 PELGAS upper_bridge_outside prospection    ADD  15052023_C_G3    10
#> 254 PELGAS upper_bridge_outside prospection    ADD  15052023_C_G3    10
#> 255 PELGAS upper_bridge_outside prospection  BEGIN  15052023_C_G3    10
#> 256 PELGAS upper_bridge_outside prospection    ADD  15052023_C_G5    10
#> 257 PELGAS upper_bridge_outside prospection    ADD  15052023_C_G5     9
#> 258 PELGAS upper_bridge_outside prospection    ADD  15052023_C_G5    10
#> 259 PELGAS upper_bridge_outside prospection    ADD  15052023_C_G7    11
#> 260 PELGAS upper_bridge_outside prospection  BEGIN  15052023_C_G7    10
#> 261 PELGAS upper_bridge_outside prospection  BEGIN  16052023_C_G1    10
#> 262 PELGAS upper_bridge_outside prospection    ADD  16052023_C_G1    10
#> 263 PELGAS upper_bridge_outside prospection    ADD  16052023_C_G1    10
#> 264 PELGAS upper_bridge_outside prospection    ADD  16052023_C_G1    10
#> 265 PELGAS upper_bridge_outside prospection    END  16052023_C_G1    10
#> 266 PELGAS upper_bridge_outside prospection  BEGIN  16052023_C_G4    10
#> 267 PELGAS upper_bridge_outside prospection    ADD  16052023_C_G4    10
#> 268 PELGAS upper_bridge_outside prospection    ADD  16052023_C_G4    10
#> 269 PELGAS upper_bridge_outside prospection    ADD  16052023_C_G4    11
#> 270 PELGAS upper_bridge_outside prospection    END  16052023_C_G4    11
#> 271 PELGAS upper_bridge_outside prospection  BEGIN  16052023_C_G6    10
#> 272 PELGAS upper_bridge_outside prospection    ADD  16052023_C_G6    10
#> 273 PELGAS upper_bridge_outside prospection    ADD  16052023_C_G6    10
#> 274 PELGAS upper_bridge_outside prospection    ADD  16052023_C_G6    10
#> 275 PELGAS upper_bridge_outside prospection    ADD  16052023_C_G6    10
#> 276 PELGAS upper_bridge_outside prospection    ADD  16052023_C_G6    10
#> 277 PELGAS upper_bridge_outside prospection    END  16052023_C_G6    10
#> 278 PELGAS upper_bridge_outside prospection    ADD  17052023_C_G8    10
#> 279 PELGAS upper_bridge_outside prospection    END  17052023_C_G8     9
#> 280 PELGAS upper_bridge_outside prospection    ADD  17052023_C_G8    10
#> 281 PELGAS upper_bridge_outside prospection    ADD  17052023_C_G8    10
#> 282 PELGAS upper_bridge_outside prospection    ADD  17052023_C_G8     9
#> 283 PELGAS upper_bridge_outside prospection    ADD  17052023_C_G8    10
#> 284 PELGAS upper_bridge_outside prospection  BEGIN  17052023_C_G8    10
#> 285 PELGAS upper_bridge_outside prospection    ADD  17052023_C_G6    10
#> 286 PELGAS upper_bridge_outside prospection  BEGIN  17052023_C_G6    10
#> 287 PELGAS upper_bridge_outside prospection    END  17052023_C_G4    10
#> 288 PELGAS upper_bridge_outside prospection    ADD  17052023_C_G4    11
#> 289 PELGAS upper_bridge_outside prospection  BEGIN  17052023_C_G4    10
#> 290 PELGAS upper_bridge_outside prospection    END  17052023_C_G2    10
#> 291 PELGAS upper_bridge_outside prospection    ADD  17052023_C_G2    11
#> 292 PELGAS upper_bridge_outside prospection    ADD  17052023_C_G2    10
#> 293 PELGAS upper_bridge_outside prospection    ADD  17052023_C_G2    10
#> 294 PELGAS upper_bridge_outside prospection    ADD  17052023_C_G2     9
#> 295 PELGAS upper_bridge_outside prospection    ADD  17052023_C_G2    10
#> 296 PELGAS upper_bridge_outside prospection    ADD  17052023_C_G2    10
#> 297 PELGAS upper_bridge_outside prospection  BEGIN  17052023_C_G2    10
#> 298 PELGAS upper_bridge_outside prospection    ADD  18052023_C_G5    11
#> 299 PELGAS upper_bridge_outside prospection  BEGIN  18052023_C_G5    11
#> 300 PELGAS upper_bridge_outside prospection    END  18052023_C_G3    11
#> 301 PELGAS upper_bridge_outside prospection    ADD  18052023_C_G3    11
#> 302 PELGAS upper_bridge_outside prospection    ADD  18052023_C_G3    11
#> 303 PELGAS upper_bridge_outside prospection  BEGIN  18052023_C_G3    10
#> 304 PELGAS upper_bridge_outside prospection    ADD  18052023_C_G1    10
#> 305 PELGAS upper_bridge_outside prospection    ADD  18052023_C_G1    10
#> 306 PELGAS upper_bridge_outside prospection    ADD  18052023_C_G1     9
#> 307 PELGAS upper_bridge_outside prospection  BEGIN  18052023_C_G1    10
#> 308 PELGAS upper_bridge_outside prospection    END 18052023_C_G11    11
#> 309 PELGAS upper_bridge_outside prospection    ADD 18052023_C_G11    10
#> 310 PELGAS upper_bridge_outside prospection  BEGIN 18052023_C_G11    11
#> 311 PELGAS upper_bridge_outside prospection    END  18052023_C_G9    11
#> 312 PELGAS upper_bridge_outside prospection    ADD  18052023_C_G9    10
#> 313 PELGAS upper_bridge_outside prospection    ADD  18052023_C_G9    10
#> 314 PELGAS upper_bridge_outside prospection    ADD  18052023_C_G9    10
#> 315 PELGAS upper_bridge_outside prospection  BEGIN  18052023_C_G9    10
#> 316 PELGAS upper_bridge_outside prospection    ADD  18052023_C_G7    10
#> 317 PELGAS upper_bridge_outside prospection    ADD  18052023_C_G5    12
#> 318 PELGAS upper_bridge_outside prospection  BEGIN 19052023_C_G11    10
#> 319 PELGAS upper_bridge_outside prospection    END  19052023_C_G9    10
#> 320 PELGAS upper_bridge_outside prospection  BEGIN  19052023_C_G9    11
#> 321 PELGAS upper_bridge_outside prospection    ADD  19052023_C_G7    10
#> 322 PELGAS upper_bridge_outside prospection  BEGIN  19052023_C_G7    10
#> 323 PELGAS upper_bridge_outside prospection  BEGIN  19052023_C_G1    11
#> 324 PELGAS upper_bridge_outside prospection    ADD  19052023_C_G1    10
#> 325 PELGAS upper_bridge_outside prospection    ADD  19052023_C_G1    10
#> 326 PELGAS upper_bridge_outside prospection    END  19052023_C_G1    10
#> 327 PELGAS upper_bridge_outside prospection  BEGIN  19052023_C_G3    11
#> 328 PELGAS upper_bridge_outside prospection    ADD  19052023_C_G3    10
#> 329 PELGAS upper_bridge_outside prospection    ADD  19052023_C_G3    10
#> 330 PELGAS upper_bridge_outside prospection    END  19052023_C_G3    10
#> 331 PELGAS upper_bridge_outside prospection  BEGIN  19052023_C_G5     9
#> 332 PELGAS upper_bridge_outside prospection    ADD  19052023_C_G5    10
#> 333 PELGAS upper_bridge_outside prospection    END  19052023_C_G5    10
#> 334 PELGAS upper_bridge_outside prospection    ADD 19052023_C_G13    11
#> 335 PELGAS upper_bridge_outside prospection  BEGIN 19052023_C_G13    11
#> 336 PELGAS upper_bridge_outside prospection  BEGIN 20052023_C_G11    10
#> 337 PELGAS upper_bridge_outside prospection    END  20052023_C_G9    10
#> 338 PELGAS upper_bridge_outside prospection    ADD  20052023_C_G9    10
#> 339 PELGAS upper_bridge_outside prospection    ADD  20052023_C_G9    10
#> 340 PELGAS upper_bridge_outside prospection    ADD  20052023_C_G9    10
#> 341 PELGAS upper_bridge_outside prospection  BEGIN  20052023_C_G9    11
#> 342 PELGAS upper_bridge_outside prospection    ADD  20052023_C_G7    10
#> 343 PELGAS upper_bridge_outside prospection    ADD  20052023_C_G7    10
#> 344 PELGAS upper_bridge_outside prospection  BEGIN  20052023_C_G7     9
#> 345 PELGAS upper_bridge_outside prospection    ADD  20052023_C_G5    10
#> 346 PELGAS upper_bridge_outside prospection    ADD  20052023_C_G5    11
#> 347 PELGAS upper_bridge_outside prospection  BEGIN  20052023_C_G5    10
#> 348 PELGAS upper_bridge_outside prospection    END  20052023_C_G3    10
#> 349 PELGAS upper_bridge_outside prospection    ADD  20052023_C_G3    10
#> 350 PELGAS upper_bridge_outside prospection    ADD  20052023_C_G3    10
#> 351 PELGAS upper_bridge_outside prospection    ADD  20052023_C_G3     8
#> 352 PELGAS upper_bridge_outside prospection    END  20052023_C_G1    10
#> 353 PELGAS upper_bridge_outside prospection    ADD  20052023_C_G1    11
#> 354 PELGAS upper_bridge_outside prospection  BEGIN  20052023_C_G1    10
#> 355 PELGAS upper_bridge_outside prospection  BEGIN  21052023_C_G1    10
#> 356 PELGAS upper_bridge_outside prospection    ADD  21052023_C_G1    10
#> 357 PELGAS upper_bridge_outside prospection    ADD  21052023_C_G1     9
#> 358 PELGAS upper_bridge_outside prospection    ADD  21052023_C_G1    10
#> 359 PELGAS upper_bridge_outside prospection    ADD  21052023_C_G1     9
#> 360 PELGAS upper_bridge_outside prospection    ADD  21052023_C_G1     9
#> 361 PELGAS upper_bridge_outside prospection    END  21052023_C_G1     9
#> 362 PELGAS upper_bridge_outside prospection  BEGIN  21052023_C_G3    10
#> 363 PELGAS upper_bridge_outside prospection    ADD  21052023_C_G3    10
#> 364 PELGAS upper_bridge_outside prospection    ADD  21052023_C_G3    10
#> 365 PELGAS upper_bridge_outside prospection    ADD  21052023_C_G3    10
#> 366 PELGAS upper_bridge_outside prospection    END  21052023_C_G3    10
#> 367 PELGAS upper_bridge_outside prospection  BEGIN  21052023_C_G5    10
#> 368 PELGAS upper_bridge_outside prospection    ADD  21052023_C_G5    10
#> 369 PELGAS upper_bridge_outside prospection    ADD  21052023_C_G5    10
#> 370 PELGAS upper_bridge_outside prospection    END  21052023_C_G5    10
#> 371 PELGAS upper_bridge_outside prospection  BEGIN  21052023_C_G7    10
#> 372 PELGAS upper_bridge_outside prospection    ADD  21052023_C_G7    11
#> 373 PELGAS upper_bridge_outside prospection    ADD  21052023_C_G7    10
#> 374 PELGAS upper_bridge_outside prospection    END  21052023_C_G7    10
#> 375 PELGAS upper_bridge_outside prospection  BEGIN  21052023_C_G9    11
#> 376 PELGAS upper_bridge_outside prospection    ADD  22052023_C_G7    10
#> 377 PELGAS upper_bridge_outside prospection    END  22052023_C_G7    10
#> 378 PELGAS upper_bridge_outside prospection  BEGIN  22052023_C_G9    10
#> 379 PELGAS upper_bridge_outside prospection    ADD  22052023_C_G9    10
#> 380 PELGAS upper_bridge_outside prospection    ADD  22052023_C_G9    10
#> 381 PELGAS upper_bridge_outside prospection    ADD  22052023_C_G9    10
#> 382 PELGAS upper_bridge_outside prospection    ADD  22052023_C_G9    10
#> 383 PELGAS upper_bridge_outside prospection    END  22052023_C_G9    10
#> 384 PELGAS upper_bridge_outside prospection  BEGIN 22052023_C_G11     9
#> 385 PELGAS upper_bridge_outside prospection    ADD 22052023_C_G11    10
#> 386 PELGAS upper_bridge_outside prospection    END 22052023_C_G11    10
#> 387 PELGAS upper_bridge_outside prospection    ADD  22052023_C_G7    10
#> 388 PELGAS upper_bridge_outside prospection  BEGIN  22052023_C_G1    10
#> 389 PELGAS upper_bridge_outside prospection    ADD  22052023_C_G1    10
#> 390 PELGAS upper_bridge_outside prospection    ADD  22052023_C_G1    10
#> 391 PELGAS upper_bridge_outside prospection    END  22052023_C_G1    10
#> 392 PELGAS upper_bridge_outside prospection  BEGIN  22052023_C_G3     8
#> 393 PELGAS upper_bridge_outside prospection    ADD  22052023_C_G3     9
#> 394 PELGAS upper_bridge_outside prospection    ADD  22052023_C_G3     9
#> 395 PELGAS upper_bridge_outside prospection    END  22052023_C_G3     9
#> 396 PELGAS upper_bridge_outside prospection  BEGIN  22052023_C_G5    10
#> 397 PELGAS upper_bridge_outside prospection    ADD  22052023_C_G5     9
#> 398 PELGAS upper_bridge_outside prospection    END  22052023_C_G5     9
#> 399 PELGAS upper_bridge_outside prospection  BEGIN  22052023_C_G7     9
#> 400 PELGAS upper_bridge_outside prospection  BEGIN  23052023_C_G1    10
#> 401 PELGAS upper_bridge_outside prospection    ADD  23052023_C_G1    10
#> 402 PELGAS upper_bridge_outside prospection    ADD  23052023_C_G1    10
#> 403 PELGAS upper_bridge_outside prospection    ADD  23052023_C_G1    10
#> 404 PELGAS upper_bridge_outside prospection    ADD  23052023_C_G1    10
#> 405 PELGAS upper_bridge_outside prospection    ADD  23052023_C_G1    10
#> 406 PELGAS upper_bridge_outside prospection    ADD  23052023_C_G1    10
#> 407 PELGAS upper_bridge_outside prospection    END  23052023_C_G1    10
#> 408 PELGAS upper_bridge_outside prospection  BEGIN  23052023_C_G3    10
#> 409 PELGAS upper_bridge_outside prospection    ADD  23052023_C_G3    11
#> 410 PELGAS upper_bridge_outside prospection    ADD  23052023_C_G3    11
#> 411 PELGAS upper_bridge_outside prospection    END  23052023_C_G3    11
#> 412 PELGAS upper_bridge_outside prospection  BEGIN  23052023_C_G5    10
#> 413 PELGAS upper_bridge_outside prospection    ADD  23052023_C_G5    10
#> 414 PELGAS upper_bridge_outside prospection    ADD  23052023_C_G5    10
#> 415 PELGAS upper_bridge_outside prospection    END  23052023_C_G5    10
#> 416 PELGAS upper_bridge_outside prospection  BEGIN  23052023_C_G7    10
#> 417 PELGAS upper_bridge_outside prospection    END  23052023_C_G7    10
#> 418 PELGAS upper_bridge_outside prospection  BEGIN  23052023_C_G9    10
#> 419 PELGAS upper_bridge_outside prospection    ADD  23052023_C_G9    10
#> 420 PELGAS upper_bridge_outside prospection    ADD  23052023_C_G9    10
#> 421 PELGAS upper_bridge_outside prospection    END  23052023_C_G9    10
#> 422 PELGAS upper_bridge_outside prospection    END  24052023_C_G9     9
#> 423 PELGAS upper_bridge_outside prospection    ADD  24052023_C_G9    10
#> 424 PELGAS upper_bridge_outside prospection    ADD  24052023_C_G9    10
#> 425 PELGAS upper_bridge_outside prospection  BEGIN  24052023_C_G9    10
#> 426 PELGAS upper_bridge_outside prospection    ADD  24052023_C_G7    10
#> 427 PELGAS upper_bridge_outside prospection    ADD  24052023_C_G7    10
#> 428 PELGAS upper_bridge_outside prospection  BEGIN  24052023_C_G7     8
#> 429 PELGAS upper_bridge_outside prospection    ADD  24052023_C_G5    10
#> 430 PELGAS upper_bridge_outside prospection  BEGIN  24052023_C_G5     8
#> 431 PELGAS upper_bridge_outside prospection    END  24052023_C_G3    11
#> 432 PELGAS upper_bridge_outside prospection  BEGIN  24052023_C_G3    11
#> 433 PELGAS upper_bridge_outside prospection    ADD  24052023_C_G1    10
#> 434 PELGAS upper_bridge_outside prospection    ADD  24052023_C_G1    10
#> 435 PELGAS upper_bridge_outside prospection    ADD  24052023_C_G1    10
#> 436 PELGAS upper_bridge_outside prospection  BEGIN  24052023_C_G1    10
#> 437 PELGAS upper_bridge_outside prospection    END 24052023_C_G11    10
#> 438 PELGAS upper_bridge_outside prospection    ADD 24052023_C_G11    10
#> 439 PELGAS upper_bridge_outside prospection  BEGIN 24052023_C_G11     9
#> 440 PELGAS upper_bridge_outside prospection    ADD  25052023_C_G9    11
#> 441 PELGAS upper_bridge_outside prospection  BEGIN  25052023_C_G9     9
#> 442 PELGAS upper_bridge_outside prospection    ADD  25052023_C_G7    10
#> 443 PELGAS upper_bridge_outside prospection    ADD  25052023_C_G7    10
#> 444 PELGAS upper_bridge_outside prospection    ADD  25052023_C_G7    10
#> 445 PELGAS upper_bridge_outside prospection  BEGIN  25052023_C_G7    10
#> 446 PELGAS upper_bridge_outside prospection    END  25052023_C_G5     9
#> 447 PELGAS upper_bridge_outside prospection    ADD  25052023_C_G5    11
#> 448 PELGAS upper_bridge_outside prospection  BEGIN  25052023_C_G5    10
#> 449 PELGAS upper_bridge_outside prospection    END  25052023_C_G3    10
#> 450 PELGAS upper_bridge_outside prospection    ADD  25052023_C_G3    10
#> 451 PELGAS upper_bridge_outside prospection    ADD  25052023_C_G3    10
#> 452 PELGAS upper_bridge_outside prospection  BEGIN  25052023_C_G3    10
#> 453 PELGAS upper_bridge_outside prospection    END  25052023_C_G1    10
#> 454 PELGAS upper_bridge_outside prospection  BEGIN  25052023_C_G1    10
#> 455 PELGAS upper_bridge_outside prospection  BEGIN  26052023_C_G1    10
#> 456 PELGAS upper_bridge_outside prospection    ADD  26052023_C_G1    10
#> 457 PELGAS upper_bridge_outside prospection    END  26052023_C_G1    10
#> 458 PELGAS upper_bridge_outside prospection  BEGIN  26052023_C_G3    10
#> 459 PELGAS upper_bridge_outside prospection    ADD  26052023_C_G3    10
#> 460 PELGAS upper_bridge_outside prospection    ADD  26052023_C_G3    10
#> 461 PELGAS upper_bridge_outside prospection    ADD  26052023_C_G3    11
#> 462 PELGAS upper_bridge_outside prospection    END  26052023_C_G3    11
#> 463 PELGAS upper_bridge_outside prospection  BEGIN  26052023_C_G5    10
#> 464 PELGAS upper_bridge_outside prospection    ADD  26052023_C_G5    10
#> 465 PELGAS upper_bridge_outside prospection    END  26052023_C_G5    10
#> 466 PELGAS upper_bridge_outside prospection  BEGIN  26052023_C_G7     9
#> 467 PELGAS upper_bridge_outside prospection    ADD  26052023_C_G7     9
#> 468 PELGAS upper_bridge_outside prospection    END  26052023_C_G7     9
#> 469 PELGAS upper_bridge_outside prospection  BEGIN  26052023_C_G9    11
#> 470 PELGAS upper_bridge_outside prospection    ADD  26052023_C_G9     9
#> 471 PELGAS upper_bridge_outside prospection    ADD  26052023_C_G9    10
#> 472 PELGAS upper_bridge_outside prospection    ADD  26052023_C_G9    10
#> 473 PELGAS upper_bridge_outside prospection    ADD 27052023_C_G11     8
#> 474 PELGAS upper_bridge_outside prospection    ADD 27052023_C_G11     8
#> 475 PELGAS upper_bridge_outside prospection  BEGIN 27052023_C_G11     8
#> 476 PELGAS upper_bridge_outside prospection    END  27052023_C_G9     8
#> 477 PELGAS upper_bridge_outside prospection  BEGIN  27052023_C_G9     8
#> 478 PELGAS upper_bridge_outside prospection    END  27052023_C_G7     8
#> 479 PELGAS upper_bridge_outside prospection    ADD  27052023_C_G7     8
#> 480 PELGAS upper_bridge_outside prospection    ADD  27052023_C_G7     9
#> 481 PELGAS upper_bridge_outside prospection    ADD  27052023_C_G7     9
#> 482 PELGAS upper_bridge_outside prospection  BEGIN  27052023_C_G7    10
#> 483 PELGAS upper_bridge_outside prospection    END  27052023_C_G5    10
#> 484 PELGAS upper_bridge_outside prospection    ADD  27052023_C_G5    10
#> 485 PELGAS upper_bridge_outside prospection    ADD  27052023_C_G5    10
#> 486 PELGAS upper_bridge_outside prospection  BEGIN  27052023_C_G5    10
#> 487 PELGAS upper_bridge_outside prospection    ADD  27052023_C_G3    10
#> 488 PELGAS upper_bridge_outside prospection  BEGIN  27052023_C_G3    10
#> 489 PELGAS upper_bridge_outside prospection    ADD  27052023_C_G1    10
#> 490 PELGAS upper_bridge_outside prospection    ADD  27052023_C_G1    10
#> 491 PELGAS upper_bridge_outside prospection    ADD  27052023_C_G1    10
#> 492 PELGAS upper_bridge_outside prospection  BEGIN  27052023_C_G1    10
#> 493 PELGAS upper_bridge_outside prospection  BEGIN  28052023_C_G1     9
#> 494 PELGAS upper_bridge_outside prospection    END  28052023_C_G1     9
#> 495 PELGAS upper_bridge_outside prospection  BEGIN  28052023_C_G3    10
#> 496 PELGAS upper_bridge_outside prospection    ADD  28052023_C_G3    10
#> 497 PELGAS upper_bridge_outside prospection    END  28052023_C_G3    10
#> 498 PELGAS upper_bridge_outside prospection  BEGIN  28052023_C_G5    10
#> 499 PELGAS upper_bridge_outside prospection    ADD  28052023_C_G5    10
#> 500 PELGAS upper_bridge_outside prospection    ADD  28052023_C_G5    10
#> 501 PELGAS upper_bridge_outside prospection    END  28052023_C_G5    10
#> 502 PELGAS upper_bridge_outside prospection  BEGIN  29052023_C_G3     9
#> 503 PELGAS upper_bridge_outside prospection  BEGIN  29052023_C_G1    10
#> 504 PELGAS upper_bridge_outside prospection    ADD  29052023_C_G1     9
#> 505 PELGAS upper_bridge_outside prospection    END  29052023_C_G5    10
#> 506 PELGAS upper_bridge_outside prospection  BEGIN  29052023_C_G5    10
#> 507 PELGAS upper_bridge_outside prospection    END  29052023_C_G3     9
#> 508 PELGAS upper_bridge_outside prospection    ADD  29052023_C_G3    10
#>     Beaufort Latitude Longitude n_obs            DateTime         TransectID
#> 1          2 48.34592 -4.541957     2 2023-04-30 06:37:02 TR_Pelgas_30042023
#> 2          2 48.29903 -4.620433     2 2023-04-30 07:00:19 TR_Pelgas_30042023
#> 3          2 48.22907 -4.709607     2 2023-04-30 07:30:55 TR_Pelgas_30042023
#> 4          3 47.96480 -4.711300     2 2023-04-30 09:10:20 TR_Pelgas_30042023
#> 5          3 47.89950 -4.680827     2 2023-04-30 09:34:07 TR_Pelgas_30042023
#> 6          3 47.83268 -4.624492     2 2023-04-30 09:59:15 TR_Pelgas_30042023
#> 7          3 47.66183 -4.504307     2 2023-04-30 11:00:00 TR_Pelgas_30042023
#> 8          3 47.51744 -4.393653     2 2023-04-30 11:51:58 TR_Pelgas_30042023
#> 9          3 47.32008 -4.271002     2 2023-04-30 12:59:52 TR_Pelgas_30042023
#> 10         3 47.13635 -4.155055     2 2023-04-30 14:04:17 TR_Pelgas_30042023
#> 11         3 46.98112 -4.054867     2 2023-04-30 14:58:58 TR_Pelgas_30042023
#> 12         3 46.79241 -3.928967     2 2023-04-30 16:05:40 TR_Pelgas_30042023
#> 13         3 46.64755 -3.830792     2 2023-04-30 16:57:10 TR_Pelgas_30042023
#> 14         3 46.54859 -3.763887     2 2023-04-30 17:32:30 TR_Pelgas_30042023
#> 15         3 46.46132 -3.705683     2 2023-04-30 18:03:36 TR_Pelgas_30042023
#> 16         3 46.30249 -3.598052     2 2023-04-30 19:00:29 TR_Pelgas_30042023
#> 17         3 44.55187 -2.456930     2 2023-05-01 05:06:56 TR_Pelgas_01052023
#> 18         3 44.41269 -2.370058     2 2023-05-01 05:56:19 TR_Pelgas_01052023
#> 19         3 44.38863 -2.354771     2 2023-05-01 06:08:13 TR_Pelgas_01052023
#> 20         2 44.33234 -2.304765     2 2023-05-01 06:56:56 TR_Pelgas_01052023
#> 21         2 44.13396 -2.197308     2 2023-05-01 08:04:50 TR_Pelgas_01052023
#> 22         2 44.09853 -2.180677     2 2023-05-01 08:16:27 TR_Pelgas_01052023
#> 23         2 44.06679 -2.165932     2 2023-05-01 08:29:24 TR_Pelgas_01052023
#> 24         2 44.08918 -2.175917     2 2023-05-01 10:30:15 TR_Pelgas_01052023
#> 25         3 44.07100 -2.164055     2 2023-05-01 10:43:32 TR_Pelgas_01052023
#> 26         4 44.06698 -2.231595     2 2023-05-01 11:01:43 TR_Pelgas_01052023
#> 27         3 44.06720 -2.309930     2 2023-05-01 11:22:29 TR_Pelgas_01052023
#> 28         3 44.06682 -2.442318     2 2023-05-01 11:57:53 TR_Pelgas_01052023
#> 29         3 44.06653 -2.523587     2 2023-05-01 12:19:43 TR_Pelgas_01052023
#> 30         2 44.00421 -2.525917     2 2023-05-01 13:39:03 TR_Pelgas_01052023
#> 31         2 43.94386 -2.531798     2 2023-05-01 13:58:53 TR_Pelgas_01052023
#> 32         2 43.88739 -2.550773     2 2023-05-01 14:18:06 TR_Pelgas_01052023
#> 33         3 43.86700 -2.533177     2 2023-05-01 14:27:01 TR_Pelgas_01052023
#> 34         3 43.86777 -2.418723     2 2023-05-01 14:56:52 TR_Pelgas_01052023
#> 35         3 43.86866 -2.177865     2 2023-05-01 15:58:09 TR_Pelgas_01052023
#> 36         2 43.86950 -2.123380     2 2023-05-01 16:12:24 TR_Pelgas_01052023
#> 37         2 43.76557 -2.234625     2 2023-05-01 16:56:26 TR_Pelgas_01052023
#> 38         2 43.66608 -2.333313     2 2023-05-01 17:39:05 TR_Pelgas_01052023
#> 39         5 43.66757 -3.127170     2 2023-05-02 05:10:33 TR_Pelgas_02052023
#> 40         5 43.66681 -2.930140     2 2023-05-02 06:00:39 TR_Pelgas_02052023
#> 41         4 43.66684 -2.675087     2 2023-05-02 07:04:16 TR_Pelgas_02052023
#> 42         4 43.66688 -2.441213     2 2023-05-02 08:01:53 TR_Pelgas_02052023
#> 43         4 43.66686 -2.344370     2 2023-05-02 08:25:36 TR_Pelgas_02052023
#> 44         4 43.66678 -2.199423     2 2023-05-02 09:01:23 TR_Pelgas_02052023
#> 45         4 43.66679 -2.094018     2 2023-05-02 09:27:06 TR_Pelgas_02052023
#> 46         2 43.66660 -1.910262     2 2023-05-02 10:12:54 TR_Pelgas_02052023
#> 47         2 43.66513 -1.766572     2 2023-05-02 10:47:49 TR_Pelgas_02052023
#> 48         3 43.66725 -1.798058     2 2023-05-02 12:29:12 TR_Pelgas_02052023
#> 49         3 43.66577 -1.672712     2 2023-05-02 13:01:10 TR_Pelgas_02052023
#> 50         3 43.66651 -1.525662     2 2023-05-02 15:33:36 TR_Pelgas_02052023
#> 51         4 43.66639 -1.456097     2 2023-05-02 15:50:38 TR_Pelgas_02052023
#> 52         4 43.69851 -1.469653     2 2023-05-02 16:05:19 TR_Pelgas_02052023
#> 53         4 43.80130 -1.476755     2 2023-05-02 16:43:38 TR_Pelgas_02052023
#> 54         3 43.73210 -1.481883     2 2023-05-02 17:42:37 TR_Pelgas_02052023
#> 55         3 43.68237 -1.475183     2 2023-05-02 17:59:50 TR_Pelgas_02052023
#> 56         3 43.66989 -1.472877     2 2023-05-02 18:05:57 TR_Pelgas_02052023
#> 57         2 43.66556 -1.466675     2 2023-05-02 18:38:59 TR_Pelgas_02052023
#> 58         2 43.66679 -1.573552     2 2023-05-02 19:12:50 TR_Pelgas_02052023
#> 59         2 44.06663 -1.463055     2 2023-05-03 11:42:57 TR_Pelgas_03052023
#> 60         3 44.06499 -1.376242     2 2023-05-03 11:20:58 TR_Pelgas_03052023
#> 61         3 44.00823 -1.385700     2 2023-05-03 10:59:12 TR_Pelgas_03052023
#> 62         3 43.86493 -1.414633     2 2023-05-03 10:09:08 TR_Pelgas_03052023
#> 63         3 43.86657 -1.459827     2 2023-05-03 09:57:05 TR_Pelgas_03052023
#> 64         4 43.86662 -1.557158     2 2023-05-03 09:32:47 TR_Pelgas_03052023
#> 65         5 43.86662 -1.685983     2 2023-05-03 09:00:42 TR_Pelgas_03052023
#> 66         5 43.86636 -1.675062     2 2023-05-03 07:05:20 TR_Pelgas_03052023
#> 67         5 43.86668 -1.696012     2 2023-05-03 06:59:26 TR_Pelgas_03052023
#> 68         5 43.86550 -1.921447     2 2023-05-03 06:01:11 TR_Pelgas_03052023
#> 69         4 43.86744 -2.132380     2 2023-05-03 05:04:38 TR_Pelgas_03052023
#> 70         2 44.06658 -1.861267     2 2023-05-03 17:29:42 TR_Pelgas_03052023
#> 71         2 44.06929 -1.983970     2 2023-05-03 17:59:36 TR_Pelgas_03052023
#> 72         2 44.06919 -2.141175     2 2023-05-03 18:38:08 TR_Pelgas_03052023
#> 73         3 44.06792 -2.170788     2 2023-05-03 18:46:09 TR_Pelgas_03052023
#> 74         3 44.06719 -2.108542     2 2023-05-03 19:08:52 TR_Pelgas_03052023
#> 75         5 43.86674 -1.735730     2 2023-05-03 08:48:04 TR_Pelgas_03052023
#> 76         2 44.06712 -1.593177     2 2023-05-03 14:16:18 TR_Pelgas_03052023
#> 77         2 44.06691 -1.758630     2 2023-05-03 14:57:58 TR_Pelgas_03052023
#> 78         2 44.06677 -1.819348     2 2023-05-03 15:13:22 TR_Pelgas_03052023
#> 79         2 44.06643 -1.808538     2 2023-05-03 17:16:43 TR_Pelgas_03052023
#> 80         3 44.46733 -1.410538     2 2023-05-04 17:02:02 TR_Pelgas_04052023
#> 81         3 44.46717 -1.656520     2 2023-05-04 16:00:30 TR_Pelgas_04052023
#> 82         3 44.46544 -1.759077     2 2023-05-04 15:34:33 TR_Pelgas_04052023
#> 83         2 44.46695 -1.868108     2 2023-05-04 13:00:38 TR_Pelgas_04052023
#> 84         1 44.46695 -2.097442     2 2023-05-04 12:01:54 TR_Pelgas_04052023
#> 85         1 44.46407 -2.171770     2 2023-05-04 11:42:53 TR_Pelgas_04052023
#> 86         2 44.34653 -2.173178     2 2023-05-04 11:04:13 TR_Pelgas_04052023
#> 87         2 44.27203 -2.169782     2 2023-05-04 10:40:09 TR_Pelgas_04052023
#> 88         2 44.26658 -2.009163     2 2023-05-04 09:59:53 TR_Pelgas_04052023
#> 89         3 44.26671 -1.876653     2 2023-05-04 09:27:58 TR_Pelgas_04052023
#> 90         3 44.26674 -1.768298     2 2023-05-04 09:01:22 TR_Pelgas_04052023
#> 91         3 44.26673 -1.654330     2 2023-05-04 08:31:11 TR_Pelgas_04052023
#> 92         4 44.26705 -1.679912     2 2023-05-04 06:27:58 TR_Pelgas_04052023
#> 93         4 44.26543 -1.569597     2 2023-05-04 06:00:49 TR_Pelgas_04052023
#> 94         4 44.26712 -1.423523     2 2023-05-04 05:24:49 TR_Pelgas_04052023
#> 95         4 44.26653 -1.340803     2 2023-05-04 05:01:15 TR_Pelgas_04052023
#> 96         1 44.86590 -2.071722     2 2023-05-05 18:12:20 TR_Pelgas_05052023
#> 97         1 44.86556 -2.109273     2 2023-05-05 16:09:18 TR_Pelgas_05052023
#> 98         1 44.86259 -1.971833     2 2023-05-05 15:34:53 TR_Pelgas_05052023
#> 99         1 44.86146 -1.833515     2 2023-05-05 14:59:43 TR_Pelgas_05052023
#> 100        1 44.86630 -1.592198     2 2023-05-05 13:56:44 TR_Pelgas_05052023
#> 101        2 44.86685 -1.382215     2 2023-05-05 13:00:05 TR_Pelgas_05052023
#> 102        2 44.86648 -1.293905     2 2023-05-05 12:36:24 TR_Pelgas_05052023
#> 103        2 44.85961 -1.261617     2 2023-05-05 11:02:33 TR_Pelgas_05052023
#> 104        2 44.66669 -1.299417     2 2023-05-05 09:57:40 TR_Pelgas_05052023
#> 105        2 44.66667 -1.420497     2 2023-05-05 09:28:06 TR_Pelgas_05052023
#> 106        3 44.66674 -1.533472     2 2023-05-05 09:00:36 TR_Pelgas_05052023
#> 107        3 44.66703 -1.662727     2 2023-05-05 08:28:20 TR_Pelgas_05052023
#> 108        3 44.66669 -1.726378     2 2023-05-05 06:59:52 TR_Pelgas_05052023
#> 109        3 44.66693 -1.876063     2 2023-05-05 06:19:18 TR_Pelgas_05052023
#> 110        3 44.66775 -1.944145     2 2023-05-05 06:00:30 TR_Pelgas_05052023
#> 111        3 44.66762 -2.078158     2 2023-05-05 05:24:32 TR_Pelgas_05052023
#> 112        3 44.66659 -2.145623     2 2023-05-05 05:06:42 TR_Pelgas_05052023
#> 113        3 44.86633 -2.832978     2 2023-05-06 18:55:09 TR_Pelgas_06052023
#> 114        3 44.86497 -2.742936     2 2023-05-06 18:29:31 TR_Pelgas_06052023
#> 115        3 44.86647 -2.633106     2 2023-05-06 18:01:17 TR_Pelgas_06052023
#> 116        4 44.86737 -2.565462     2 2023-05-06 17:43:35 TR_Pelgas_06052023
#> 117        4 44.86692 -2.534207     2 2023-05-06 17:35:07 TR_Pelgas_06052023
#> 118        4 44.86686 -2.398185     2 2023-05-06 17:00:02 TR_Pelgas_06052023
#> 119        4 44.86641 -2.240468     2 2023-05-06 16:19:03 TR_Pelgas_06052023
#> 120        3 44.94741 -2.449603     2 2023-05-06 15:04:34 TR_Pelgas_06052023
#> 121        3 44.99183 -2.564955     2 2023-05-06 14:32:53 TR_Pelgas_06052023
#> 122        3 45.00123 -2.447793     2 2023-05-06 14:00:51 TR_Pelgas_06052023
#> 123        3 45.01361 -2.219213     2 2023-05-06 12:59:17 TR_Pelgas_06052023
#> 124        3 45.01709 -2.161103     2 2023-05-06 12:43:32 TR_Pelgas_06052023
#> 125        2 45.02001 -2.090913     2 2023-05-06 12:24:35 TR_Pelgas_06052023
#> 126        2 45.02243 -2.056787     2 2023-05-06 10:02:39 TR_Pelgas_06052023
#> 127        2 45.02971 -1.923398     2 2023-05-06 09:30:10 TR_Pelgas_06052023
#> 128        2 45.03695 -1.791483     2 2023-05-06 08:58:10 TR_Pelgas_06052023
#> 129        2 45.04993 -1.553835     2 2023-05-06 07:59:57 TR_Pelgas_06052023
#> 130        3 45.05303 -1.497665     2 2023-05-06 07:46:10 TR_Pelgas_06052023
#> 131        3 45.06329 -1.310023     2 2023-05-06 06:59:49 TR_Pelgas_06052023
#> 132        3 45.06669 -1.251577     2 2023-05-06 04:58:55 TR_Pelgas_06052023
#> 133        4 45.18405 -2.079468     2 2023-05-07 05:02:51 TR_Pelgas_07052023
#> 134        4 45.25750 -1.877227     2 2023-05-07 05:59:24 TR_Pelgas_07052023
#> 135        4 45.26577 -1.854465     2 2023-05-07 06:06:26 TR_Pelgas_07052023
#> 136        3 45.24926 -1.903855     2 2023-05-07 07:45:26 TR_Pelgas_07052023
#> 137        3 45.26691 -1.856192     2 2023-05-07 07:59:23 TR_Pelgas_07052023
#> 138        3 45.34071 -1.655363     2 2023-05-07 08:57:11 TR_Pelgas_07052023
#> 139        3 45.38260 -1.541213     2 2023-05-07 09:29:33 TR_Pelgas_07052023
#> 140        3 45.42027 -1.438477     2 2023-05-07 09:58:07 TR_Pelgas_07052023
#> 141        3 45.44042 -1.383417     2 2023-05-07 10:13:46 TR_Pelgas_07052023
#> 142        3 45.43809 -1.388863     2 2023-05-07 11:55:42 TR_Pelgas_07052023
#> 143        3 45.48705 -1.258422     2 2023-05-07 12:30:55 TR_Pelgas_07052023
#> 144        3 45.40737 -1.248596     2 2023-05-07 13:00:55 TR_Pelgas_07052023
#> 145        4 45.27746 -1.225622     2 2023-05-07 13:45:18 TR_Pelgas_07052023
#> 146        4 45.25456 -1.352710     2 2023-05-07 16:06:44 TR_Pelgas_07052023
#> 147        4 45.24526 -1.426027     2 2023-05-07 16:26:15 TR_Pelgas_07052023
#> 148        4 45.23406 -1.557770     2 2023-05-07 16:59:30 TR_Pelgas_07052023
#> 149        4 45.22268 -1.681450     2 2023-05-07 17:30:25 TR_Pelgas_07052023
#> 150        4 45.20898 -1.798352     2 2023-05-07 17:58:45 TR_Pelgas_07052023
#> 151        4 45.19121 -1.982373     2 2023-05-07 18:43:09 TR_Pelgas_07052023
#> 152        4 45.18841 -2.022597     2 2023-05-07 18:52:44 TR_Pelgas_07052023
#> 153        4 45.18290 -2.079720     2 2023-05-07 19:07:19 TR_Pelgas_07052023
#> 154        3 45.31341 -2.236223     2 2023-05-08 15:59:35 TR_Pelgas_08052023
#> 155        3 45.36372 -2.102680     2 2023-05-08 17:32:02 TR_Pelgas_08052023
#> 156        3 45.39557 -2.029133     2 2023-05-08 18:01:12 TR_Pelgas_08052023
#> 157        3 45.44938 -1.919985     2 2023-05-08 18:47:06 TR_Pelgas_08052023
#> 158        3 45.41942 -1.990185     2 2023-05-08 14:45:32 TR_Pelgas_08052023
#> 159        3 45.38169 -2.075697     2 2023-05-08 15:11:25 TR_Pelgas_08052023
#> 160        2 45.56505 -1.631292     2 2023-05-08 07:58:58 TR_Pelgas_08052023
#> 161        2 45.56701 -1.625895     2 2023-05-08 10:06:09 TR_Pelgas_08052023
#> 162        2 45.48345 -1.829738     2 2023-05-08 11:03:37 TR_Pelgas_08052023
#> 163        2 45.40838 -2.018373     2 2023-05-08 11:59:21 TR_Pelgas_08052023
#> 164        2 45.49885 -1.279925     2 2023-05-08 05:11:33 TR_Pelgas_08052023
#> 165        2 45.63988 -1.368848     2 2023-05-08 06:01:38 TR_Pelgas_08052023
#> 166        2 45.66143 -1.379637     2 2023-05-08 06:13:11 TR_Pelgas_08052023
#> 167        2 45.66633 -1.377585     2 2023-05-08 06:46:02 TR_Pelgas_08052023
#> 168        2 45.64978 -1.424393     2 2023-05-08 07:00:08 TR_Pelgas_08052023
#> 169        2 45.60297 -1.538688     2 2023-05-08 07:32:12 TR_Pelgas_08052023
#> 170        2 45.59086 -1.568208     2 2023-05-08 07:40:32 TR_Pelgas_08052023
#> 171        4 45.79745 -1.577220     2 2023-05-09 07:36:45 TR_Pelgas_09052023
#> 172        5 45.76247 -1.668540     2 2023-05-09 07:59:32 TR_Pelgas_09052023
#> 173        5 45.66698 -1.912517     2 2023-05-09 09:00:16 TR_Pelgas_09052023
#> 174        5 45.61862 -2.029575     2 2023-05-09 09:29:25 TR_Pelgas_09052023
#> 175        5 45.55495 -2.200912     2 2023-05-09 12:09:33 TR_Pelgas_09052023
#> 176        5 45.49645 -2.336938     2 2023-05-09 12:53:28 TR_Pelgas_09052023
#> 177        5 45.43933 -2.298870     2 2023-05-09 13:14:51 TR_Pelgas_09052023
#> 178        6 45.33602 -2.224528     2 2023-05-09 13:54:23 TR_Pelgas_09052023
#> 179        6 45.23946 -2.421037     2 2023-05-09 14:59:33 TR_Pelgas_09052023
#> 180        6 45.15494 -2.624870     2 2023-05-09 15:59:03 TR_Pelgas_09052023
#> 181        6 45.13350 -2.672238     2 2023-05-09 16:13:05 TR_Pelgas_09052023
#> 182        6 45.13860 -2.656072     2 2023-05-09 18:15:20 TR_Pelgas_09052023
#> 183        6 45.05087 -2.882780     2 2023-05-09 19:23:06 TR_Pelgas_09052023
#> 184        5 45.21903 -3.274230     2 2023-05-10 09:29:00 TR_Pelgas_10052023
#> 185        5 45.16386 -3.198098     2 2023-05-10 08:59:21 TR_Pelgas_10052023
#> 186        5 45.25105 -2.976433     2 2023-05-10 07:58:23 TR_Pelgas_10052023
#> 187        5 45.28888 -2.879845     2 2023-05-10 07:31:40 TR_Pelgas_10052023
#> 188        5 45.29965 -2.852212     2 2023-05-10 07:24:00 TR_Pelgas_10052023
#> 189        5 45.33526 -2.761530     2 2023-05-10 06:58:37 TR_Pelgas_10052023
#> 190        5 45.41434 -2.555813     2 2023-05-10 05:59:27 TR_Pelgas_10052023
#> 191        5 45.51176 -2.307012     2 2023-05-10 04:47:27 TR_Pelgas_10052023
#> 192        4 45.70468 -2.385918     2 2023-05-10 17:01:47 TR_Pelgas_10052023
#> 193        4 45.61657 -2.603170     2 2023-05-10 15:59:44 TR_Pelgas_10052023
#> 194        4 45.52848 -2.819027     2 2023-05-10 14:59:09 TR_Pelgas_10052023
#> 195        4 45.45122 -2.999645     2 2023-05-10 14:08:46 TR_Pelgas_10052023
#> 196        5 45.37167 -3.198298     2 2023-05-10 11:03:01 TR_Pelgas_10052023
#> 197        5 45.27858 -3.358432     2 2023-05-10 10:02:12 TR_Pelgas_10052023
#> 198        3 46.11626 -1.400350     2 2023-05-11 07:49:08 TR_Pelgas_11052023
#> 199        3 46.09778 -1.445447     2 2023-05-11 08:01:28 TR_Pelgas_11052023
#> 200        3 46.01426 -1.648328     2 2023-05-11 08:59:25 TR_Pelgas_11052023
#> 201        3 45.96890 -1.758028     2 2023-05-11 09:30:08 TR_Pelgas_11052023
#> 202        4 45.92376 -1.867233     2 2023-05-11 10:00:34 TR_Pelgas_11052023
#> 203        4 45.87726 -1.981062     2 2023-05-11 10:33:16 TR_Pelgas_11052023
#> 204        3 45.89155 -1.945575     2 2023-05-11 12:24:47 TR_Pelgas_11052023
#> 205        3 45.84146 -2.064492     2 2023-05-11 12:59:55 TR_Pelgas_11052023
#> 206        3 45.76403 -2.263277     2 2023-05-11 13:58:22 TR_Pelgas_11052023
#> 207        4 45.73881 -2.326273     2 2023-05-11 14:17:26 TR_Pelgas_11052023
#> 208        4 45.72601 -2.357572     2 2023-05-11 14:26:31 TR_Pelgas_11052023
#> 209        4 45.71011 -2.395805     2 2023-05-11 14:37:38 TR_Pelgas_11052023
#> 210        4 45.69201 -2.440365     2 2023-05-11 14:50:38 TR_Pelgas_11052023
#> 211        5 45.69306 -2.425573     2 2023-05-11 16:59:58 TR_Pelgas_11052023
#> 212        5 45.64594 -2.537718     2 2023-05-11 17:32:33 TR_Pelgas_11052023
#> 213        5 45.63201 -2.571233     2 2023-05-11 17:42:01 TR_Pelgas_11052023
#> 214        5 45.60997 -2.638060     2 2023-05-11 18:01:55 TR_Pelgas_11052023
#> 215        5 45.61777 -2.675245     2 2023-05-11 18:40:56 TR_Pelgas_11052023
#> 216        5 45.58046 -2.705470     2 2023-05-11 18:59:01 TR_Pelgas_11052023
#> 217        4 45.50136 -3.479072     2 2023-05-12 04:45:38 TR_Pelgas_12052023
#> 218        4 45.60492 -3.223160     2 2023-05-12 05:57:41 TR_Pelgas_12052023
#> 219        4 45.61178 -3.208010     2 2023-05-12 06:02:17 TR_Pelgas_12052023
#> 220        4 45.59851 -3.235115     2 2023-05-12 07:53:26 TR_Pelgas_12052023
#> 221        4 45.70226 -2.981193     2 2023-05-12 09:04:54 TR_Pelgas_12052023
#> 222        4 45.72579 -2.921263     2 2023-05-12 09:21:49 TR_Pelgas_12052023
#> 223        4 45.72464 -2.926447     2 2023-05-12 09:57:56 TR_Pelgas_12052023
#> 224        4 45.79122 -2.756760     2 2023-05-12 10:47:17 TR_Pelgas_12052023
#> 225        4 45.77232 -2.798603     2 2023-05-12 13:07:02 TR_Pelgas_12052023
#> 226        4 45.84485 -2.622112     2 2023-05-12 13:58:06 TR_Pelgas_12052023
#> 227        4 45.93173 -2.405263     2 2023-05-12 15:00:31 TR_Pelgas_12052023
#> 228        5 46.00335 -2.223680     2 2023-05-12 15:53:05 TR_Pelgas_12052023
#> 229        5 46.01480 -2.195620     2 2023-05-12 16:01:00 TR_Pelgas_12052023
#> 230        5 46.05684 -2.095787     2 2023-05-12 16:30:06 TR_Pelgas_12052023
#> 231        5 46.13745 -1.891177     2 2023-05-12 17:26:56 TR_Pelgas_12052023
#> 232        5 46.18537 -1.776303     2 2023-05-12 17:59:37 TR_Pelgas_12052023
#> 233        5 46.23626 -1.648897     2 2023-05-12 18:35:20 TR_Pelgas_12052023
#> 234        4 46.39124 -1.829512     2 2023-05-14 11:09:49 TR_Pelgas_14052023
#> 235        4 46.09046 -2.592268     2 2023-05-14 18:03:14 TR_Pelgas_14052023
#> 236        4 46.09266 -2.587308     2 2023-05-14 16:14:27 TR_Pelgas_14052023
#> 237        4 46.11645 -2.526903     2 2023-05-14 15:57:16 TR_Pelgas_14052023
#> 238        4 46.20551 -2.301895     2 2023-05-14 14:55:24 TR_Pelgas_14052023
#> 239        4 46.29039 -2.080722     2 2023-05-14 13:54:58 TR_Pelgas_14052023
#> 240        4 46.30717 -2.041115     2 2023-05-14 12:11:14 TR_Pelgas_14052023
#> 241        2 46.41582 -1.768147     2 2023-05-14 09:31:14 TR_Pelgas_14052023
#> 242        2 46.25509 -1.669707     2 2023-05-14 08:29:51 TR_Pelgas_14052023
#> 243        2 46.14786 -1.477908     2 2023-05-14 07:29:00 TR_Pelgas_14052023
#> 244        2 46.11992 -1.352840     2 2023-05-14 06:57:18 TR_Pelgas_14052023
#> 245        3 46.11975 -1.352265     2 2023-05-14 06:57:10 TR_Pelgas_14052023
#> 246        3 46.10783 -1.289952     2 2023-05-14 06:41:41 TR_Pelgas_14052023
#> 247        3 46.03640 -2.757685     2 2023-05-15 12:12:17 TR_Pelgas_15052023
#> 248        4 46.06776 -2.773192     2 2023-05-15 12:01:05 TR_Pelgas_15052023
#> 249        4 46.20185 -2.878652     2 2023-05-15 11:12:54 TR_Pelgas_15052023
#> 250        4 46.21954 -2.850297     2 2023-05-15 11:02:34 TR_Pelgas_15052023
#> 251        3 46.33403 -2.562227     2 2023-05-15 09:40:29 TR_Pelgas_15052023
#> 252        3 46.41418 -2.360603     2 2023-05-15 07:01:11 TR_Pelgas_15052023
#> 253        2 46.48847 -2.173077     2 2023-05-15 06:06:14 TR_Pelgas_15052023
#> 254        2 46.52877 -2.071383     2 2023-05-15 05:36:59 TR_Pelgas_15052023
#> 255        2 46.58221 -1.933153     2 2023-05-15 04:58:26 TR_Pelgas_15052023
#> 256        4 45.79591 -3.334248     2 2023-05-15 15:00:22 TR_Pelgas_15052023
#> 257        4 45.87113 -3.144245     2 2023-05-15 14:06:02 TR_Pelgas_15052023
#> 258        4 45.94154 -2.968010     2 2023-05-15 13:15:56 TR_Pelgas_15052023
#> 259        5 45.61543 -3.776523     2 2023-05-15 19:13:16 TR_Pelgas_15052023
#> 260        5 45.72243 -3.518997     2 2023-05-15 17:56:57 TR_Pelgas_15052023
#> 261        4 46.21189 -2.862632     2 2023-05-16 04:57:54 TR_Pelgas_16052023
#> 262        4 46.12169 -3.095723     2 2023-05-16 06:04:36 TR_Pelgas_16052023
#> 263        4 46.02585 -3.335978     2 2023-05-16 07:14:28 TR_Pelgas_16052023
#> 264        4 45.96206 -3.495828     2 2023-05-16 08:00:38 TR_Pelgas_16052023
#> 265        4 45.91227 -3.627672     2 2023-05-16 08:41:08 TR_Pelgas_16052023
#> 266        4 45.90961 -3.626102     2 2023-05-16 10:22:35 TR_Pelgas_16052023
#> 267        4 45.85437 -3.766060     2 2023-05-16 11:03:41 TR_Pelgas_16052023
#> 268        4 45.81255 -3.880127     2 2023-05-16 11:38:00 TR_Pelgas_16052023
#> 269        4 45.87206 -3.960158     2 2023-05-16 12:05:01 TR_Pelgas_16052023
#> 270        4 45.95999 -4.072917     2 2023-05-16 12:44:26 TR_Pelgas_16052023
#> 271        4 45.96324 -4.069785     2 2023-05-16 12:45:55 TR_Pelgas_16052023
#> 272        4 45.98727 -4.014935     2 2023-05-16 13:02:09 TR_Pelgas_16052023
#> 273        3 46.03196 -3.903383     2 2023-05-16 13:35:25 TR_Pelgas_16052023
#> 274        3 46.06624 -3.818828     2 2023-05-16 14:00:03 TR_Pelgas_16052023
#> 275        3 46.14411 -3.625923     2 2023-05-16 14:54:43 TR_Pelgas_16052023
#> 276        3 46.23568 -3.398782     2 2023-05-16 15:59:17 TR_Pelgas_16052023
#> 277        3 46.32128 -3.191788     2 2023-05-16 16:59:55 TR_Pelgas_16052023
#> 278        4 46.49285 -2.759908     2 2023-05-17 15:15:41 TR_Pelgas_17052023
#> 279        2 46.67938 -2.290447     2 2023-05-17 17:34:59 TR_Pelgas_17052023
#> 280        2 46.66105 -2.339830     2 2023-05-17 17:21:04 TR_Pelgas_17052023
#> 281        3 46.63462 -2.405702     2 2023-05-17 17:02:13 TR_Pelgas_17052023
#> 282        4 46.55160 -2.612568     2 2023-05-17 16:00:34 TR_Pelgas_17052023
#> 283        3 46.39258 -3.009550     2 2023-05-17 14:00:52 TR_Pelgas_17052023
#> 284        3 46.35188 -3.111447     2 2023-05-17 13:30:47 TR_Pelgas_17052023
#> 285        3 46.34750 -3.120393     2 2023-05-17 10:56:19 TR_Pelgas_17052023
#> 286        3 46.32032 -3.191530     2 2023-05-17 10:36:35 TR_Pelgas_17052023
#> 287        3 46.32417 -3.201503     2 2023-05-17 10:33:30 TR_Pelgas_17052023
#> 288        3 46.40331 -3.241797     2 2023-05-17 10:05:34 TR_Pelgas_17052023
#> 289        3 46.49395 -3.288122     2 2023-05-17 09:33:20 TR_Pelgas_17052023
#> 290        3 46.50058 -3.292890     2 2023-05-17 09:30:20 TR_Pelgas_17052023
#> 291        3 46.45253 -3.412800     2 2023-05-17 08:58:24 TR_Pelgas_17052023
#> 292        3 46.36754 -3.623603     2 2023-05-17 08:01:12 TR_Pelgas_17052023
#> 293        3 46.27854 -3.843193     2 2023-05-17 06:59:36 TR_Pelgas_17052023
#> 294        3 46.19854 -4.038805     2 2023-05-17 05:59:59 TR_Pelgas_17052023
#> 295        3 46.15156 -4.156403     2 2023-05-17 05:22:21 TR_Pelgas_17052023
#> 296        3 46.11899 -4.236803     2 2023-05-17 04:57:19 TR_Pelgas_17052023
#> 297        3 46.10457 -4.271765     2 2023-05-17 04:46:54 TR_Pelgas_17052023
#> 298        3 46.91855 -2.473760     2 2023-05-18 11:02:28 TR_Pelgas_18052023
#> 299        3 46.88071 -2.399398     2 2023-05-18 10:41:20 TR_Pelgas_18052023
#> 300        3 46.86680 -2.382823     2 2023-05-18 10:34:18 TR_Pelgas_18052023
#> 301        3 46.81469 -2.512277     2 2023-05-18 10:00:14 TR_Pelgas_18052023
#> 302        3 46.77351 -2.615437     2 2023-05-18 09:32:23 TR_Pelgas_18052023
#> 303        3 46.70402 -2.788500     2 2023-05-18 08:44:47 TR_Pelgas_18052023
#> 304        3 46.60468 -3.032765     2 2023-05-18 06:02:28 TR_Pelgas_18052023
#> 305        3 46.55464 -3.160003     2 2023-05-18 05:25:10 TR_Pelgas_18052023
#> 306        3 46.53403 -3.211033     2 2023-05-18 05:09:41 TR_Pelgas_18052023
#> 307        3 46.50411 -3.284680     2 2023-05-18 04:47:40 TR_Pelgas_18052023
#> 308        3 46.70340 -3.369065     2 2023-05-18 18:21:44 TR_Pelgas_18052023
#> 309        3 46.74167 -3.271407     2 2023-05-18 17:55:40 TR_Pelgas_18052023
#> 310        3 46.75668 -3.237117     2 2023-05-18 17:46:19 TR_Pelgas_18052023
#> 311        3 46.75326 -3.232288     2 2023-05-18 17:21:42 TR_Pelgas_18052023
#> 312        3 46.78255 -3.167740     2 2023-05-18 17:03:44 TR_Pelgas_18052023
#> 313        3 46.78266 -3.167453     2 2023-05-18 17:03:38 TR_Pelgas_18052023
#> 314        3 46.86568 -2.956110     2 2023-05-18 16:03:32 TR_Pelgas_18052023
#> 315        3 46.93332 -2.783348     2 2023-05-18 15:15:00 TR_Pelgas_18052023
#> 316        1 47.00854 -2.590650     2 2023-05-18 13:00:34 TR_Pelgas_18052023
#> 317        2 47.01362 -2.436788     2 2023-05-18 11:33:06 TR_Pelgas_18052023
#> 318        2 47.24758 -3.123762     2 2023-05-19 16:21:54 TR_Pelgas_19052023
#> 319        2 47.25292 -3.111652     2 2023-05-19 15:53:55 TR_Pelgas_19052023
#> 320        2 47.19679 -3.248165     2 2023-05-19 15:14:36 TR_Pelgas_19052023
#> 321        3 47.09053 -3.502532     2 2023-05-19 12:02:55 TR_Pelgas_19052023
#> 322        3 47.03599 -3.631738     2 2023-05-19 11:25:40 TR_Pelgas_19052023
#> 323        2 47.23542 -2.671225     2 2023-05-19 04:42:27 TR_Pelgas_19052023
#> 324        3 47.10786 -2.940188     2 2023-05-19 06:02:28 TR_Pelgas_19052023
#> 325        4 47.02881 -3.147747     2 2023-05-19 06:59:43 TR_Pelgas_19052023
#> 326        4 46.98656 -3.249643     2 2023-05-19 07:29:02 TR_Pelgas_19052023
#> 327        3 46.99061 -3.241232     2 2023-05-19 09:10:48 TR_Pelgas_19052023
#> 328        3 46.96455 -3.307808     2 2023-05-19 09:29:06 TR_Pelgas_19052023
#> 329        3 46.91862 -3.415273     2 2023-05-19 10:00:03 TR_Pelgas_19052023
#> 330        3 46.88892 -3.501568     2 2023-05-19 10:24:21 TR_Pelgas_19052023
#> 331        3 46.88892 -3.501568     2 2023-05-19 10:24:23 TR_Pelgas_19052023
#> 332        3 46.97718 -3.581608     2 2023-05-19 11:00:53 TR_Pelgas_19052023
#> 333        3 47.02958 -3.632700     2 2023-05-19 11:23:07 TR_Pelgas_19052023
#> 334        2 47.25857 -2.910215     2 2023-05-19 17:25:38 TR_Pelgas_19052023
#> 335        3 47.30029 -2.982142     2 2023-05-19 17:04:55 TR_Pelgas_19052023
#> 336        3 46.23291 -4.560243     2 2023-05-20 18:55:56 TR_Pelgas_20052023
#> 337        4 46.23366 -4.557310     2 2023-05-20 18:11:38 TR_Pelgas_20052023
#> 338        4 46.25102 -4.514353     2 2023-05-20 17:59:04 TR_Pelgas_20052023
#> 339        4 46.28228 -4.435470     2 2023-05-20 17:36:34 TR_Pelgas_20052023
#> 340        4 46.32819 -4.319353     2 2023-05-20 17:02:52 TR_Pelgas_20052023
#> 341        4 46.38220 -4.183165     2 2023-05-20 16:24:19 TR_Pelgas_20052023
#> 342        4 46.41867 -4.091745     2 2023-05-20 13:57:38 TR_Pelgas_20052023
#> 343        4 46.49488 -3.897718     2 2023-05-20 13:02:40 TR_Pelgas_20052023
#> 344        4 46.50726 -3.865772     2 2023-05-20 12:53:16 TR_Pelgas_20052023
#> 345        4 46.56800 -3.712793     2 2023-05-20 11:02:38 TR_Pelgas_20052023
#> 346        4 46.65460 -3.493053     2 2023-05-20 10:00:17 TR_Pelgas_20052023
#> 347        5 46.70558 -3.364840     2 2023-05-20 09:27:27 TR_Pelgas_20052023
#> 348        5 46.70280 -3.364705     2 2023-05-20 09:21:38 TR_Pelgas_20052023
#> 349        5 46.70461 -3.438545     2 2023-05-20 09:02:45 TR_Pelgas_20052023
#> 350        5 46.70951 -3.675975     2 2023-05-20 08:00:02 TR_Pelgas_20052023
#> 351        4 46.71162 -3.905303     2 2023-05-20 07:00:23 TR_Pelgas_20052023
#> 352        4 46.71508 -3.946278     2 2023-05-20 06:46:46 TR_Pelgas_20052023
#> 353        4 46.78043 -3.779783     2 2023-05-20 05:57:55 TR_Pelgas_20052023
#> 354        4 46.86927 -3.551617     2 2023-05-20 04:55:10 TR_Pelgas_20052023
#> 355        3 46.36077 -4.843985     2 2023-05-21 04:32:57 TR_Pelgas_21052023
#> 356        4 46.40133 -4.745542     2 2023-05-21 05:02:11 TR_Pelgas_21052023
#> 357        4 46.47570 -4.556597     2 2023-05-21 05:59:57 TR_Pelgas_21052023
#> 358        4 46.54975 -4.367815     2 2023-05-21 07:00:06 TR_Pelgas_21052023
#> 359        5 46.62470 -4.177057     2 2023-05-21 08:01:39 TR_Pelgas_21052023
#> 360        5 46.69561 -3.995892     2 2023-05-21 08:59:33 TR_Pelgas_21052023
#> 361        5 46.71362 -3.950298     2 2023-05-21 09:13:59 TR_Pelgas_21052023
#> 362        5 46.72564 -3.956142     2 2023-05-21 09:19:15 TR_Pelgas_21052023
#> 363        5 46.75749 -3.972615     2 2023-05-21 09:31:28 TR_Pelgas_21052023
#> 364        4 46.83646 -4.012092     2 2023-05-21 10:01:45 TR_Pelgas_21052023
#> 365        4 46.99985 -4.089878     2 2023-05-21 11:02:46 TR_Pelgas_21052023
#> 366        4 47.02232 -4.097293     2 2023-05-21 11:10:48 TR_Pelgas_21052023
#> 367        4 47.02180 -4.111445     2 2023-05-21 11:14:32 TR_Pelgas_21052023
#> 368        4 46.94370 -4.262243     2 2023-05-21 12:00:09 TR_Pelgas_21052023
#> 369        4 46.83022 -4.469930     2 2023-05-21 13:04:20 TR_Pelgas_21052023
#> 370        4 46.73690 -4.636903     2 2023-05-21 13:57:40 TR_Pelgas_21052023
#> 371        2 46.74592 -4.619618     2 2023-05-21 15:36:14 TR_Pelgas_21052023
#> 372        2 46.70403 -4.696038     2 2023-05-21 15:59:44 TR_Pelgas_21052023
#> 373        3 46.59530 -4.889712     2 2023-05-21 17:00:18 TR_Pelgas_21052023
#> 374        2 46.52307 -5.018405     2 2023-05-21 17:38:18 TR_Pelgas_21052023
#> 375        3 46.51286 -5.017845     2 2023-05-21 18:19:57 TR_Pelgas_21052023
#> 376        2 47.27289 -3.674438     2 2023-05-22 11:59:56 TR_Pelgas_22052023
#> 377        2 47.32659 -3.577822     2 2023-05-22 12:29:39 TR_Pelgas_22052023
#> 378        2 47.31435 -3.599975     2 2023-05-22 14:39:37 TR_Pelgas_22052023
#> 379        1 47.35526 -3.525488     2 2023-05-22 15:03:10 TR_Pelgas_22052023
#> 380        2 47.40777 -3.429653     2 2023-05-22 15:33:09 TR_Pelgas_22052023
#> 381        2 47.45795 -3.339757     2 2023-05-22 16:00:57 TR_Pelgas_22052023
#> 382        3 47.50288 -3.260092     2 2023-05-22 16:27:40 TR_Pelgas_22052023
#> 383        3 47.51385 -3.236292     2 2023-05-22 16:34:43 TR_Pelgas_22052023
#> 384        3 47.51966 -3.235498     2 2023-05-22 16:37:11 TR_Pelgas_22052023
#> 385        3 47.57939 -3.266362     2 2023-05-22 17:00:17 TR_Pelgas_22052023
#> 386        3 47.62114 -3.287890     2 2023-05-22 17:15:57 TR_Pelgas_22052023
#> 387        3 47.16885 -3.861848     2 2023-05-22 11:00:33 TR_Pelgas_22052023
#> 388        3 47.03824 -3.629390     2 2023-05-22 05:07:16 TR_Pelgas_22052023
#> 389        3 46.96012 -3.816405     2 2023-05-22 06:00:33 TR_Pelgas_22052023
#> 390        4 46.92246 -3.906428     2 2023-05-22 06:26:24 TR_Pelgas_22052023
#> 391        4 46.90539 -3.947327     2 2023-05-22 06:38:25 TR_Pelgas_22052023
#> 392        5 46.90837 -3.953915     2 2023-05-22 06:41:05 TR_Pelgas_22052023
#> 393        5 46.94228 -3.998748     2 2023-05-22 06:59:36 TR_Pelgas_22052023
#> 394        4 46.98711 -4.057800     2 2023-05-22 07:24:12 TR_Pelgas_22052023
#> 395        4 47.02121 -4.105975     2 2023-05-22 07:43:22 TR_Pelgas_22052023
#> 396        4 47.02904 -4.113440     2 2023-05-22 07:47:54 TR_Pelgas_22052023
#> 397        4 47.04931 -4.077060     2 2023-05-22 08:00:47 TR_Pelgas_22052023
#> 398        4 47.10206 -3.981857     2 2023-05-22 08:33:48 TR_Pelgas_22052023
#> 399        4 47.09550 -3.994157     2 2023-05-22 10:16:50 TR_Pelgas_22052023
#> 400        3 47.08275 -4.334258     2 2023-05-23 04:35:34 TR_Pelgas_23052023
#> 401        4 47.12968 -4.259030     2 2023-05-23 05:00:49 TR_Pelgas_23052023
#> 402        4 47.23609 -4.087787     2 2023-05-23 05:59:52 TR_Pelgas_23052023
#> 403        4 47.34641 -3.910043     2 2023-05-23 07:00:45 TR_Pelgas_23052023
#> 404        4 47.45682 -3.734017     2 2023-05-23 07:59:52 TR_Pelgas_23052023
#> 405        3 47.48927 -3.684302     2 2023-05-23 08:16:38 TR_Pelgas_23052023
#> 406        3 47.56903 -3.556617     2 2023-05-23 08:58:01 TR_Pelgas_23052023
#> 407        3 47.60075 -3.499845     2 2023-05-23 09:15:58 TR_Pelgas_23052023
#> 408        3 47.60393 -3.503163     2 2023-05-23 09:17:44 TR_Pelgas_23052023
#> 409        3 47.62223 -3.563017     2 2023-05-23 09:32:14 TR_Pelgas_23052023
#> 410        3 47.66472 -3.691852     2 2023-05-23 10:04:05 TR_Pelgas_23052023
#> 411        3 47.70023 -3.800330     2 2023-05-23 10:32:16 TR_Pelgas_23052023
#> 412        3 47.69999 -3.801205     2 2023-05-23 10:32:31 TR_Pelgas_23052023
#> 413        2 47.64916 -3.870090     2 2023-05-23 10:57:36 TR_Pelgas_23052023
#> 414        2 47.51146 -4.059498     2 2023-05-23 12:06:53 TR_Pelgas_23052023
#> 415        2 47.50501 -4.075248     2 2023-05-23 12:13:12 TR_Pelgas_23052023
#> 416        2 47.51771 -4.050078     2 2023-05-23 13:55:46 TR_Pelgas_23052023
#> 417        2 47.42966 -4.171092     2 2023-05-23 14:42:29 TR_Pelgas_23052023
#> 418        3 47.42983 -4.171527     2 2023-05-23 17:18:35 TR_Pelgas_23052023
#> 419        3 47.39785 -4.215817     2 2023-05-23 17:33:59 TR_Pelgas_23052023
#> 420        4 47.34137 -4.293140     2 2023-05-23 18:01:04 TR_Pelgas_23052023
#> 421        4 47.25054 -4.418480     2 2023-05-23 18:44:12 TR_Pelgas_23052023
#> 422        4 47.87853 -4.401098     2 2023-05-24 17:00:49 TR_Pelgas_24052023
#> 423        4 47.75481 -4.564940     2 2023-05-24 16:01:37 TR_Pelgas_24052023
#> 424        2 47.73776 -4.587507     2 2023-05-24 15:53:32 TR_Pelgas_24052023
#> 425        3 47.68707 -4.654717     2 2023-05-24 15:29:15 TR_Pelgas_24052023
#> 426        3 47.61477 -4.749888     2 2023-05-24 13:00:43 TR_Pelgas_24052023
#> 427        4 47.49501 -4.907770     2 2023-05-24 12:00:47 TR_Pelgas_24052023
#> 428        4 47.42110 -5.003927     2 2023-05-24 11:21:54 TR_Pelgas_24052023
#> 429        4 47.40622 -4.991602     2 2023-05-24 11:00:51 TR_Pelgas_24052023
#> 430        4 47.29460 -4.795330     2 2023-05-24 09:59:15 TR_Pelgas_24052023
#> 431        4 47.29305 -4.790793     2 2023-05-24 09:57:46 TR_Pelgas_24052023
#> 432        4 47.33626 -4.736217     2 2023-05-24 09:39:08 TR_Pelgas_24052023
#> 433        4 47.41999 -4.626367     2 2023-05-24 07:02:01 TR_Pelgas_24052023
#> 434        4 47.54907 -4.460057     2 2023-05-24 06:02:59 TR_Pelgas_24052023
#> 435        4 47.61231 -4.378707     2 2023-05-24 05:33:08 TR_Pelgas_24052023
#> 436        3 47.73288 -4.222270     2 2023-05-24 04:35:43 TR_Pelgas_24052023
#> 437        4 47.90740 -4.462137     2 2023-05-24 17:35:42 TR_Pelgas_24052023
#> 438        4 47.89843 -4.453255     2 2023-05-24 17:31:53 TR_Pelgas_24052023
#> 439        4 47.86139 -4.416185     2 2023-05-24 17:16:04 TR_Pelgas_24052023
#> 440        4 47.19373 -5.688752     2 2023-05-25 18:00:08 TR_Pelgas_25052023
#> 441        5 47.24271 -5.625617     2 2023-05-25 17:37:04 TR_Pelgas_25052023
#> 442        5 47.33692 -5.503690     2 2023-05-25 14:57:29 TR_Pelgas_25052023
#> 443        4 47.45596 -5.349397     2 2023-05-25 14:00:11 TR_Pelgas_25052023
#> 444        3 47.56898 -5.202288     2 2023-05-25 13:06:13 TR_Pelgas_25052023
#> 445        3 47.64227 -5.107515     2 2023-05-25 12:31:16 TR_Pelgas_25052023
#> 446        3 47.64194 -5.106050     2 2023-05-25 10:20:36 TR_Pelgas_25052023
#> 447        3 47.68533 -5.050910     2 2023-05-25 10:00:53 TR_Pelgas_25052023
#> 448        3 47.74121 -4.978192     2 2023-05-25 09:35:16 TR_Pelgas_25052023
#> 449        3 47.73131 -4.990807     2 2023-05-25 07:36:16 TR_Pelgas_25052023
#> 450        3 47.80922 -4.889155     2 2023-05-25 07:00:19 TR_Pelgas_25052023
#> 451        3 47.93429 -4.725805     2 2023-05-25 06:01:24 TR_Pelgas_25052023
#> 452        2 47.96720 -4.682857     2 2023-05-25 05:46:02 TR_Pelgas_25052023
#> 453        0 47.97051 -4.677252     2 2023-05-25 05:44:07 TR_Pelgas_25052023
#> 454        2 47.94050 -4.486867     2 2023-05-25 04:57:08 TR_Pelgas_25052023
#> 455        3 47.41431 -5.013953     2 2023-05-26 04:35:18 TR_Pelgas_26052023
#> 456        3 47.35375 -5.093457     2 2023-05-26 05:04:10 TR_Pelgas_26052023
#> 457        3 47.33794 -5.116247     2 2023-05-26 05:12:27 TR_Pelgas_26052023
#> 458        4 47.34425 -5.105922     2 2023-05-26 07:00:59 TR_Pelgas_26052023
#> 459        5 47.21527 -5.275178     2 2023-05-26 08:01:23 TR_Pelgas_26052023
#> 460        5 47.09144 -5.437012     2 2023-05-26 09:01:27 TR_Pelgas_26052023
#> 461        4 47.02226 -5.527480     2 2023-05-26 09:33:11 TR_Pelgas_26052023
#> 462        4 46.97021 -5.595367     2 2023-05-26 09:57:02 TR_Pelgas_26052023
#> 463        5 46.96774 -5.594785     2 2023-05-26 09:58:18 TR_Pelgas_26052023
#> 464        5 46.83524 -5.458973     2 2023-05-26 10:58:08 TR_Pelgas_26052023
#> 465        6 46.80600 -5.434645     2 2023-05-26 11:10:09 TR_Pelgas_26052023
#> 466        5 46.80522 -5.425533     2 2023-05-26 11:12:56 TR_Pelgas_26052023
#> 467        5 46.88535 -5.312767     2 2023-05-26 12:01:33 TR_Pelgas_26052023
#> 468        5 46.99283 -5.175448     2 2023-05-26 13:02:26 TR_Pelgas_26052023
#> 469        4 46.99539 -5.172225     2 2023-05-26 14:51:48 TR_Pelgas_26052023
#> 470        4 47.01287 -5.149785     2 2023-05-26 15:00:46 TR_Pelgas_26052023
#> 471        3 47.13289 -4.996188     2 2023-05-26 16:00:26 TR_Pelgas_26052023
#> 472        3 47.26053 -4.831967     2 2023-05-26 17:00:05 TR_Pelgas_26052023
#> 473        3 47.65215 -4.672653     2 2023-05-27 18:00:41 TR_Pelgas_27052023
#> 474        3 47.60088 -4.604033     2 2023-05-27 17:30:22 TR_Pelgas_27052023
#> 475        2 47.54833 -4.533278     2 2023-05-27 16:58:21 TR_Pelgas_27052023
#> 476        2 47.54702 -4.532007     2 2023-05-27 13:46:32 TR_Pelgas_27052023
#> 477        2 47.52182 -4.492288     2 2023-05-27 13:29:42 TR_Pelgas_27052023
#> 478        1 47.51919 -4.489055     2 2023-05-27 13:28:03 TR_Pelgas_27052023
#> 479        1 47.51089 -4.486018     2 2023-05-27 13:24:10 TR_Pelgas_27052023
#> 480        2 47.45994 -4.471468     2 2023-05-27 13:01:08 TR_Pelgas_27052023
#> 481        2 47.32150 -4.431933     2 2023-05-27 12:00:44 TR_Pelgas_27052023
#> 482        3 47.26514 -4.416287     2 2023-05-27 11:39:44 TR_Pelgas_27052023
#> 483        3 47.25395 -4.413180     2 2023-05-27 11:35:20 TR_Pelgas_27052023
#> 484        3 47.24324 -4.427475     2 2023-05-27 11:30:01 TR_Pelgas_27052023
#> 485        4 47.18629 -4.505505     2 2023-05-27 11:01:27 TR_Pelgas_27052023
#> 486        4 47.10452 -4.617157     2 2023-05-27 10:19:12 TR_Pelgas_27052023
#> 487        4 47.06459 -4.671225     2 2023-05-27 09:31:44 TR_Pelgas_27052023
#> 488        3 47.03271 -4.714940     2 2023-05-27 09:15:06 TR_Pelgas_27052023
#> 489        3 47.00974 -4.746028     2 2023-05-27 07:01:32 TR_Pelgas_27052023
#> 490        3 46.88610 -4.914272     2 2023-05-27 06:00:47 TR_Pelgas_27052023
#> 491        3 46.78777 -5.047783     2 2023-05-27 05:10:51 TR_Pelgas_27052023
#> 492        3 46.71118 -5.152110     2 2023-05-27 04:31:02 TR_Pelgas_27052023
#> 493        3 48.13341 -5.140008     2 2023-05-28 05:32:08 TR_Pelgas_28052023
#> 494        3 48.13320 -5.083678     2 2023-05-28 05:47:04 TR_Pelgas_28052023
#> 495        3 48.13322 -5.068995     2 2023-05-28 07:28:59 TR_Pelgas_28052023
#> 496        3 48.13347 -4.939017     2 2023-05-28 08:00:28 TR_Pelgas_28052023
#> 497        3 48.13319 -4.789572     2 2023-05-28 08:38:12 TR_Pelgas_28052023
#> 498        3 48.13341 -4.786688     2 2023-05-28 09:12:25 TR_Pelgas_28052023
#> 499        3 48.13333 -4.703868     2 2023-05-28 09:31:55 TR_Pelgas_28052023
#> 500        3 48.13327 -4.569918     2 2023-05-28 10:03:35 TR_Pelgas_28052023
#> 501        3 48.13308 -4.337520     2 2023-05-28 10:58:39 TR_Pelgas_28052023
#> 502        5 48.22930 -4.894888     2 2023-05-29 08:10:47 TR_Pelgas_29052023
#> 503        4 48.32958 -5.159487     2 2023-05-29 05:15:17 TR_Pelgas_29052023
#> 504        4 48.26232 -4.980678     2 2023-05-29 06:07:05 TR_Pelgas_29052023
#> 505        4 48.30806 -4.613903     2 2023-05-29 11:15:28 TR_Pelgas_29052023
#> 506        4 48.20609 -4.677230     2 2023-05-29 10:32:35 TR_Pelgas_29052023
#> 507        5 48.18542 -4.650650     2 2023-05-29 09:18:07 TR_Pelgas_29052023
#> 508        5 48.18640 -4.761967     2 2023-05-29 08:50:04 TR_Pelgas_29052023
```

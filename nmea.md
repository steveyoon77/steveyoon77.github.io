# GPS NMEA
## $GPGGA
Global Positioning System Fix Data

Example:
```$GPGGA,134658.00,5106.9792,N,11402.3003,W,2,09,1.0,1048.47,M,-16.27,M,08,AAAA*60```

|Structure |Description |Symbol |Example |
|:-- |:-- |:-- |:-- |
|$GPGGA |Log header | |$GPGGA |
|utc |UTC time status of position (hours/minutes/seconds/ decimal seconds) |hhmmss.ss |202134.00 |
|lat |Latitude (DDmm.mm) |llll.ll |5106.9847 |
|lat dir |Latitude direction (N=North, S=South) |a |N |
|lon |Longitude (DDDmm.mm) |yyyyy.yy |11402.2986 |
|lon dir |Longitude direction(E=East, W=West) |a |W |
|quality |refer to "GPS Quality Indicators" | x |1 |
|# sats |Number of satelites in use. May be different to the number in view |xx |10 |
|hdop |Horizontal dilution of precision | x.x |1.0 |
|alt |Antenna altitude above/below mean sea level |x.x |1062.22 |
|a-units |Units of antenna altitude (M=metres) |M |M|
|undulation |Undulation - the relationship between the geoid and the WGS84 ellipsiod |x.x |-16.271 |
|u-units |Units of undulation(M=metres) |M |M |
|age |Age of correction data (in seconds). The maximum age reported here is limited to 99 sec. |xx |(empty when no differential data is present) |
|stn ID |Differential base station ID |xxx |(empty when no differential data is present) |
|\*xx |Checksum |\*hh |\*48 |
|{CR}{LF} |Sentence terminator | |{CR}{LF} |

GPS Quality Indicators:

|Indicator |Description |
|:-- |:-- |
|0 |Fix not available or invalid |
|1 |Single point<br/>Converging PPP(TerraStar-L) |
|2 |Pseudo-range differential<br/>Converged PPP(TerraStar-L)<br/>Converging PPP(TerraStar-C, TerraStar-C PRO, TerraStar-X) |
|4 |RTK fixed ambiguity solution |
|5 |RTK floating ambiguity solution<br/>Converged PPP(TerraStar-C, TerraSTar-C PRO, TerraSTar-X) |
|6 |Dead reckoning mode |
|7 |Manual input mode (fixed position) |
|8 |Simulator mode |
|9 |WAAS(SBAS) |

## $GPGLL
Geographic position

Example:
```
$GPGLL,5107.0013414,N,11402.3279144,W,205412.00,A,A*73
```

|Structure |Description |Example |
|:-- |:-- |:-- |
|$GPGLL |Log header |$GPGLL |
|lat |Latitude (DDmm.mm) |5106.7198674 |
|lat dir |Latitude direction (N = North, S = South) |N |
|lon |Longitude (DDDmm.mm) |11402.3587526 |
|lon dir |Longitude direction (E = East, W = West) |W |
|utc |UTC time status of position (hours/minutes/seconds/decimal seconds) |220152.50 |
|data status |Data status: A = Data valid, V = Data invalid |A |
|mode ind |Positioning system mode indicator, see Table: NMEA Positioning System Mode Indicator |A |
|\*xx |Check sum |*1B |
|{CR}{LF} |Sentence terminator |{CR}{LF} |

NMEA Positioning System Mode Indicator:

|Mode |Indicator |
|:-- |:-- |
|A |Autonomous |
|D |Differential |
|E |Estimated (dead reckoning) mode |
|M |Manual input |
|N |Data not valid |

## $GPGSA
GPS DOP and active satellites

Example: 
```
$GPGSA,M,3,17,02,30,04,05,10,09,06,31,12,,,1.2,0.8,0.9*35
```

|Structure |Description |Symbol |Example |
|:-- |:-- |:-- |:-- |
|$GPGSA |Log header | |$GPGSA |
|mode MA |A = Automatic 2D/3D<br/>M = Manual, forced to operate in 2D or 3D |M |M |
|mode 123 |Mode: 1 = Fix not available; 2 = 2D; 3 = 3D |x |3 |
|prn |PRN numbers of satellites used in solution (null for unused fields), total of 12 fields<br/><li><ul>GPS = 1 to 32</ul><ul>SBAS = 33 to 64 (add 87 for PRN number)</ul><ul>GLO = 65 to 96</ul></li>|xx,xx,..... |18,03,13,25,16,24,12,20,,,, |
|pdop |Position dilution of precision |x.x |1.5 |
|hdop |Horizontal dilution of precision |x.x |0.9 |
|vdop |Vertical dilution of precision |x.x |1.2 |
|system ID |GNSS system ID. GPS System ID = 1, L1 C/A Signal ID = 1 | | |
|\*xx |Checksum |\*hh |\*3F |
|{CR}{LF} |Sentence terminator |{CR}{LF} |

## $GPGSV
GPS Satellites in View

Example:
```
$GPGSV,3,1,11,18,87,050,48,22,56,250,49,21,55,122,49,03,40,284,47*78
$GPGSV,3,2,11,19,25,314,42,26,24,044,42,24,16,118,43,29,15,039,42*7E
$GPGSV,3,3,11,09,15,107,44,14,11,196,41,07,03,173,*4D
$GLGSV,2,1,06,65,64,037,41,66,53,269,43,88,39,200,44,74,25,051,*64
$GLGSV,2,2,06,72,16,063,35,67,01,253,*66
```

|Structure |Description |Symbol |Example |
|:-- |:-- |:-- |:-- |
|$GPGSV |Log header | |$GPGSV |
|# msgs |Total number of messages (1-9) |x |3 |
|msg # |Message number (1-9) |x |1 |
|# sats |Total number of satellites in view. May be different than the number of satellites in use |xx |09 |
|prn |Satellites PRN number<br/><li><ul>GPS = 1 to 32</ul><ul>Galileo = 1 to 36</ul><ul>BeiDou = 1 to 63</ul><ul>NavIC = 1 to 14</ul><ul>QZSS = 1 to 10</ul><ul>SBAS = 33 to 64 (add 87 for PRN#s)</ul><ul>GLONASS = 65 to 96</ul></li> |xx |03 |
|elev |Elevation, degree, Max 90 |xx |51 |
|azimuth |Azimuth, degree True, 000 to 359 |xxx |140 |
|SNR |SNR (C/No) 00-99dB, null when not tracking |xx |42 |
|... |Next satellite PRN number, elev, azimuth, SNR | | |
|system ID |GNSS system ID | | |
|\*xx |Checksum |\*hh |\*72 |
|{CR}{LR} |Sentence terminator | |{CR}{LR} |

## $GPRMC
GPS specific information

Example:
```
$GPRMC,144326.00,A,5107.0017737,N,11402.3291611,W,0.080,323.3,210307,0.0,E,A*20
```

|Structure |Field Description |Symbol |Example |
|:-- |:-- |:-- |:-- |
|$GPRMC |Log header | |$GPRMC |
|utc |UTC of position |hhmmss.ss |144326.00 |
|pos status |Position status (A = data valid, V = data invalid) |A |A |
|lat |Latitude (DDmm.mm) |llll.ll |5107.0017737 |
|lat dir |Latitude direction: (N = North, S = South) |a |N |
|lon |Longitude (DDDmm.mm) |yyyyy.yy |11402.3291611 |
|lon dir |Longitude direction: (E = East, W = West) |a |W |
|speed Kn |Speed over ground, knots |x.x |0.080 |
|track true |Track made good, degrees True |x.x |323.3|
|date |Date: dd/mm/yy |xxxxxx |210307 |
|mag var |Magnetic variation, degrees |Note that this field is the actual magnetic variation and will always be positive. The direction of the magnetic variation is always positive. |x.x |0.0 |
|var dir |Magnetic variation direction E/W |Easterly variation (E) subtracts from True course.
Westerly variation (W) adds to True course. |a |E |
|mode ind |Positioning system mode indicator, see Table: NMEA Positioning System Mode Indicator |a |A |
|\*xx |Checksum |\*hh |\*20 |
|{CR}{LR} |Sentence terminator | |{CR}{LR} |

NMEA Positioning System Mode Indicator:

|Mode |Indicator |
|:-- |:-- |
|A |Autonomous |
|D |Differential |
|E |Estimated (dead reckoning) mode |
|M |Manual input |
|N |Data not valid |
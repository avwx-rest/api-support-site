# Data Sources

## Station List

Station data is compiled from two primary sources: [OurAirports] and NOAA's [Aviation Weather Center]. The resulting list includes operating airports, heliports, and standalone weather stations like ocean buoys. AVWX also manages each station's reporting status, i.e. does the airport produce METAR/TAF instead of AWOS/ASOS which are not supported. The list is recompiled about once a month.

If you find any issues with the station data, either [email me] or submit an edit at [OurAirports] so it can be included in the next update.

## Aviation and Atmospheric Weather

### NOAA

Unless otherwise specified, all aviation reports are sourced from NOAA ADDS based in the United States. While not perfect, it has provided the widest global coverage in a single location for the most important types of aviation weather reports.

### METAR & TAF

NOAA is used as the default provider for METAR and TAF reports, but other regional sources are used if they report faster or more accurate updates.

- Australia: `AU` country code sourced from the [Australian Bureau of Meteorology]
- Korea: `RK` ICAO prefix sourced from [Korean Meteorological Administration]
- Columbia: `SK` ICAO prefix sourced from [Columbia Civil Aeronautics]


If you would like to see a regional source added to this list, [email me] with the source and any conflicting reports you may have encountered using AVWX.

[email me]: mailto:avwx@dupont.dev "Email Me"
[OurAirports]: https://ourairports.com "OurAirports"
[Aviation Weather Center]: https://aviationweather.gov "Aviation Weather Center"
[Australian Bureau of Meteorology]: http://www.bom.gov.au/aviation/ "Australian Bureau of Meteorology"
[Korean Meteorological Administration]: http://amoapi.kma.go.kr "Korean Meteorological Administration"
[Columbia Civil Aeronautics]: http://meteorologia.aerocivil.gov.co "Columbia Civil Aeronautics"
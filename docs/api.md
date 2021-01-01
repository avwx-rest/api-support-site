# API Usage

## Search

### Coordinates

When using coordinates instead of an ICAO code, the API will search for the nearest airport known to submit reports to the data source. 

There are times you may want to override these defaults. For example, setting `airport=false` will include independent weather stations like those out at sea. This could be useful to find the absolute closest weather observation, not just those useful for airport operations.

You may also wish to include non-reporting stations to a station search by setting `reporting=false` in the URL. This will include all airports which may be desired for routing purposes.

### Nearest

When using the nearest endpoints, the results are sorted by great circle distance with the closest stations appearing first. There are some limitations though. Internally, the search is performed using raw coordinate values on a (-180, 180) x (-90, 90) grid and iterated until the desired number of stations have been found matching the search criteria. This means:

- Coordinates searches will not cross the -180, 180 gap since they appear at either end of the naive grid .
- Searches near the poles start preferring longer latitude distances over shorter longitude distances.

These shouldn't be an issue for the vast majority of users, and the final results will still be ordered by their true distances.

## Common Gotchas

### Do I need to include all of those parameters?

Not unless it overrides a default value. For example, calling [https://avwx.rest/api/metar/KMCO]() will work just fine if the API token is in the header.

### Why is my report out of date?

AVWX uses a responsive short-term cache system for all report types. Normally, the cache is there to return the most recent report after non-24-hour stations and airports close for the night or if there is some short-term error with the report sources rather than returning an error response. Because of this, it's possible to receive a report that may be multiple days old as it represents the last time an AVWX user requested that specific report and one was available.

My recommendation is to add some client-side logic to check for the recency of the report. However, you can override the default functionality and have AVWX return an error code when a current report is not available by caching the `onfail` URL parameter to `error`.

# HTTP Codes

Here is a list of all supported HTTP status codes. Many non-200 responses include a sample response for development purposes, but it will always be in a `"sample"` field as to not conflict with successful fulfillment workflows.

## 200 Success

Normal success response for the requested resource.

## 204 No Data

This occurs when the data source doesn't return a report for the requested station or the station is known to not submit reports to the data source. This second field is usually static, so subsequent calls will also return a 204 code.

## 400 Client Error

Most 400 client errors are due to invalid URL parameters or unknown ICAO codes. AVWX only accepts 4-character ICAO codes of currently operating stations. Closed airports, IATA codes, and non-ICAO GPS codes are not recognized.

You may also receive this if no report is found from the data sources and nothing is available in the cache.

## 401 Missing Authorization

The endpoint requires authorization to access. Be sure to include your API token in the request header or as a URL parameter.

## 403 Unauthorized

The API token was rejected for one of the following reasons:

- Token value could not be found
- Token has been disabled by the user or admin
- User's plan type does not have access to the requested resource

## 429 Too Many Requests

The user's account or token has hit it's daily call limit. You can view your recent usage from the [account portal][token use]. If you need to increase your call limit, you can upgrade your plan or opt-in to overage billing.

## 500 Unknown Server Error

Error representing a code error not handled by any other HTTP code. Bug reports are automatically submitted for review. Subsequent retries are likely to fail.

## 502 Cannot Connect to Data Source

There was an issue fetching a report from the data source. This is usually a temporary issue and retries can be made shortly after.

## 503 Server Rebooting

The server is being updated and the request has been cancelled. Retry your connection immediately for the request to be queued.

[token use]: http://account.avwx.rest/token/usage "Token Usage Graph"
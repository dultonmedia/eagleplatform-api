## Using Eagle Platform server API

### Authentication

* Before using Server API you have to get your access credentials
* Every request should be authenticated by chosen method
* It is always better to use OAuth
* It is always better to use HTTPS

### Parameters

* Every request should contain account code variable as GET parameter

### Output

Our API provides JSON output for all requests.

Check API method reference for the detailed result descriptions.

In all cases field standards are:

* Date and time: ISO 8601
* Booleans: true / false

Every API output has the following structure:

* `time`: current server time in ISO 8601
* `version`: API version (“3.0”)
* `data`: object or array with output
* `errors`: Errors array. Could be empty or null in case of success answer.
* `status`: Response code. 200 for OK.

If result is a list it will include the following metadata:

* Total count of records found
* Index of the first element in array

If there is an error:

We use HTTP codes according to the standard to indicate an error. Detailed descrption may occur in `errors` field.

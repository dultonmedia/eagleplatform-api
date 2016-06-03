## Get list of records for filter

Returns record for filter by its ID. 

    GET http://api.eagleplatform.com/media/filters{id}/records.json

### Parameters

* `id` Filter ID. Can be obtained from Eagle Platform web interface
* `page` (optional) Current page. First page is 1
* `per_page` (optional) Amount of records to show per page.

#### Output

Array of records fields wrapped to "records" object.

### Example request

    curl -X GET "https://api.eagleplatform.com/media/filters/100500/records.json?account=myaccount&auth_token=mytoken"


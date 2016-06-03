## Get list of records for filter

Returns record for filter by its ID. 

    GET http://api.eagleplatform.com/media/filters/{id}.json

### Parameters

* `id` Filter ID. Can be obtained from Eagle Platform web interface
* `page` (optional) Current page. First page is 1
* `per_page` (optional) Amount of records to show per page.

#### Output

Basic data for filter with records object. Each record contains standard fields.

### Example request

    curl -X GET "https://api.eagleplatform.com/media/filters/100500.json?account=myaccount&auth_token=mytoken"

### Example output

    {
        "time": "2016-06-03T13:26:37+03:00",
        "version": "3.0",
        "data": {
            "id": 12344,
            "name": "Best videos",
            "total_entries": 492,
            "total_pages": 10,
            "current_page": 1,
            "records": [
                {
                    "id": 477768,
                    "name": "Video one",
                    "description": null,
                    ...

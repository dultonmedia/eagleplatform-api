## One record views statistics

Allows caller to get video statistics by its ID.

    GET http://api.eagleplatform.com/media/records/{id}/statistics.json
    
### Params

* `id` - Record ID
* `uniq` - Boolean, set true to get unique viewers statistics
* `date_from` - Date from which show statistics. Usually in format `dd.mm.yyyy`
* `date_to` - Date to which show statistics. Usually in format `dd.mm.yyyy`

### Response

You will receive an array of views per day.

### Example request

    curl -X GET "https://api.eagleplatform.com/media/records/100500/statistics.json?date_from=10.01.2016&date_to=20.01.2016&account=myaccount&auth_token=mytoken"


## One record views statistics by embed URL

Allows caller to get video statistics by its ID.

    GET http://api.eagleplatform.com/media/records/{id}/statistics_embed.json
    
### Params

* `id` - Record ID
* `uniq` - Boolean, set true to get unique viewers statistics
* `date_from` - Date from which show statistics. Usually in format `dd.mm.yyyy`
* `date_to` - Date to which show statistics. Usually in format `dd.mm.yyyy`

### Response

You will receive an array of views per day splitted by embed URL of player.

### Example request

    curl -X GET "https://api.eagleplatform.com/media/records/100500/statistics_embed.json?date_from=10.01.2016&date_to=20.01.2016&account=myaccount&auth_token=mytoken"

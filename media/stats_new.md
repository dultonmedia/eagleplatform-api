### Popular videos
Returns list of the most popular videos by view count
`https://eagle.media.eagleplatform.com/api/v2/stat/vod/popular.json?date_from=2015-01-01&date_to=2016-07-01`  
  
Params:  
`date_from`  
`date_to`  
`limit`  
  
Dates format for this and other requests: `yyyy-MM-dd`  
Default `limit` is 10.  
If both `date_from` and `date_to` are blank, results for current date are returning.  

### Embeds
Returns count of record views, coupled with embed URL and date.  
`https://eagle.media.eagleplatform.com/api/v2/stat/vod/embeds.json?date_from=2015-01-01&date_to=2016-07-01`    
  
Params:  
`date_from`  
`date_to`  
`record_id`  
`sum`  
If `record_id` is not presented, results for all account records are provided.  
If `sum` param is presented and set to 'true', just the amount of total views will be returned.  

### Views
Returns count of views and unique viewers, coupled with embed URL and date.  
`https://eagle.media.eagleplatform.com/api/v2/stat/vod/views.json?date_from=2015-01-01&date_to=2016-07-01`    
  
Params:  
`date_from`  
`date_to`  
`record_id`  
`sum`  
If `record_id` is not presented, results for all account records are provided.  
If `sum` param is presented and set to 'true', just the amount of total unique viewers will be returned.  

### Platforms
Returns count of record views coupled with client platform and date.  
`https://eagle.media.eagleplatform.com/api/v2/stat/vod/platforms.json?date_from=2015-01-01&date_to=2016-07-01&record_id=123`   

Params:  
`date_from`  
`date_to`  
`record_id`  
`sum`  
If `record_id` is not presented, results for all account records are provided.  
If `sum` param is presented and set to 'true', result is not splitted by date.


### Browsers
Returns count of record views coupled with client browsers and date.  
`https://eagle.media.eagleplatform.com/api/v2/stat/vod/browsers.json?date_from=2015-01-01&date_to=2016-07-01&record_id=123`   

Params:  
`date_from`  
`date_to`  
`record_id`  
`sum`  
If `record_id` is not presented, results for all account records are provided.  
If `sum` param is presented and set to 'true', result is not splitted by date.  


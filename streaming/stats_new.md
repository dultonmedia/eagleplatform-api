### Embeds
Returns count of translation views, coupled with embed URL and date.  
`https://eagle.auth.eagleplatform.com/api/v2/stat/live/embeds.json?date_from=2015-01-01&date_to=2016-07-01`    
  
Params:  
`date_from`  
`date_to`  
`translation_id`  
`sum`  
If `translation_id` is not presented, results for all account translations are provided.  
If `sum` param is presented and set to 'true', just the amount of total views will be returned.  

### Views
Returns count of views and unique viewers, coupled with embed URL and date.  
`https://eagle.auth.eagleplatform.com/api/v2/stat/live/views.json?date_from=2015-01-01&date_to=2016-07-01`    
  
Params:  
`date_from`  
`date_to`  
`translation_id`  
`sum`  
If `translation_id` is not presented, results for all account translations are provided.  
If `sum` param is presented and set to 'true', just the amount of total unique viewers will be returned.  

### Viewers count  
Returns count of viewers at particular time.  
`https://eagle.auth.eagleplatform.com/api/v2/stat/live/viewers_count.json?date_from=2015-01-01&date_to=2016-07-01&translation_id_id=123`     

Params:  
`date_from`  
`date_to`  
`translation_id`  

Example output: {"data":[{"time":"2017-06-05 12:24:58","cnt":"1"},{"time":"2017-06-05 12:25:14","cnt":"1"},{"time":"2017-06-05 12:25:28","cnt":"1"},{"time":"2017-06-05 12:25:53","cnt":"1"}]}    
  
### Max viewers count  
Returns maximum count of viewers within the date range.  
`https://eagle.auth.eagleplatform.com/api/v2/stat/live/max_viewers_count.json?date_from=2015-01-01&date_to=2016-07-01&translation_id_id=123`   

Example: {  
  "data": 6  
}  

Params:  
`date_from`  
`date_to`  
`translation_id`  



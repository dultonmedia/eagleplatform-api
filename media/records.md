## Record object

All record-related API methods will accept or return record object parameters as described below.

* `id` Unique Record ID
* `name` Record name as would be displayed in player
* `is_hd` Boolean indicator if processed record will have height of 720 px or more
* `description` Record description
* `tags` Tags list as array
* `duration` Duration in milliseconds
* `origin` Temporary link to download originally uploaded video file
* `origin_size` Size of originally uploaded video file
* `albums` Array of album IDs
* `is_processed` Boolean flag showing if record was fully processed
* `screenshots` Array of screenshot URLs
* `current_screenshot` URL of current screenshot
* `view_count` Count of views
* `click_url` URL related to the record
* `user_id` ID of record owner
* `recorded_at` Date of record. Can be manually changed
* `updated_at` Date of record last update.
* `created_at` Date of record creation.

Record will also include all fields defined on Metadata management page.

* `record_files` Array of converted video files

## Get record

### Returns record object by its ID. Record fields are wrapped to "record" object.

    GET http://api.eagleplatform.com/media/records/{id}.json

Example request

    curl -X GET "https://api.eagleplatform.com/media/records/100500.json?account=myaccount&auth_token=mytoken"

Example output

    {
      "time": "2016-04-06T13:26:16+03:00",
      "version": "3.0",
      "data": {
        "record": {
          "id": 100500,
          "name": "My video blog record one",
          "description": null,
          "duration": 164000,
          ...


## Create record

Creates record. Record fields should be passed as request fields wrapped with record object

    POST http://api.eagleplatform.com/media/records.json
    record[name]="New record"

### Download video from HTTP/FTP URL

You can pass additional parameters when creating record to ask platform to download video.

Use source field containing two attributes:

* `type` – `ftp` or `http`
* `parameters` – attibutes object depending on selected type

Parameters for FTP:

* `host` – server hostname, e.g. `ftp.source.ru`
* `file` – absolute path to the file, e.g. `/videos/video.mp4`
* `username` – FTP login
* `password` – FTP password

Для скачки с HTTP

* `url` – Full video file URL, e.g. `http://videos.ru/video.mp4`

### Updating custom screenshot

Pass URL or data to custom_screenshot field to update screenshot

## Update record

Updates record. Record fields should be passed as request fields wrapped with record object.

    PUT http://api.eagleplatform.com/media/records/{id}.json

## Delete record

    DELETE http://api.eagleplatform.com/media/records/{id}.json

Moves video file to recycle bin.
    

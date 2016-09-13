## Translation object

All record-related API methods will accept or return record object parameters as described below.

* `id` – unique translation ID
* `name` – name of translation
* `status` – status (online / offline)
* `description` – description
* `stream_name` – unique stream name used in broadcaster
* `created_at` – date of creation
* `updated_at` – date of latest update
* `starts_at` – date of start, if defined by announce
* `ad_template_id` – ID of used advertisement template
* `age_restrictions_type` – class of age restrictions
* `country_access_template_id` – ID of country access restrictions template
* `player_template_id` – player template ID
* `site_access_template_id` - ID of domain access template
* `user` - ID of user created the translation 

## Get translations list

Returns array of translation objects. Translation fields are wrapped to "translation" object.

    GET http://api.eagleplatform.com/media/streaming/translations.json

## Get translation

Returns translation object by its ID. Translation fields are wrapped to "translation" object.

    GET http://api.eagleplatform.com/media/streaming/translations/{id}.json

Example request

    curl -X GET "https://api.eagleplatform.com/streaming/translations/100500.json?account=myaccount&auth_token=mytoken"

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


## Create translation

Creates a new translation. Pass the translation fields as request fields wrapped with translation object

    POST http://api.eagleplatform.com/streaming/translations.json
    translation[name]="New translation"


### Updating translation

    PUT http://api.eagleplatform.com/streaming/translations/{id}.json

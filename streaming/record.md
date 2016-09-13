## Controlling record status

Each broadcast may have records. User can control record state

### Start record

Starts record.

    PUT http://api.eagleplatform.com/streaming/translations/{id}/rec.json

### Stop record

Stops recording and saves video file to mediahosting.

    PUT http://api.eagleplatform.com/streaming/translations/{id}/stop_rec.json


## Controlling translation states

Each translation can have 3 states:

* Stopped
* Started
* Paused

Using these states you can control the player appearance without interrupting incoming video stream.

### Start

Starts stopped translation.

    PUT http://api.eagleplatform.com/streaming/translations/{id}/start.json

### Pause

Pauses started translation.

    PUT http://api.eagleplatform.com/streaming/translations/{id}/pause.json

### Finish

Stops started or paused translation.

    PUT http://api.eagleplatform.com/streaming/translations/{id}/finish.json

### Resume

Resumes paused translation.

    PUT http://api.eagleplatform.com/streaming/translations/{id}/resume.json


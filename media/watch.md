## Receiving direct video URL

Allows caller to get direct video URL for using it inside 3rd party players or mobile apps.

Please note that link could be requested *every time* when you want to show content. It has expire time, 
and it is also linked to IP adress of those who will be able to watch video.

Currently this API allows to get HLS type video stream URL only. In case if you need other popular format please contact support.


    GET http://api.eagleplatform.com/media/records/{id}/watch.json
    
Params

* `ip` - IP address of viewer. You can skip it: we will sign video URL with IP address of `watch` API method caller.

Example request

    curl -X GET "https://api.eagleplatform.com/media/records/100500/watch.json?ip=123.132.123.213&account=myaccount&auth_token=mytoken"

You will get list of video URLs. Use first one for most cases. Other URLs are secondary and provided for fallback.

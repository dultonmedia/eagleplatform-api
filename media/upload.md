## Receiving upload link

Upload URL can be obtained by using create record or update record methods. 

It will be passed in `upload_link_chunked` field of server response.

This URL is protected by parameters and linked with IP address of those who will upload the file. 
By default it is IP address of record create/update API request caller. You can pass `ip` param to API to set another uploader. You can also pass `any` word as `ip` param to disable IP address check. However, it is not recommended to allow any IP address in production environment.

## Chunked upload request

Use link received as `upload_link_chunked` to make POST upload requests.

Chunked upload follows Blueimp File Upload client side code: https://github.com/blueimp/jQuery-File-Upload

Common requirements include:

* Always use `Content-Type` of file being uploaded (multipart/form-data; boundary=...)
* Use valid `Content-Disposition` (attachment; filename="file.mp4")
* Use valid `Content-Range` of chunks being uploaded

Pass the chunk to request payload inside boundary.

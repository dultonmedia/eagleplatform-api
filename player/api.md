# Eagle Player API

Methods and events are available from skins, plugins and externally from IFrame API. 

## Methods

To use methods just call them as regular methods of `player` object: `player.play();`

### Sizes

* `play` - starts video playback. Works everytime even if video is paused or stopped.
* `pause` - pauses video playback.
* `stop` - stops video playback.

### Sizes

* `getWidth` and `getHeight` - returns player dimensions as they seen in pixels
* `getVideoWidth` and `getVideoHeight` - returns video dimensions as they streamed
* `getDisplayVideoWidth` and `getDisplayVideoHeight` - returns video dimensions as they seen on display

## Events

To use events just use `on` subscription similar to JQuery. First parameter will be the event name and the second will be optional parameter depending on event type.

* `resize` - when size of player possibly changed.
* `fullscreen` - when player comes to fullscreen or from fullscreen. Passes boolean parameter, true indicates that fullscreen is enabled

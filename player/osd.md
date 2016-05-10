# On Screen Display

Player allows to show clickable areas over the video with optional captions.

To use this feature you have to provide SRT-formatted file.

## Format definition

Each SRT record would have the following format:

* 1 `ID according SRT specification`
* 00:00:17,000 --> 00:00:20,000 `Timing according SRT specification`
* 30:30:100:100 `Dimensions`
* http://eagleplatform.com `URL`
* Hello `(optional) Text`

## Dimensions definition

Dimensions are rectangle definition of (Top-Left X):(Top-Left Y):(Bottom-Right-X):(Bottom-Right-Y)

All the measures are in percents of video (not player).

Examples: 

* 0:0:100:100 will fill all video screen
* 40:40:60:60 will fill small area of 20% in the center of video

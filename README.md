# dateoverlay
add film date overlay over picture

#!/bin/bash
ffmpeg -i IMG_2665-6.jpg -filter_complex color=c=black@0.0:s=5776x3852,format=rgba,drawtext=fontsize=170:fontfile=MTC-7-Segment.ttf:text=24 04 28:fontcolor=#ff7515@0.9:x=4700:y=3400,boxblur=2[vf],[0:v][vf]overlay=alpha=1 -frames:v 1 result.jpg

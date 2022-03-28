# usps-maps-gif

from this thread: https://news.ycombinator.com/item?id=30822685

get all the PNG files

    cd img & wget https://postalpro.usps.com/mnt/glusterfs/ribbs/service_standards/svcmaps/orig/FCM/{005..999}\_FCM.png
    
FCM = First-Class Letters & Flats

create a GIF (using imagemagick's `convert`)

    convert -delay 10 -loop 0 img/*.png usps-maps.gif
    

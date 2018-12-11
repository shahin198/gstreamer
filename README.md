# gstreamer

# Gstreamer install
```
sudo apt-get install libgstreamer1.0-0 gstreamer1.0-plugins-base gstreamer1.0-plugins-good gstreamer1.0-plugins-bad gstreamer1.0-plugins-ugly gstreamer1.0-libav gstreamer1.0-doc gstreamer1.0-tools
```
# read video from file
```
gst-launch-1.0 -q filesrc location=video.mp4 ! decodebin ! jpegenc ! jpegparse ! jpegdec ! xvimagesink sync=true

gst-launch-1.0 filesrc location=video.mp4 ! decodebin ! pulsesink

```

https://software.intel.com/en-us/node/722575

# mix video file without gape
```
gst-launch-1.0 concat name=c ! queue ! avdec_h264 ! queue ! videoconvert ! videoscale ! autovideosink   filesrc location=1.mp4 ! qtdemux ! h264parse ! c.   filesrc location=2.mp4 ! qtdemux ! h264parse ! c.
```

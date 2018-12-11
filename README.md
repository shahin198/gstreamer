# gstreamer

# Gstreamer install
```
sudo apt-get install libgstreamer1.0-0 gstreamer1.0-plugins-base gstreamer1.0-plugins-good gstreamer1.0-plugins-bad gstreamer1.0-plugins-ugly gstreamer1.0-libav gstreamer1.0-doc gstreamer1.0-tools
```
# read video from file
```
gst-launch filesrc location=video.mp4 !decodebin2 name=dec ! queue ! ffmpegcolorspace ! autovideosink dec. ! queue ! audioconvert ! audioresample ! autoaudiosink
```


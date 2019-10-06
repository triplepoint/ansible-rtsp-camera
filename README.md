# Intro [![Build Status](https://travis-ci.org/triplepoint/ansible-rtsp-camera.svg?branch=master)](https://travis-ci.org/triplepoint/ansible-rtsp-camera)
Build, configure, and install the V4L2 RTSP camera streaming service at:
https://github.com/mpromonet/v4l2rtspserver

See the default variable comments in `defaults/main.yml` for information on configuration.

This deployment essentially uses two tools: `v4l2-ctl`, which configures the camera,
and `v4l2rtspserver`, which runs the RTSP stream.

`v4l2-ctl` configuration is best described at:
https://www.mankier.com/1/v4l2-ctl

While `v4l2rtspserver` is documented here:
https://github.com/mpromonet/v4l2rtspserver#usage

# Reference
- https://zoneminder.blogspot.com/p/rasbpeery-pi-zero-camera.html

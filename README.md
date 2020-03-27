# Intro [![Build Status](https://www.travis-ci.com/triplepoint/ansible-rtsp-camera.svg?branch=master)](https://www.travis-ci.com/triplepoint/ansible-rtsp-camera)
Build, configure, and install the V4L2 RTSP camera streaming service at:
https://github.com/mpromonet/v4l2rtspserver

See the default variable comments in `defaults/main.yml` for information on configuration.

This deployment essentially uses two tools: `v4l2-ctl`, which configures the camera,
and `v4l2rtspserver`, which runs the RTSP stream.

`v4l2-ctl` configuration is best described at:
https://www.mankier.com/1/v4l2-ctl

While `v4l2rtspserver` is documented here:
https://github.com/mpromonet/v4l2rtspserver#usage

## Requirements
None.

## Role Variables
See the [comment in the default variables file](defaults/main.yml) for information on configuration.

## Dependencies
None.

## Example Playbook
    - hosts: whatever
      roles:
        - triplepoint.rtsp_camera

## Role Testing
This role is tested with `molecule`, using `pipenv` to handle dependencies and the Python testing environment.

### Setting Up Your Execution Environment
``` sh
pip install pipenv
```

Once you have `pipenv` installed, you can build the execution virtualenv with:
``` sh
pipenv install --dev
```

### Running Tests
Once you have your environment configured, you can execute `molecule` with:
``` sh
pipenv run molecule test
```

### Regenerating the Lock File
You shouldn't have to do this very often, but if you change the Python package requirements using `pipenv install {some_package}` commands or by editing the `Pipfile` directly, or if you find the build dependencies have fallen out of date, you might need to regenerate the `Pipfile.lock`.
``` sh
pipenv update --dev
```
Be sure and check in the regenerated `Pipfile.lock` when this process is complete.

## License
MIT

# Notes
- https://zoneminder.blogspot.com/p/rasbpeery-pi-zero-camera.html

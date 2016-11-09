Appium
======

Appium server to run tests on Android devices.

This image has been created based on Selenium Base image: https://github.com/rgonalo/docker-appium

How to use this image
---------------------

#### Launch the image

Launch the image with *--privileged* option to allow docker instance to view connected USB devices:

``` bash
$ docker run -d -P -p 4723:4723 --privileged -v /dev/bus/usb:/dev/bus/usb --name appium totaldesigner/appium
```

#### Run Appium tests

Connect your Android mobile to the host via USB and execute your Appium tests on the remote server
*192.168.99.100:4723*.

You can tail Appium server logs with the following docker command:

``` bash
$ docker logs --follow appium
```

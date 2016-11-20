# Docker-chrome

Poc, to use chrome from docker from your desktop environement:
* X
* pulseaudio

```
docker run -it --rm
-v /run/user/$UID/pulse/native:/var/run/pulse/native 
-v /tmp/.X11-unix:/tmp/.X11-unix
-v chrome:/chrome/.config/chromium
-e DISPLAY=unix$DISPLAY who0/docker-chrome
```

Pulse socket should be exposed inside docker with *PULSE_SERVER=unix:/var/run/pulse/native*

You can add extra storage to save preferences, historique.
```
/chrome/.config/chromium
/chrome/.config/
```
>You need change folder's right to chrome user.

# R2D2 Audio container

## Use
It's important to note that imn order for this container to function correctly, the Pulse Audio interface MUST be passed into the container as well as the user details (normally user 1000). If these are not passed in (or if the raw audio device is passed into of the pulse interface) then the audio will not work correctly

```
sudo docker run -it -v .:/mnt -v /run/user/1000/pulse/native:/run/user/1000/pulse/native -e PULSE_SERVER=unix:/run/user/1000/pulse/native -u 1000:1000 <container_ID> bash
``` 
# asf-steam-client
dockerized https://github.com/JustArchi/ArchiSteamFarm/

At first you need to pull repo with default configs for ArchiSteamFarm
```cd $HOME; git clone https://github.com/fedya/asf-steam-client.git```

Then open config/firstbot.json and replace SteamLogin and SteamPassword values with own ones

to run it, just use:

```docker run -ti --volume=$HOME/asf-steam-client/config:/root/config asf```

After startup probably you need to enter verification code from steam


How to run GUI mono application in docker?
1. unmask second CMD string and mask first
2. run:

```docker run -ti -env=DISPLAY --volume=/tmp/.X11-unix:/tmp/.X11-unix:rw --volume=/home/fdrt/asf-steam-client/config:/root/config --volume=/tmp/.docker.xauth:/tmp/.docker.xauth:rw --env=XAUTHORITY=/tmp/.docker.xauth asf```


How to build container:
```docker build --tag=asf --file Dockerfile.asf .```

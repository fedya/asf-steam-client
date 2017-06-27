# asf-steam-client
dockerized https://github.com/JustArchi/ArchiSteamFarm/

At first you need to pull repo with default configs for ArchiSteamFarm
````cd $HOME; git clone https://github.com/fedya/asf-steam-client.git```

Then open config/firstbot.json and replace SteamLogin and SteamPassword values with own ones

to run it, just use:

```docker run -ti --volume=$HOME/asf-steam-client/config:/root/config asf```

After startup probably you need to enter verification code from steam

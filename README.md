<p align="center"><img src="https://raw.githubusercontent.com/titaniumnetwork-dev/Ultraviolet-Static/main/public/uv.png" height="200"></p>

<h1 align="center">Anything Hub</h1>

The deployable all-in-one bundle for [Ultraviolet](https://github.com/06NinjaKid06/Ultraviolet), a highly sophisticated proxy used for evading internet censorship or accessing websites in a controlled sandbox using the power of service workers and more!

## Deployment

[![Run on Replit](https://binbashbanana.github.io/deploy-buttons/buttons/remade/replit.svg)](https://github.com/06NinjaKid06/Anything-Hub/wiki/Run-on-Replit)
[![Deploy on Railway](https://binbashbanana.github.io/deploy-buttons/buttons/remade/railway.svg)](https://github.com/06NinjaKid06/Anything-Hub/wiki/Deploy-on-Railway)
[![Remix on Glitch](https://binbashbanana.github.io/deploy-buttons/buttons/remade/glitch.svg)](https://github.com/06NinjaKid06/Anything-Hub/wiki/Remix-on-Glitch)
[![Deploy to Koyeb](https://binbashbanana.github.io/deploy-buttons/buttons/remade/koyeb.svg)](https://github.com/06NinjaKid06/Anything-Hub/wiki/Deploy-to-Koyeb)

If you are deploying to an alternative service or a server, refer to [Deploy via terminal](https://github.com/06NinjaKid06/Anything-Hub/wiki/Deploy-via-terminal).

Additional information such as [customizing your frontend](https://github.com/06NinjaKid06/Anything-Hub/wiki/Customizing-your-frontend) can be found on the [wiki](https://github.com/06NinjaKid06/Anything-Hub/wiki).

Support and updates are in our [Discord Server](discord.gg/unblock).

> [!IMPORTANT]  
> Until deployed on a domain with a valid SSL certificate, Firefox cannot load the site. Use chromium for testing on localhost

### HTTP Transport
The example uses [EpoxyTransport](https://github.com/MercuryWorkshop/EpoxyTransport) to fetch proxied data encrypted. 

You may also want to use [CurlTransport](https://github.com/MercuryWorkshop/CurlTransport), a different way of fetching encrypted data, or [Bare-Client](https://github.com/MercuryWorkshop/Bare-as-module3), the legacy (unencrypted!) transport.

In public/register-sw.js, look for the line `BareMux.SetTransport("EpxMod.EpoxyClient", { wisp: "ws://localhost:8080/wisp" });`, which can be changed to any of the transports. Make sure to `importScripts` the transport's bundle in `public/uv/sw.js` and add a script tag in `public/404.html` and `public/index.html`. 

See the [bare-mux](https://github.com/MercuryWorkshop/bare-mux) documentation for more information

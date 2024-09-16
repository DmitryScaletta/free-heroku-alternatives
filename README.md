# Free Heroku Alternatives

Heroku [shuts down their free plans](https://twitter.com/heroku/status/1562817050565054469) so here are some free alternatives to deploy your backend applications.

This comparison describes only free tiers of these services.

See also [free database services](https://github.com/DmitryScaletta/free-database-services)

| | <sub>Shutdown for Inactivity</sub> | <sub>Credit Card Required</sub> | <sub>Free Tier Limits</sub> | <sub>RAM</sub> | <sub>Disk Space</sub> | <sub>Disk Write Access</sub> | <sub>Network Bandwidth</sub> | <sub>Docker-file</sub> | <sub>GitHub Integra-tion</sub> |
| ------------ | ---- | --- | -------------- | ----- | ------ | ---- | ------------- | --- | --- |
| fly.io       | No   | Yes |                | 256MB | 3GB    | Yes  | 160GB         | Yes | No  |
| Railway.app  | No   | Yes | $5*            | 512MB | 1GB    |      | $0.10/GB      | Yes | Yes |
| render.com   | 15m  | No  | 750 hours      | 512MB |        | No   | 100GB         | Yes | Yes |
| glitch.com   | 5m   | No  | 1000 hours     | 512MB | 200MB* | Yes  | 4000 req/hour | No  |     | 
| fl0.com      | 24h  | No  | invite-only    | 256MB | 1GB?   | Yes  | 5GB           | Yes | Yes |
| Adaptable.io | Yes* | No  | ~25,000 req/mo | 256MB | 1GB    | Yes* | 5GB           | No* | Yes |
| Zeabur.com   | No   | No  | $5             | 512MB | 1GB    | Yes  |               | Yes | Yes |
| Koyeb.com    | Yes* | No  |                | 512MB | 2GB    | Yes  | 100GB         | Yes | Yes |
| Lade.io      | No   | No  |                | 128MB | 1GB    | Yes  | 100GB         | Yes | No  |

\* See information below

## fly.io

[Pricing](https://fly.io/docs/about/pricing/) | [About Free Postgres](https://fly.io/docs/reference/postgres/#about-free-postgres-on-fly) | [Deployment](https://fly.io/docs/app-guides/continuous-deployment-with-github-actions/#speed-run-your-way-to-continuous-deployment)

* Up to 3 shared-cpu-1x 256mb VMs
* Free Postgres
  * single node, 3gb volume (single database)
  * 2x1gb volumes (database in two regions, or a primary and replica in the same region)
  * 3x1gb volumes (database in three regions)

## Railway.app

[Pricing](https://railway.app/pricing) | [Free Trial](https://docs.railway.app/reference/pricing#free-trial) | [Deployment](https://docs.railway.app/deploy/deployments)

* First month: $5 or 500 hours of usage, credit card is not required
* To get free $5/month - credit card is required and you have to be [verified](https://blog.railway.app/p/pricing-and-plans-migration-guide-2023#what%E2%80%99s-the-deal-with-verification):
  * very active GitHub account
  * active usage on Railway
  * no spammy or abusive behaviour detected
* Has Postgres, Redis, MongoDB, MySQL
* Can't run an app 24/7 at a free tier because it offers only 500 hours of usage per month
* Project deploys are stood down if credit limit OR execution hour limit is reached
* Need to redeploy projects after the new monthly credit is applied to your account

<details>
<summary>os.cpus()</summary>

```json
[
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":429977550,"nice":4877620,"sys":100221000,"idle":2236262230,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":530307840,"nice":6992540,"sys":104119280,"idle":2159677140,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":531292710,"nice":6954080,"sys":104655000,"idle":2165640630,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":547151450,"nice":7143210,"sys":105376640,"idle":2151592570,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":552904880,"nice":7234820,"sys":105625660,"idle":2147697520,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":572768080,"nice":7805300,"sys":101886850,"idle":1998757280,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":560505030,"nice":6684900,"sys":107260890,"idle":2134275420,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":573149420,"nice":6695010,"sys":107365710,"idle":2128629600,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":566875240,"nice":6857330,"sys":107589550,"idle":2135357390,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":569532820,"nice":6849130,"sys":107298700,"idle":2134912670,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":569806580,"nice":6872870,"sys":107199790,"idle":2134851970,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":574875360,"nice":4793910,"sys":107062680,"idle":2129160960,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":570777860,"nice":4896690,"sys":106414590,"idle":2139333750,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":570867560,"nice":4870710,"sys":107309590,"idle":2135238060,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":582392240,"nice":4899970,"sys":108861520,"idle":2120797550,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":578386010,"nice":4940840,"sys":108575000,"idle":2125157350,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":520093030,"nice":5064300,"sys":105708810,"idle":2185946050,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":443641460,"nice":5138010,"sys":102879030,"idle":2266763470,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":440584160,"nice":5153180,"sys":101942580,"idle":2271730290,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":427817060,"nice":5236540,"sys":101030220,"idle":2285973890,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":424426660,"nice":4804650,"sys":100285420,"idle":2285252450,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":421252000,"nice":5071310,"sys":99151740,"idle":2296282390,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":415649930,"nice":4844940,"sys":100851290,"idle":2293205670,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":414107010,"nice":4704680,"sys":100748620,"idle":2296303770,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":418074100,"nice":4743990,"sys":101072840,"idle":2294456620,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":412244320,"nice":4795740,"sys":100025830,"idle":2300035030,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":407350930,"nice":4870930,"sys":100091520,"idle":2306181050,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":405358380,"nice":4845980,"sys":99191980,"idle":2308132560,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":404763220,"nice":5067500,"sys":107482530,"idle":2256940970,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":404258000,"nice":4938940,"sys":103694880,"idle":2282950000,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":400346480,"nice":4855750,"sys":101393630,"idle":2296042160,"irq":0}},
  {"model":"Intel(R) Xeon(R) CPU @ 2.20GHz","speed":2199,"times":{"user":398576090,"nice":4846670,"sys":100361930,"idle":2304048900,"irq":0}}
]
```
</details>

## Render.com

[Pricing](https://render.com/pricing) | [Limits for Free Tier](https://render.com/docs/free#free-web-services) | [Deployment](https://render.com/docs/deploys)

* Free Redis: 25MB RAM, 50 connections, No persistence
* Free [DDOS protection](https://render.com/docs/ddos-protection) to every app using Cloudflare
* Free Web Services do not support persistent disks
* Free Web Services can be restarted at any time
* Free Web Services can use up to 400 free build hours per month, shared with static sites

<details>
<summary>os.cpus()</summary>

```json
[
  {"model":"AMD EPYC 7571","speed":2542,"times":{"user":174236890,"nice":41690,"sys":94674930,"idle":476275030,"irq":0}},
  {"model":"AMD EPYC 7571","speed":2547,"times":{"user":186440240,"nice":52690,"sys":102817790,"idle":472428170,"irq":0}},
  {"model":"AMD EPYC 7571","speed":2200,"times":{"user":184893690,"nice":59310,"sys":101664400,"idle":471043630,"irq":0}},
  {"model":"AMD EPYC 7571","speed":2200,"times":{"user":185885080,"nice":54210,"sys":102281640,"idle":473727850,"irq":0}},
  {"model":"AMD EPYC 7571","speed":2200,"times":{"user":191267210,"nice":61690,"sys":105612430,"idle":465391730,"irq":0}},
  {"model":"AMD EPYC 7571","speed":2547,"times":{"user":184773470,"nice":61930,"sys":101221800,"idle":472552340,"irq":0}},
  {"model":"AMD EPYC 7571","speed":2200,"times":{"user":186733720,"nice":70410,"sys":102413860,"idle":472580080,"irq":0}},
  {"model":"AMD EPYC 7571","speed":2547,"times":{"user":186168680,"nice":80780,"sys":102599080,"idle":469537790,"irq":0}}
]
```
</details>

## Glitch

[Pricing](https://glitch.com/pricing) | [Free Tier Restrictions](https://help.glitch.com/kb/article/17-technical-restrictions/) | [Persistence](https://help.glitch.com/kb/article/22-do-you-have-built-in-persistence-or-a-database/) | [Github Action](https://github.com/marketplace/actions/glitch-project-sync)

* Apps are limited to 4000 requests per hour (subsequent requests will return a 429 "Too Many Requests" response).
* Apps have a limit of 200MB of disk space in the container. The contents of your apps's `/tmp` directory currently don't count towards that total. Those files are removed when the app restarts.
* By default your node.js modules don't count towards that total - there's a separate 1GB limit for node modules.
* There's an additional 512MB of assets storage space. The maximum file size per upload is limited to 256MB.

<details>
<summary>os.cpus()</summary>

```json
[
  {"model":"Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz","speed":2499,"times":{"user":392954400,"nice":760542130,"sys":397252320,"idle":2252573240,"irq":0}},
  {"model":"Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz","speed":2499,"times":{"user":329321660,"nice":756776420,"sys":456550360,"idle":2255211520,"irq":0}},
  {"model":"Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz","speed":2499,"times":{"user":382870720,"nice":787021250,"sys":372660160,"idle":2265251340,"irq":0}}
]
```
</details>

## fl0.com

[Builds & Deployments](https://docs.fl0.com/docs/platform/builds-deployments) | [Supported Scenarios](https://docs.fl0.com/docs/supported-scenarios)

* Invite-only from 4th May 2024

<details>
<summary>os.cpus()</summary>

```json
[
  {"model":"Intel(R) Xeon(R) Platinum 8275CL CPU @ 3.00GHz","speed":3617,"times":{"user":256960,"nice":3810,"sys":102520,"idle":28391470,"irq":0}},
  {"model":"Intel(R) Xeon(R) Platinum 8275CL CPU @ 3.00GHz","speed":2999,"times":{"user":274440,"nice":3020,"sys":104220,"idle":28388940,"irq":0}},
  {"model":"Intel(R) Xeon(R) Platinum 8275CL CPU @ 3.00GHz","speed":2999,"times":{"user":274890,"nice":3330,"sys":104990,"idle":28403950,"irq":0}},
  {"model":"Intel(R) Xeon(R) Platinum 8275CL CPU @ 3.00GHz","speed":2999,"times":{"user":305950,"nice":1990,"sys":105790,"idle":28370670,"irq":0}},
  {"model":"Intel(R) Xeon(R) Platinum 8275CL CPU @ 3.00GHz","speed":3608,"times":{"user":284490,"nice":3900,"sys":105520,"idle":28394810,"irq":0}},
  {"model":"Intel(R) Xeon(R) Platinum 8275CL CPU @ 3.00GHz","speed":2999,"times":{"user":301920,"nice":2960,"sys":105020,"idle":28370150,"irq":0}},
  {"model":"Intel(R) Xeon(R) Platinum 8275CL CPU @ 3.00GHz","speed":2999,"times":{"user":285230,"nice":7930,"sys":104650,"idle":28397560,"irq":0}},
  {"model":"Intel(R) Xeon(R) Platinum 8275CL CPU @ 3.00GHz","speed":3600,"times":{"user":404610,"nice":2110,"sys":111550,"idle":28279030,"irq":0}},
  {"model":"Intel(R) Xeon(R) Platinum 8275CL CPU @ 3.00GHz","speed":3675,"times":{"user":321350,"nice":3090,"sys":107030,"idle":28354550,"irq":0}},
  {"model":"Intel(R) Xeon(R) Platinum 8275CL CPU @ 3.00GHz","speed":2999,"times":{"user":318750,"nice":3690,"sys":102570,"idle":28370200,"irq":0}},
  {"model":"Intel(R) Xeon(R) Platinum 8275CL CPU @ 3.00GHz","speed":2999,"times":{"user":314820,"nice":2110,"sys":106290,"idle":28369010,"irq":0}},
  {"model":"Intel(R) Xeon(R) Platinum 8275CL CPU @ 3.00GHz","speed":3598,"times":{"user":320310,"nice":3500,"sys":111890,"idle":28286330,"irq":0}},
  {"model":"Intel(R) Xeon(R) Platinum 8275CL CPU @ 3.00GHz","speed":3599,"times":{"user":313590,"nice":3710,"sys":108010,"idle":28328580,"irq":0}},
  {"model":"Intel(R) Xeon(R) Platinum 8275CL CPU @ 3.00GHz","speed":2999,"times":{"user":300940,"nice":4490,"sys":108260,"idle":28369610,"irq":0}},
  {"model":"Intel(R) Xeon(R) Platinum 8275CL CPU @ 3.00GHz","speed":2999,"times":{"user":290070,"nice":4080,"sys":104160,"idle":28378910,"irq":0}},
  {"model":"Intel(R) Xeon(R) Platinum 8275CL CPU @ 3.00GHz","speed":2999,"times":{"user":414090,"nice":2290,"sys":118980,"idle":28196530,"irq":0}}
]
```
</details>

## Adaptable.io

[Pricing](https://adaptable.io/pricing) | [Deployment](https://adaptable.io/docs/deploying-your-existing-app) | [App requirements](https://adaptable.io/docs/app-guides/deploy-nodejs-app#containerized-app-requirements)

* 37,500 active CPU seconds per month (625 minutes or 10.4 hours).
* 25,000 estimated requests/month for typical REST API.
* Free managed Postgres or MongoDB is included with each app (MS SQL available as add-on).
* Web services do not support persistent disks. Apps can write to local disk, but files will be lost when the app is scaled down or updated.
* Web services cannot perform background tasks (HTTP request processing only). App CPU allocation is set to zero when your app is not processing a network request.
* Web services can be restarted at any time.
* Apps may be paused for abusive use.
* Dockerfile support is not yet released.

## Zeabur.com

[Pricing](https://zeabur.com/pricing) | [Pricing Model](https://docs.zeabur.com/billing/pricing) | [Deployment](https://docs.zeabur.com/get-started)

* Has Postgres, Redis, MongoDB, MySQL and other databases
* Should use about 20% CPU and 100MB RAM to run an app 24/7 at a free tier.
* Include a US$ 5 free credits every month
* Apps do not have to sleep, wake up, spin up or recycle. All front-ends and back-ends are ready on-demand, immediately and at all times.
* Can deploy from pre-built services and templates

<details>
<summary>os.cpus()</summary>

```json
[
  {"model":"AMD EPYC 7B12","speed":2249,"times":{"user":1079889550,"nice":0,"sys":517413340,"idle":1440992040,"irq":0}},
  {"model":"AMD EPYC 7B12","speed":2249,"times":{"user":1098516910,"nice":0,"sys":511087310,"idle":1445546250,"irq":0}},
  {"model":"AMD EPYC 7B12","speed":2249,"times":{"user":1090612360,"nice":0,"sys":512215370,"idle":1480410470,"irq":0}},
  {"model":"AMD EPYC 7B12","speed":2249,"times":{"user":1027847790,"nice":10,"sys":516513570,"idle":1232710880,"irq":0}}
]
```
</details>

## Koyeb.com 

[Pricing](https://www.koyeb.com/pricing) | [Pricing Frequently Asked Questions](https://www.koyeb.com/docs/faqs/pricing) | [Deploy](https://www.koyeb.com/docs/deploy)

* Signing up using a GitHub account lets you join the Hobby plan without adding a credit card
* The app can be paused if you didn't sign into your account for 2 weeks. Notified by email
* One free web Service in the Frankfurt region with 256MB of RAM, 0.1 vCPU, and 2.5GB of SSD
* Anti-DDoS

<details>
<summary>os.cpus()</summary>

```json
[
  { "model": "AMD EPYC", "speed": 0, "times": { "user": 590, "nice": 0, "sys": 1110, "idle": 361200, "irq": 0 } }
]
```
</details>

## Lade.io

[Pricing](https://www.lade.io/pricing) | [Deployment](https://www.lade.io/docs/platform/cli)

* Free services for up to 5 apps or databases
* Free databases include MariaDB, Memcached, MongoDB, MySQL, Postgres, Redis

<details>
<summary>os.cpus()</summary>

```json
[
  {"model":"Intel Core Processor (Haswell, no TSX, IBRS)","speed":2399,"times":{"user":34422500,"nice":7840,"sys":15136040,"idle":1035575260,"irq":0}}
]
```
</details>

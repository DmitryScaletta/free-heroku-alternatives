# Free Heroku Alternatives

Heroku [shuts down their free plans](https://twitter.com/heroku/status/1562817050565054469) so here are some free alternatives to deploy your backend applications.

This comparison describes only free tiers of these services.

|                         | fly.io        | Railway.app     | render.com    | glitch.com        |
| ----------------------- | ------------- | --------------- | ------------- | ----------------- |
| Shutdown for Inactivity | No            | No              | 15 minutes    | 5 minutes         |
| Credit Card             | Not Required* | Not Required    | Not Required  | Not Required      |
| Free Tier Limits        | 2,340 hours   | $5 or 500 hours | 750 hours     | 1000 hours        |
| RAM                     | 256MB         | 512MB           | 512MB         | 512MB             |
| Disk Space              | 1GB, 3GB*     | 1GB             |               | 200MB*            |
| Disk Write Access       | Yes           |                 | No            | Yes               |
| Network Bandwidth       | 160GB         | 100GB           | 100GB         | 4000 req/hour     |
| Can use Dockerfile      | Yes           | Yes             | Yes           | No (only Node.js) |

\* See information below

## fly.io

[Pricing](https://fly.io/docs/about/pricing/) | [About Free Postgres](https://fly.io/docs/reference/postgres/#about-free-postgres-on-fly) | [Deployment](https://fly.io/docs/app-guides/continuous-deployment-with-github-actions/#speed-run-your-way-to-continuous-deployment)

* Without a payment method set
  * You can create up to 2 apps full time with one VM each
  * Run 2 shared-cpu-1x VMs with 256MB RAM full time with time to spare
  * Provision 1GB of persistent volumes for permanent storage

* With a payment method set
  * You can create unlimited apps with many VMs
  * Run 3 shared-cpu-1x VMs with 256MB RAM full time
  * Provision 3GB of persistent volumes for permanent storage

* Free Postgres ([requires a credit card](https://fly.io/blog/free-postgres/))
  * single node, 3gb volume (single database)
  * 2x1gb volumes (database in two regions, or a primary and replica in the same region)
  * 3x1gb volumes (database in three regions)

<details>
  <summary>os.cpus() without a payment method set</summary>

```json
[
  {"model":"AMD EPYC","speed":2595,"times":{"user":50,"nice":0,"sys":70,"idle":118890,"irq":0}}
]
```
</details>

## Railway.app

[Pricing](https://railway.app/pricing) | [About Free Starter Plan](https://docs.railway.app/reference/plans#starter-plan) | [Deployment](https://docs.railway.app/deploy/deployments)

* Github integration for deployment
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
* Free Web Services do not support persistent disks.
* Free Web Services can be restarted at any time.
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

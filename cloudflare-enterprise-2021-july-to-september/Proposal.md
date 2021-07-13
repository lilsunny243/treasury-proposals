# Proposal for Financing Cloudflare's Enterprise Plan for Subscan 

Subscan is an aggregate high-precision blockchain explorer for Substrate-based chains. We have supported several influential blockchains, including Polkadot, Kusama, and Westend, for over a year. For many users, Subscan is their first stop in the blockchain world. As we continue to deliver new features and support more blockchains, our user base is on the steady rise. Therefore, high robustness and availability are currently among our major concerns.

We have been the target of several attempts of DDoS attacks during the past months. Cloudflare is our CDN service provider, and we are on their Public Plan, which has successfully protected us from being severely affected.
![chart-nginx-under-attack](./chart-nginx-under-attack.png)
![chart-gcp-load-balancer-under-attack](./chart-gcp-load-balancer-under-attack.png)

Some users reported cases of service outages in some areas during the month of June. Since our DevOps team built a monitoring dashboard, we noticed the problems shortly after they happened. With careful diagnosis and analysis, we managed to pinpoint the cause. They coincided with the incidents of Cloudflare's Public Service. 
![cloudflare-public-plan-incident-june-2nd](./cloudflare-public-plan-incident-june-2nd.png)
![cloudflare-public-plan-incident-june-8th](./cloudflare-public-plan-incident-june-8th.png)
![cloudflare-public-plan-incident-impacted-subscan](./cloudflare-public-plan-incident-impacted-subscan.png)

After consulting with Cloudflare's technical support team, we realized that their Enterprise Plan could meet our higher availability requirements.

Opting in to Cloudflare's Enterprise Plan can bring about other advantages. Argo smart routing, a bonus feature included in the Enterprise Plan, promises an estimated increase of 30% in speed. 
A large proportion of requests come from mainland China, where Internet access can be unpredictable sometimes. With Cloudflare's Enterprise Plan, we can utilize their China network to offer a fast and reliable experience for visitors inside China.

We have received financial support from Treasury during the past month, and such support proved fruitful. This proposal is for financing Subscan's upgrade to Cloudflare's Enterprise Plan (July 2021-September 2021), which amounts to ****DOTs according to ` $ ?? / 15 = ? DOT`. 

If you need more detailed informatio, feel free to inquire us.

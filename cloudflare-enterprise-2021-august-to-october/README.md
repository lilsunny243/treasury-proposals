# Cloudflare Enterprise Plan for Subscan from August 2021 to October 2021

Subscan is an aggregate high-precision blockchain explorer for Substrate-based chains. We have been supporting several influential blockchains, including Polkadot, Kusama, Rococo, and Westend for over a year. For many users, Subscan is their first stop in the blockchain world. As we continue to deliver new features and support more blockchains, our user base is on the steady rise. Therefore, high robustness and availability are currently among our major concerns.

## Why We Can't Do Without a Firewall?

In the past few months, we have become one of many victims of multiple DDoS attacks. For example, here are some of the screenshots from the Google Cloud Platform Load Balancer and our Nginx monitoring system during one of the attacks:

![](./chart-nginx-under-attack.png)
![](./chart-gcp-load-balancer-under-attack.png)

The attacker generated much more packets and requests per second than usual. This forced us to find a firewall to protect Subscan and filter out DDoS traffic. In the next few days, we enabled Cloudflare as our firewall and CDN provider. However, attackers still point to Subscan as a valuable target. The following chart from Cloudflare shows that it successfully prevented many potential malicious attempts in a day:

![](./cloudflare-firewall-analysis-june-21.png)

Fortunately, we are able to mitigate the impact of those attempts and Subscan has not had any major outage due to DDoS attacks since using Cloudflare.

## Why We Need the Cloudflare Enterprise Plan?

Up until June, we had been utilizing Cloudflare for some months. A considerable number of users reported multiple service interruptions in certain areas during the month. Benefit from the complete monitoring pipeline built by Subscan DevOps team, we noticed and observed the issues shortly after it was raised. For example, here are two dashboard snapshots on June 2nd and June 8th, which showing a very similar phenomenon:

![](./cloudflare-public-plan-incident-june-2nd.png)
![](./cloudflare-public-plan-incident-june-8th.png)

With careful diagnosis and analysis, we managed to pinpoint the cause. They coincided with some Cloudflare incidents of the Pro plan. The screenshot below recorded the announcement and postmortem by our DevOps team explaining the incident at that time:

![](./cloudflare-public-plan-incident-impacted-subscan.png)

After consulting with Cloudflare sales and support, we realized that the enterprise plan is a great choice that meets our high availability requirements, just as they suggested. Argo smart routing, one core feature included in the enterprise plan, can help us re-route the traffic during zonal network failures. The enhanced WAF rules can be even more accurate and effective in blocking the attackers. Beyond that, here are also several features that we can utilize to improve Subscan's accessibility and reliability.

## What Other Features Can the Cloudflare Enterprise Plan Offer to Us?

Opting into the Cloudflare enterprise plan will bring about other advantages besides higher availability.

For example, Argo smart routing promises an estimated increase of 30% in network latency.

Also, a relatively large proportion of Subscan users comes from mainland China, where Internet access can be unpredictable sometimes. With the Cloudflare enterprise plan, we can utilize their China network infrastructure to offer a faster and more reliable experience for visitors inside China.

The technical support for Cloudflare enterprise users is apparently better than other plans as well. We will be able to contact the support engineers, if there is any incident, via emails and even phone calls rather than just tickets. This allows us to become more proactive and advantageous in providing highly avaialble services to Subscan users in the Polkadot ecosystem.

## The Financial Support

We have received financial support from the Polkadot treasury during the past month, and such support proved fruitful. This proposal is for financing Subscan's upgrade to the Cloudflare enterprise plan, which amounts to 967 DOTs. This includes 5000 $USD per month, and 3 months in total (August 2021 ~ October 2021), according to the EMA30 price `1 DOT ≈ 15.5 $USD`.

The quotation of the enterprise plan for Subscan can be found on [GitHub](https://github.com/itering/subscan-treasury-proposals/blob/master/cloudflare-enterprise-2021-august-to-october/cloudflare-enterprise-quotation.xlsx).

In case we missed any information or you have any questions, please feel free to send us an inquiry.

## References

- Cloudflare Enterprise plan: <https://www.cloudflare.com/plans/enterprise/>
- Cloudflare Argo: <https://www.cloudflare.com/products/argo-smart-routing/>
- Cloudflare incident on June 2nd: <https://www.cloudflarestatus.com/incidents/zbzjv8sm3g94>
- Cloudflare incident on June 8th: <https://www.cloudflarestatus.com/incidents/2hnqwq90dlrk>

The source code of this proposal is hosted on [GitHub](https://github.com/itering/subscan-treasury-proposals/tree/master/cloudflare-enterprise-2021-august-to-october).

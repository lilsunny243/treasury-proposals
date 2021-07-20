# Cloudflare Enterprise Plan for Subscan from August 2021 to October 2021

Subscan is an aggregate high-precision blockchain explorer for Substrate-based chains. We have supported several influential blockchains, including Polkadot, Kusama, and Westend over a year. For many users, Subscan is their first stop in the blockchain world. As we continue to deliver new features and support more blockchains, our user base is on the steady rise. Therefore, high robustness and availability are currently among our major concerns.

## Why We Can't Do without Firewall?

In the past few months, we have become one of the victims of DDoS attacks multiple times. For example, there are some of the screenshots from the Google Cloud Platform Load Balancer and our Nginx monitoring system during one of the attacks:

![](./chart-nginx-under-attack.png)
![](./chart-gcp-load-balancer-under-attack.png)

The attacker generated much more packets and requests per second than usual. This forced us to find a firewall to protect Subscan and filter out DDoS traffic. In the next few days, we enabled Cloudflare as our firewall and CDN provider. However, attackers still point to Subscan as a valuable target. The following chart from Cloudflare shows that it successfully prevented many potential malicious attempts in a day:

![](./cloudflare-firewall-analysis-june-21.png)

Fortunately, with Cloudflare, we are able to mitigate the impact of those attempts and Subscan has not been outage due to DDoS attacks since using Cloudflare.

## Why We Need the Cloudflare Enterprise Plan?

In June, we had been utilizing Cloudflare for some months. More than several users reported multiple service interruptions in certain areas during the month. Benefit from the complete monitoring pipeline built by Subscan DevOps team, we noticed and observed the issues shortly after it was raised. For example, there are two dashboard snapshots on June 2nd and June 8th, but showing a very similar phenomenon:

![](./cloudflare-public-plan-incident-june-2nd.png)
![](./cloudflare-public-plan-incident-june-8th.png)

With careful diagnosis and analysis, we managed to pinpoint the cause. They coincided with the Cloudflare incidents of public plans. The screenshot below recorded the announcement and postmortem by our DevOps team explaining the incident at that time:

![](./cloudflare-public-plan-incident-impacted-subscan.png)

After consulting with Cloudflare sales and support, we realized that the Enterprise plan is a great choice that meets our higher availability requirements, just as they suggested. Argo smart routing, one core feature included in the enterprise plan, can help us re-route the traffic during zonal network failures. The enhanced WAF rules can be even more accurate and effective in blocking the attackers. Beyond that, there are also several features that we can utilize to improve Subscan's accessibility and reliability.

## What other features can the Cloudflare Enterprise plan offer to us?

Opting into the Cloudflare enterprise plan will bring about other advantages besides higher availability.

For example, Argo smart routing promises an estimated increase of 30% in network latency.

Also, a relatively large proportion of Subscan users comes from mainland China, where Internet access can be unpredictable sometimes. With the Cloudflare enterprise plan, we can utilize their China network infrastructure to offer a faster and more reliable experience for visitors inside China.

The technical support for Cloudflare enterprise users is apparently better than other plans as well. We will be able to contact the support engineers, if there is any incident, via emails and even phone calls rather than just tickets. This allows us to become more proactive and advantageous in providing highly avaialble services to Subscan users in the Polkadot ecosystem.

## The Financial Support

We have received financial support from Treasury during the past month, and such support proved fruitful. This proposal is for financing Subscan's upgrade to the Cloudflare enterprise plan, which amounts to 937.5 DOTs. This includes 5000 $USD per month, and 3 months (August 2021 ~ October 2021) in total, according to the MA30 price (1 DOT ≈ 16 $USD).

The quotation of the enterprise plan for Subscan can be found on [GitHub](https://github.com/itering/subscan-treasury-proposals/blob/master/cloudflare-enterprise-2021-august-to-october/cloudflare-enterprise-quotation.xlsx).

In case we missed any information or you have any questions, please feel free to inquire us.

## References

- Cloudflare Enterprise plan: <https://www.cloudflare.com/plans/enterprise/>
- Cloudflare Argo: <https://www.cloudflare.com/products/argo-smart-routing/>
- Cloudflare incident on June 2nd: <https://www.cloudflarestatus.com/incidents/zbzjv8sm3g94>
- Cloudflare incident on June 8th: <https://www.cloudflarestatus.com/incidents/2hnqwq90dlrk>

The source code of this proposal is hosted on [GitHub](https://github.com/itering/subscan-treasury-proposals/tree/master/cloudflare-enterprise-2021-august-to-october).

I'm the DevOps engineer from Subscan team to answer the questions and give the community more details on the story of Subscan using Cloudflare.

1. We had other attempts before choosing Cloudflare:

    In fact, we had very similar concerns as you. Before we migrate onto Cloudflare, we've tried a few simpler solutions, such as increasing the number of Nginx instances, optimize the Nginx parameters, enable rate-limiting by client IP address, adding a backup Google Cloud Platform Load Balancer ingress IP and so on. We also consulted Nginx's official blog [Mitigating DDoS Attacks with NGINX and NGINX Plus](https://www.nginx.com/blog/mitigating-ddos-attacks-with-nginx-and-nginx-plus/), to make sure we followed the best practices to tune Nginx.

    But the effect didn't look good. Even we redirected the traffic to the backup load balancer when the primary one is down, the service could have been unavailable for more than a while, because the backup became another target of the attackers shortly.

    We have a complete incident postmortem which includes our attempts while the past attacks. However, I'm afraid we couldn't make it public since it was written in Chinese and contains some sensitive information that is related to monitoring and employment of the company. If the report is helpful to the proposal, we would be happy to provide it privately.

2. We had a research of other solutions while looking for a firewall provider:

    - We initially tend to use the DDoS mitigation service provided by Google Cloud Platform HTTP Load Balancer. However, the problems are:
        1. The GCP load balancers are billed by network bandwidth, the more traffic passes your service, the higher amount it bills. This could lead to an unpredictable cost for Subscan.
        2. As we use the GCP TCP (not HTTP) Load Balancer and maintain an HTTP gateway ourselves, if we migrate to the HTTP load balancer, we would have to give up several customized features in our HTTP gateway, because GCP HTTP Load Balancer doesn't support. It could make us rely on GCP's functionality further as well.

    - Our second option is external firewall/CDN providers, for example, Akamai. The problems are:
        1. Much higher costs than Cloudflare (from the quotation) that we cannot afford currently.
        2. Compares to Anycast that Cloudflare uses, the Unicast technology is relatively older, more "centralized", and has been replacing in many scenarios. This doesn't seem to meet Subscan's general idea.

    - Using an open-source solution and software, deploy our own network infrastructure and firewall is another choice as well. The problems are:
        1. We have limited human resources, lack of suitable engineers to do this.
        2. The cost of building the network infrastructure is too high for Subscan, on the contrary, the availability could be lower than current.

3. We consulted with sales AND support. Our DevOps engineers had multiple meetings with the technical support engineers, which focus on the tech detail of the features included in the enterprise plan. We especially discussed whether the corresponding functions can solve existing problems. This helps us made an independent decision.

    The enterprise plan is also one of the solutions we found proactively after our research mentioned above. Basically, we had conversations with Cloudflare to ask "can the feature XX address the specific issue we had", not "how we can address the issue". We won't talk with them if any cheaper ideas work well, as the Pro plan we've been using for months.

4. Subscan currently cannot deprecate Cloudflare. According to the facts above, we are not able to remove the firewall, or say, Cloudflare:

    - Changing to other providers - they don't have such cost-effective plans.
    - Removing firewalls - Subscan could be outage immediately due to the continuous attacks (see the firewall events screenshot).

    The explorers are the most intuitive experience for end-users. If Subscan's service is impacted due to attacks, users may relate that and blockchain network issues, not just the explorers. Continuing to use the Pro plan instead of adopting the Enterprise plan or deploying other solutions could harm the experience and feelings of the users. I believe this is something we and the Polkadot treasury do not want to see. Therefore, we have aligned interests in this regard.

5. From my personal perspective as a DevOps engineer, Subscan definitely can rely on less 3rd party services or dependencies to be more decentralized, like hiring network engineers and building the network infrastructure. But being a relatively centralized blockchain explorer, the economics benefits of being completely free from external dependencies are too low. We have to somehow figure out and practice the "balance". I think using Cloudflare as a CDN and firewall provider for Subscan doesn't break this balance. Although if in a very low chance that Cloudflare make any malicious move, whether proactive or passive due to being hacked, we can quickly change the provider from Cloudflare to any other available options (e.g. Akamai). Subscan still has the control and any data rows stored in Subscan's database won't be tampered with. Utilizing Anycast provided by Cloudflare can reduce the risk of inaccessibility from the whole global network once if our single ingress endpoint has network failures, which is more decentralized.

I hope this helps answer your questions!

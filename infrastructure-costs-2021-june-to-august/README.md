# The Infrastructure Costs of Subscan for Polkadot Network from June 2021 to August 2021

Subscan is an aggregated Blockchain explorer for Substrate-based chains. We have supported several chains, such as Polkadot, Kusama, and Westend, for more than one year. We have seen an encouraging trend in the number of users and their activeness since last August. However, with the rapid growth of users, stability and reliability in infrastructure are becoming a challenge. We have to pay large bills to ensure the quality of our service.

Subscan is supposed to be a financially independent service in the long run. Although Subscan is starting to generate some revenue, it still falls short for the time being. Therefore, we wish to get some financial support of the Polkadot Treasury to continue our commitment to the improvement of our service.

## Current Service Scale of Subscan

Here are some statistics of the current service scale of Subscan.

![](subscan-cloudflare.png)

![](subscan-qps-per-network.png)

As the charts shows Subscan's RPS (requests per second) and its distribution in the last 2 weeks, we can see that Subscan for Polkadot, Kusama, Westend, and Rococo are still the majority of the Subscan user sources. This value is seeming to decrease gradually, from the last time we submit the proposal ~80% to this season ~70%.

We also launched the [service status page](https://subscan.statuspage.io/) in the last few months. In order to improve the transparency of the Subscan service, some core metrics from our backend monitoring system have been published on it. Any user in the community is able to watch the incidents, scheduled maintenance, along with the real-time request success rate and service response time graph, etc.

## Billing Info

The infrastructure cost refers to what we spent on Subscan on the Google Cloud Platform.

### June 2021

![](cost-table-june.png)

Subtotal in June: $7,384.03

### July 2021

![](cost-table-july.png)

Subtotal in July: $7,865.29

### August 2021

![](cost-table-august.png)

Subtotal in August: $8,643.68

### Total Amount

`$7,384.03 + $7,865.29 + $8,643.68 = $23,893`

*Compute Engine*, *Cloud Logging*, and *Cloud SQL* are the three primary services, among which *Compute Engine* alone constitutes around 70% of the total cost. Detailed billing info and other relevant proof are available in private upon request.

The estimated infrastructure cost we spent on Polkadot, Kusama, Westend, and Rococo adds up to $16,725 according to the request distribution chart. Therefore, the amount we are requesting is 616 DOT (1 DOT ≈ 27.15 $USD). Such support is indispensable for our goal to capitalize on economies of scale.

## References

- Subscan for Polkadot Network: https://polkadot.subscan.io/
- Subscan Service Status: https://subscan.statuspage.io/

The source code of this proposal is hosted on [GitHub](https://github.com/itering/subscan-treasury-proposals/blob/master/infrastructure-costs-2021-june-to-august/).

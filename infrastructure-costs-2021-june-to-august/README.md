# The Infrastructure Costs of Subscan for Polkadot Network from June 2021 to August 2021

Subscan is an aggregated Blockchain explorer for Substrate-based chains. We have supported several chains, such as Polkadot, Kusama, and Westend, for more than one year. We have seen an encouraging trend in the number of users and their level of activity. However, with the rapid growth of users, stability and reliability in infrastructure are becoming a challenge. As a result, Subscan has to expend more resources to ensure the quality of the service.

In the long run, we foresee Subscan is being a financially independent service. Although Subscan is starting to generate some revenue, it currently falls short of supporting the infrastructure costs. Therefore, we are looking for financial support from Polkadot Treasury to help to continue providing a realiable explorer service to the community.

## Current Service Scale of Subscan

Below are some metrics from Cloudflare and Subscan's monitoring system for the last few weeks.

*Subscan traffic overview:*
![](https://github.com/itering/subscan-treasury-proposals/raw/master/infrastructure-costs-2021-june-to-august/subscan-cloudflare.png)

*Subscan API traffic and distribution:*
![](https://github.com/itering/subscan-treasury-proposals/raw/master/infrastructure-costs-2021-june-to-august/subscan-qps-per-network.png)

As the charts demonstrate, Polkadot, Kusama, Westend, and Rococo are the major user traffic of Subscan. This request-per-second value is showing a decreasing trend from ~80% the last time we submitted the proposal to ~70% currently.

We also launched the [service status page](https://subscan.statuspage.io/) in the last few months. In order to improve the transparency of the Subscan service, several core metrics of our backend have been published on it. Any user in the community is able to watch the incidents, scheduled maintenances, real-time request success rate, service response time graph, etc.

![](https://github.com/itering/subscan-treasury-proposals/raw/master/infrastructure-costs-2021-june-to-august/subscan-statuspage-metrics.png)

## Billing Info

The infrastructure cost refers to what we have spent on Google Cloud Platform.

### June 2021

![](https://github.com/itering/subscan-treasury-proposals/raw/master/infrastructure-costs-2021-june-to-august/cost-table-june.png)

Subtotal in June: $7,384.03

### July 2021

![](https://github.com/itering/subscan-treasury-proposals/raw/master/infrastructure-costs-2021-june-to-august/cost-table-july.png)

Subtotal in July: $7,865.29

### August 2021

![](https://github.com/itering/subscan-treasury-proposals/raw/master/infrastructure-costs-2021-june-to-august/cost-table-august.png)

Subtotal in August: $8,643.68

### Total Amount

`$7,384.03 + $7,865.29 + $8,643.68 = $23,893`

*Compute Engine*, *Cloud Logging*, and *Cloud SQL* are the three primary services, among which *Compute Engine* alone constitutes around 70% of the total cost. Detailed billing info and other relevant proof are available upon request.

The estimated infrastructure cost we spent on Polkadot, Kusama, Westend, and Rococo adds up to $16,725 according to the request distribution chart. Therefore, the amount we are requesting is 616 DOT (1 DOT ≈ 27.15 $USD). Such support is indispensable for our goal to capitalize on economies of scale.

## References

- Subscan for Polkadot Network: https://polkadot.subscan.io/
- Subscan Service Status: https://subscan.statuspage.io/

The source code of this proposal is hosted on [GitHub](https://github.com/itering/subscan-treasury-proposals/blob/master/infrastructure-costs-2021-june-to-august/).

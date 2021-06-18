# The Infrastructure Costs of Subscan for Polkadot Network from March 2021 to May 2021

Subscan is an aggregated Blockchain explorer for Substrate-based chains. We have supported several chains, such as Polkadot, Kusama, and Westend, for more than one year. We have seen an encouraging trend in the number of users and their activeness since last August. However, with the rapid growth of users, stability and reliability in infrastructure are becoming a challenge. We have to pay large bills to ensure the quality of our service.

Subscan is supposed to be a financially independent service in the long run. However, although it is starting to generate some revenue, it still falls short for the time being. Therefore, we wish to get some financial support of the Polkadot Treasury to continue our commitment to the improvement of our service.

Following are some statistics of the current service scale of Subscan.

## Current Service Scale of Subscan

![](subscan-cloudflare.png)

![](subscan-qps-per-network.png)

We can see from the charts that Polkadot accounts for the absolute majority of all requests by Subscan.

## Billing Info

The infrastructure cost refers to what we spent on Subscan for Polkadot Network (<https://polkadot.subscan.io/>) on the Google Cloud Platform. Following are the rounded figures for the past three months (March to May 2021).

| March 2021 | April 2021 | May 2021 |  Subtotal |
| ---------: | ---------: | -------: | --------: |
|   $6593.67 |   $6524.53 | $7668.53 | $20786.73 |

![](cost-table-march.png)

![](cost-table-april.png)

![](cost-table-may.png)

*Compute Engine*, *Stackdriver Logging*, and *Cloud SQL* are the three primary services, among which *Compute Engine* alone constitutes around 80% of the total cost. Detailed billing info and other relevant proof are available in private upon request.

The estimated infrastructure cost we spent on Polkadot adds up to $18,000. Therefore, the amount we are requesting is 780 DOT (1 DOT ≈ 23 $USD). Such support is indispensable for our goal to capitalize on economies of scale.

## References

- Subscan for Polkadot Network: https://polkadot.subscan.io/
- Subscan Service Status: https://subscan.statuspage.io/

The source code of this proposal is hosted on [GitHub](https://github.com/itering/subscan-treasury-proposals/blob/master/infrastructure-costs-2021-march-to-may/polkadot.md).

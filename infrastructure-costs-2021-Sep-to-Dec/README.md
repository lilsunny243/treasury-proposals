# The Infrastructure Costs of Subscan for Polkadot Network from Sep 2021 to Dec 2021

Subscan is an aggregated Blockchain explorer for Substrate-based chains. We have supported several chains:

- Relay chain: Polkadot, Kusama
- Testnet: Westend, Rococo
- Public parachain: Statemine

We not just provide basic explorer services for the above networks, and develop new features, optimize the ux and fix bugs as always.
Please refer to the version update document:
> https://medium.com/subscan

Over the past few months，We have seen an encouraging trend in the number of users and their level of activity. However, with the rapid growth of users, stability and reliability in infrastructure are becoming a challenge. As a result, Subscan has to expend more resources to ensure the quality of the service. 

Actually, Subscan is starting to generate some revenue, which mainly comes from the development fee and O&M fee to support the new network. As our original supporters, Parity/W3F helped a lot in the early stage of Subscan. We don't want to charge the team a high premium O&M fee to gain profits, instead we will do more development and research to provide better explorer services to repay the ecosyetem. Therefore, we decided to only apply the necessary infrastructure costs as O&M fees, and the rest of the cost will on the subscan team. 

## Current Service Scale of Subscan

Below are some metrics from Cloudflare and Subscan's monitoring system for the last few weeks.

*Subscan traffic overview:*
![](https://github.com/itering/subscan-treasury-proposals/raw/master/infrastructure-costs-2021-Sep-to-Dec/subscan-cloudflare.png)

*Subscan API traffic and distribution:*
![](https://github.com/itering/subscan-treasury-proposals/raw/master/infrastructure-costs-2021-Sep-to-Dec/subscan-qps-per-network.png)



## Billing Info

The infrastructure cost refers to what we have spent on Google Cloud Platform.

### September 2021

![](https://github.com/itering/subscan-treasury-proposals/raw/master/infrastructure-costs-2021-Sep-to-Dec/9_2021.jpeg)

Subtotal in September: $9,370.69

### October 2021

![](https://github.com/itering/subscan-treasury-proposals/raw/master/infrastructure-costs-2021-Sep-to-Dec/10_2021.jpeg)

Subtotal in October: $8,495.50

### November 2021

![](https://github.com/itering/subscan-treasury-proposals/raw/master/infrastructure-costs-2021-Sep-to-Dec/11_2021.jpeg)

Subtotal in November: $10,057.64

### December 2021

![](https://github.com/itering/subscan-treasury-proposals/raw/master/infrastructure-costs-2021-Sep-to-Dec/12_2021.jpeg)

Subtotal in December: $10,349.90


### Total Amount

`$9,370.69 + $8,495.50 + $10,057.64 + $10,349.90 = $38,273.73`

*Compute Engine*, *Cloud Logging*, and *Cloud SQL* are the three primary services, among which *Compute Engine* alone `constitutes around 75%` of the total cost. Detailed billing info and other relevant proof are available upon request.

The estimated infrastructure cost we spent on Polkadot, Kusama, Westend, and Rococo adds up to `$28,705` according to the request distribution chart. Therefore, the amount we are requesting is `1354 DOT (1 DOT ≈ 21.20 $USD)`. Such support is indispensable for our goal to capitalize on economies of scale.

## References

- Subscan for Polkadot Network: https://polkadot.subscan.io/
- Subscan Service Status: https://subscan.statuspage.io/

The source code of this proposal is hosted on [GitHub](https://github.com/itering/subscan-treasury-proposals/blob/master/infrastructure-costs-2021-Sep-to-Dec/).

# Subscan Multi-sig Treasury Proposal

`Multisig` is an important module in the Substrate ecological network, which is of great significance for the fund management and permissions. It is widely integrated into the runtime by the networks that developed based on Substrate, and is gradually accepted and used by more users.

Subscan multi-sig app is designed to help users create and manage multi-signature accounts and extrinsics. We keep working to provide users with a more convenient multi-signature tool, and will aim for this goal in the future.

Since [the grant delivery](https://github.com/w3f/Grant-Milestone-Delivery/blob/master/deliveries/multisignature_management_tool_milestone_2.md) in Aug 2021, we have also fixed some disturbing bugs, and have been adding many new exciting features and enhancing UI/ UX for the multi-sig tool.

The goal of this proposal is to seek funds for the new features developed for [Subscan multi-sig app](https://github.com/itering/subscan-multisig-react). These new features are divided into 3 Milestones, and we have completed Milestone 1 and 2. More details can be found on Github:

- [Milestone 1: August-December 2021](https://github.com/itering/subscan-multisig-react/milestone/1)
- [Milestone 2: January-March 2022](https://github.com/itering/subscan-multisig-react/milestone/2)
- [Milestone 3: April-June 2022](https://github.com/itering/subscan-multisig-react/milestone/3)

It can be seen that the number of commits is much more than Issues. Many small features are not recorded here, and the actual workload will be more.

In summary, our work focuses on two points:

- Make it more convenient for users to use multi-signature related functions.
- Improve compatibility and facilitate more network integration.

We sincerely welcome suggestions and feedbacks from the community to help us improve UX. Over the next 3 months, we will complete Milestone 3 and add more community-requested features.

**Here are some details of the main features:**

- Custom endpoints for new network
The default support networks include Polkadot, Kusama, Darwinia, Crab and Pangolin. Users can now add custom substrate-based chain by configuring name, endpoint and explorer(optional).
With this function, we can now serve all networks with standard multisig modules, without the trouble to deploy another fork instance. Thus, it becomes a convenient facility in the Polkadot ecosystem, and users without coding experience can configure networks with ease.
![](./custom-endpoint.png)
[Issue & PR related](https://github.com/itering/subscan-multisig-react/issues/78)

- Historical multi-sig extrinsic indexing
Historical multi-sig extrinsics (including confirmed/cancelled ) are stored and indexed using SubQuery.  Accounts(member account + threshold) with extrinsic history will be stored as well. This is a prerequisite for importing multi-sig account from url.
![](./history-extrinsics.png)
[Issue & PR related](https://github.com/itering/subscan-multisig-react/issues/88)

- Import a multi-sig account (which has multi-sig extrinsic history) from url. (e.g. [https://multisig.subscan.io/account/1x8aa2N2Ar9SQweJv9vsuZn3WYDHu7gMQu1RePjZuBe33Hv#r%3Dwss%3A%2F%2Frpc.polkadot.io](https://multisig.subscan.io/account/1x8aa2N2Ar9SQweJv9vsuZn3WYDHu7gMQu1RePjZuBe33Hv#r%3Dwss%3A%2F%2Frpc.polkadot.io))
We know that a multi-signature account can be assembled and saved locally for the sent multi-signature extrinsic, according to the threshold and member accounts. Thus, when a user shares a url containing an endpoint and a multi-signature address, the corresponding threshold and member accounts are queried and saved locally for information viewing and further operations.
[Issue & PR related](https://github.com/itering/subscan-multisig-react/issues/137)

- Import & export a multi-sig account through json file
Creating a multi-sig account by manually input dozens of member accounts can be quite annoying. This feature can save us the trouble of doing so.
![](./export.png)
![](./import.png)
[Issue & PR related](https://github.com/itering/subscan-multisig-react/issues/121)

- Optimize the acquisition method of call data to adapt to more usage scenarios
When a member initiate an extrinsic from other tools such as [polkadot.js/apps](https://polkadot.js.org/apps/#/explorer), the call data may not store on chain, and user can manually input the call data which will be verified correspondingly.
[Issue & PR related](https://github.com/itering/subscan-multisig-react/issues/61)

- Compatible with metadata v14 upgrade
Some related data structure have changed, such as call data stored on chain. We’ve made relevant adjustment to make it compatible with metadata v14 upgrade.

**UI/UX improvement:**

- Refine the general UI layout.
- Show estimated reserve amount when submitting an extrinsic.
[Issue & PR related](https://github.com/itering/subscan-multisig-react/issues/84)

- Optimize call data display in extrinsic list on account detail page.
[Issue & PR related](https://github.com/itering/subscan-multisig-react/issues/119)

- Distinguish between cancelled extrinsic and confirmed extrinsic.
- Add connection timeout message.
- Optimize wallet list.
[Issue & PR related](https://github.com/itering/subscan-multisig-react/issues/148)

- Show multi-sig account balance.
[Issue & PR related](https://github.com/itering/subscan-multisig-react/issues/94)

- Improve performance and load speed.
[Issue & PR related](https://github.com/itering/subscan-multisig-react/issues/149)

Future plans:

- Optimize network configuration architecture, support external chain submit RPC endpoint and subquery GraphQL endpoint configuration by PR.

    We are committed to building multi-sig tools as an open, highly compatible infrastructure like the polkadot.js app. In order to achieve this goal, we still need to complete these tasks: [Issue & PR related](https://github.com/itering/subscan-multisig-react/issues/157)

    - Open source SubQuery schema/template so that external chain can deploy and host the node by themselves.
    - Submit PR to include the RPC endpoint and subquery GraphQL endpoint into the menu.
    - Automatically check the format and usability of PR (subsequent manual review will be carried out).
    - Update README to provide instructions.


- Batch import/export multi-sig accounts
[Issue & PR related](https://github.com/itering/subscan-multisig-react/issues/138)
- Deploy the SubQuery service for networks that have frequent  multi-sig extrinsics.
[Issue & PR related](https://github.com/itering/subscan-multisig-react/issues/151)
- Simplify transfer operations.
Currently it requires user to select module and call to make transfer extrinsic. To make it easier, we plan to add a separate entrance for transfer.
![](./transfer.png)
[Issue & PR related](https://github.com/itering/subscan-multisig-react/issues/136)

- Add “favorite” and “share” multi-sig account features.
[Issue & PR related](https://github.com/itering/subscan-multisig-react/issues/143)
- Add more community-requested features.
- Add user education docs, videos, etc.

**Funding**
development and maintenance cost:

- [Milestone 1: August-December 2021](https://github.com/itering/subscan-multisig-react/milestone/1): $32,100
- [Milestone 2: January-March 2022](https://github.com/itering/subscan-multisig-react/milestone/2): $35,800
- [Milestone 3: April-June 2022](https://github.com/itering/subscan-multisig-react/milestone/3): $34,400

**Total proposed amount: $102,300**

---

2022-04-05 16:03:48 (+UTC), Block #9743467

DOT EMA30 Price ( USD ): 20.636;

**Number of DOT: 4,957.294**

- [https://polkadot.subscan.io/tools/price_converter?value=102300&type=time&from=USD&to=DOT&time=1649174400](https://polkadot.subscan.io/tools/price_converter?value=102300&type=time&from=USD&to=DOT&time=1649174400)

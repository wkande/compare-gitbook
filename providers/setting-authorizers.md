# Setting Authorizers

We are assuming that you have [configured your Airnode](/provider-guides/configuring-airnode.md) \(and set `endpointId`s of your endpoints\), and [deployed your Airnode](/provider-guides/deploying-airnode.md) and received your `providerId` in your receipt file. Requesters who know your `providerId` and `endpointId`s should now be able to make requests to your endpoints. However, you probably do not want to serve the entire public with your Airnode, but rather

* Only serve your own client contracts
* Only serve requesters who have made a subscription payment
* Only serve requesters who have gone through KYC
* ...

In this guide, we will explain how you can achieve this.


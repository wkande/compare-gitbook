# Setting Authorizers

We are assuming that you have [configured your Airnode](/provider-guides/configuring-airnode.md) \(and set `endpointId`s of your endpoints\), and [deployed your Airnode](/provider-guides/deploying-airnode.md) and received your `providerId` in your receipt file. Requesters who know your `providerId` and `endpointId`s should now be able to make requests to your endpoints. However, you probably do not want to serve the entire public with your Airnode, but rather

* Only serve your own client contracts
* Only serve requesters who have made a subscription payment
* Only serve requesters who have gone through KYC
* ...

In this guide, we will explain how you can achieve this.

## `authorizers`

[`EndpointStore.sol`](/request-response-protocol/general-structure.md#endpointstoresol) keeps a list of [authorizer](/request-response-protocol/authorizer.md) addresses for each `providerId`–`endpointId` pair. An authorizer is a contract that Airnode calls to check if it should respond to a specific request. It can enforce any kind of authorization policy that one could implement as a contract.



## Default state: Deny all

By default, the authorizers of all endpoints of a provider is an empty list. An empty authorizers list means that endpoint is not allowed to be used by anyone. Therefore, after deploying your Airnode, you must also set authorizers for your endpoints for them to be accessible.

Allow all

The simplest authorization policy is opening the endpoint to the public, so let us see how to do that first. Authorizers being set to `[0]` means that all requests made to it will be authorized \(i.e., will be responded to by Airnode\). Only the `providerAdmin` of a provider can update the authorizers of its endpoints. Therefore, you will need to make a transaction using the provider admin address \(that you have set in `config.json` as `providerAdminForRecordCreation`\) to [`EndpointStore.sol`](/request-response-protocol/general-structure.md#endpointstoresol). In JS \(using ethers.js\):




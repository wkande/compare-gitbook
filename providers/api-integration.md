# API Integration

To integrate a System X to a System Y, we need to do three things:

* Specify the interface of System X
* Specify the interface of System Y
* Specify how the interface of System X maps to the interface of System Y

[Oracle Integration Specifications \(OIS\)](/airnode/ois.md) are designed to follow these exact steps:

* API operations are specified
* Oracle endpoints are specified
* Oracle endpoints are mapped to API operations

Therefore, the only thing you need to do to integrate an API to Airnode is to create an OIS. You can do this simply by reading the [OIS docs](/airnode/ois.md) and creating the OIS for your specific API and use-case. This guide aims to follow a more instructive approach and give some tips along the way. Make sure to refer to the [OIS docs](/airnode/ois.md) when you need further details, and you can also refer to the [OAS 3.0.3 docs](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.3.md) about fields related to API specifications.


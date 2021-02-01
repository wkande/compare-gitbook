# Configuring Airnaode

Users configure their Airnodes by providing a `config.json` and a `security.json` file during deployment/redeployment. `config.json` specifies the API–oracle integration specifications in the form of [OIS](/airnode/ois.md)es, but also user-specific configuration details. `security.json` includes security credentials such as API keys. Both [`config.json`](/airnode/config-json.md) and [`security.json`](/airnode/security-json.md) formats are documented, which you can follow to create these files. This guide aims to follow a more instructive approach and give some tips along the way.

We assume that you have already followed the [API integration guide](/provider-guides/api-integration.md) and created your OIS. Similar to the [OIS template](/templates/ois.json) we have provided in the previous guide, we have a [`config.json` template](/templates/config.json) and a [`security.json` template](/templates/security.json) for this guide. Download these files and see the [template notation information](/provider-guides/api-integration.md#ois-template).


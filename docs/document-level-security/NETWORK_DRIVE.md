### Setting up the Network Drive connector

See the [Developer guide](../../docs/DEVELOPING.md) for setting up connectors.

## Document level security

Document level security (DLS) enables you to restrict access to documents based on a userís permissions. This feature is available by default for the Network Drive connector.
Network drive connector DLS supports each kind of permission such as folder & file permissions and is shared with individuals or groups.

The native Netowrk Drive connector will offer DLS support for Windows Network Drive only.

Refer to [document level security](https://www.elastic.co/guide/en/enterprise-search/master/dls.html) for more information.

**Note:** Refer to [DLS in Search Applications](https://www.elastic.co/guide/en/enterprise-search/master/dls-e2e-guide.html) to learn how to ingest data from Network Drive with DLS enabled, when building a search application.

## Additional Pre-requisite

In order to fetch users and groups in the Network Drive, the account credentials added in the configurations, should have access to the Powershell of the Windows Server where the Network Drive is hosted.

#### Additional Configuration

##### `Enable document level security`

Toggle to enable [document level security (DLS)](https://www.elastic.co/guide/en/enterprise-search/master/dls.html). When enabled:
- Full syncs will fetch access control lists for each document and store them in the `_allow_access_control` field.
- Access control syncs will fetch users' access control lists and store them in a separate index.

# ![LOGO](logo.png) DnsManagementClient **flow**ground Connector

## Description

A generated **flow**ground connector for the DnsManagementClient API (version 2018-05-01).

Generated from: https://api.apis.guru/v2/specs/azure.com/dns/2018-05-01/swagger.json<br/>
Generated at: 2019-05-07T17:38:06+03:00

## API Description

The DNS Management Client.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Lists the DNS zones in all resource groups in a subscription.

*Tags:* `Zones`

#### Input Parameters
* `$top` - _optional_ - The maximum number of DNS zones to return. If not specified, returns up to 100 zones.
* `api-version` - _required_ - Specifies the API version.
* `subscriptionId` - _required_ - Specifies the Azure subscription ID, which uniquely identifies the Microsoft Azure subscription.

### Returns the DNS records specified by the referencing targetResourceIds.

#### Input Parameters
* `api-version` - _required_ - Specifies the API version.
* `subscriptionId` - _required_ - Specifies the Azure subscription ID, which uniquely identifies the Microsoft Azure subscription.

### Lists the DNS zones within a resource group.

*Tags:* `Zones`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `$top` - _optional_ - The maximum number of record sets to return. If not specified, returns up to 100 record sets.
* `api-version` - _required_ - Specifies the API version.
* `subscriptionId` - _required_ - Specifies the Azure subscription ID, which uniquely identifies the Microsoft Azure subscription.

### Deletes a DNS zone. WARNING: All DNS records in the zone will also be deleted. This operation cannot be undone.

*Tags:* `Zones`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `zoneName` - _required_ - The name of the DNS zone (without a terminating dot).
* `If-Match` - _optional_ - The etag of the DNS zone. Omit this value to always delete the current zone. Specify the last-seen etag value to prevent accidentally deleting any concurrent changes.
* `api-version` - _required_ - Specifies the API version.
* `subscriptionId` - _required_ - Specifies the Azure subscription ID, which uniquely identifies the Microsoft Azure subscription.

### Gets a DNS zone. Retrieves the zone properties, but not the record sets within the zone.

*Tags:* `Zones`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `zoneName` - _required_ - The name of the DNS zone (without a terminating dot).
* `api-version` - _required_ - Specifies the API version.
* `subscriptionId` - _required_ - Specifies the Azure subscription ID, which uniquely identifies the Microsoft Azure subscription.

### Updates a DNS zone. Does not modify DNS records within the zone.

*Tags:* `Zones`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `zoneName` - _required_ - The name of the DNS zone (without a terminating dot).
* `If-Match` - _optional_ - The etag of the DNS zone. Omit this value to always overwrite the current zone. Specify the last-seen etag value to prevent accidentally overwriting any concurrent changes.
* `api-version` - _required_ - Specifies the API version.
* `subscriptionId` - _required_ - Specifies the Azure subscription ID, which uniquely identifies the Microsoft Azure subscription.

### Creates or updates a DNS zone. Does not modify DNS records within the zone.

*Tags:* `Zones`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `zoneName` - _required_ - The name of the DNS zone (without a terminating dot).
* `If-Match` - _optional_ - The etag of the DNS zone. Omit this value to always overwrite the current zone. Specify the last-seen etag value to prevent accidentally overwriting any concurrent changes.
* `If-None-Match` - _optional_ - Set to '*' to allow a new DNS zone to be created, but to prevent updating an existing zone. Other values will be ignored.
* `api-version` - _required_ - Specifies the API version.
* `subscriptionId` - _required_ - Specifies the Azure subscription ID, which uniquely identifies the Microsoft Azure subscription.

### Lists all record sets in a DNS zone.

*Tags:* `RecordSets`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `zoneName` - _required_ - The name of the DNS zone (without a terminating dot).
* `$top` - _optional_ - The maximum number of record sets to return. If not specified, returns up to 100 record sets.
* `$recordsetnamesuffix` - _optional_ - The suffix label of the record set name that has to be used to filter the record set enumerations. If this parameter is specified, Enumeration will return only records that end with .<recordSetNameSuffix>
* `api-version` - _required_ - Specifies the API version.
* `subscriptionId` - _required_ - Specifies the Azure subscription ID, which uniquely identifies the Microsoft Azure subscription.

### Lists all record sets in a DNS zone.

*Tags:* `RecordSets`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `zoneName` - _required_ - The name of the DNS zone (without a terminating dot).
* `$top` - _optional_ - The maximum number of record sets to return. If not specified, returns up to 100 record sets.
* `$recordsetnamesuffix` - _optional_ - The suffix label of the record set name that has to be used to filter the record set enumerations. If this parameter is specified, Enumeration will return only records that end with .<recordSetNameSuffix>
* `api-version` - _required_ - Specifies the API version.
* `subscriptionId` - _required_ - Specifies the Azure subscription ID, which uniquely identifies the Microsoft Azure subscription.

### Lists the record sets of a specified type in a DNS zone.

*Tags:* `RecordSets`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `zoneName` - _required_ - The name of the DNS zone (without a terminating dot).
* `recordType` - _required_ - The type of record sets to enumerate.
    Possible values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT.
* `$top` - _optional_ - The maximum number of record sets to return. If not specified, returns up to 100 record sets.
* `$recordsetnamesuffix` - _optional_ - The suffix label of the record set name that has to be used to filter the record set enumerations. If this parameter is specified, Enumeration will return only records that end with .<recordSetNameSuffix>
* `api-version` - _required_ - Specifies the API version.
* `subscriptionId` - _required_ - Specifies the Azure subscription ID, which uniquely identifies the Microsoft Azure subscription.

### Deletes a record set from a DNS zone. This operation cannot be undone.

*Tags:* `RecordSets`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `zoneName` - _required_ - The name of the DNS zone (without a terminating dot).
* `relativeRecordSetName` - _required_ - The name of the record set, relative to the name of the zone.
* `recordType` - _required_ - The type of DNS record in this record set. Record sets of type SOA cannot be deleted (they are deleted when the DNS zone is deleted).
    Possible values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT.
* `If-Match` - _optional_ - The etag of the record set. Omit this value to always delete the current record set. Specify the last-seen etag value to prevent accidentally deleting any concurrent changes.
* `api-version` - _required_ - Specifies the API version.
* `subscriptionId` - _required_ - Specifies the Azure subscription ID, which uniquely identifies the Microsoft Azure subscription.

### Gets a record set.

*Tags:* `RecordSets`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `zoneName` - _required_ - The name of the DNS zone (without a terminating dot).
* `relativeRecordSetName` - _required_ - The name of the record set, relative to the name of the zone.
* `recordType` - _required_ - The type of DNS record in this record set.
    Possible values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT.
* `api-version` - _required_ - Specifies the API version.
* `subscriptionId` - _required_ - Specifies the Azure subscription ID, which uniquely identifies the Microsoft Azure subscription.

### Updates a record set within a DNS zone.

*Tags:* `RecordSets`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `zoneName` - _required_ - The name of the DNS zone (without a terminating dot).
* `relativeRecordSetName` - _required_ - The name of the record set, relative to the name of the zone.
* `recordType` - _required_ - The type of DNS record in this record set.
    Possible values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT.
* `If-Match` - _optional_ - The etag of the record set. Omit this value to always overwrite the current record set. Specify the last-seen etag value to prevent accidentally overwriting concurrent changes.
* `api-version` - _required_ - Specifies the API version.
* `subscriptionId` - _required_ - Specifies the Azure subscription ID, which uniquely identifies the Microsoft Azure subscription.

### Creates or updates a record set within a DNS zone.

*Tags:* `RecordSets`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `zoneName` - _required_ - The name of the DNS zone (without a terminating dot).
* `relativeRecordSetName` - _required_ - The name of the record set, relative to the name of the zone.
* `recordType` - _required_ - The type of DNS record in this record set. Record sets of type SOA can be updated but not created (they are created when the DNS zone is created).
    Possible values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT.
* `If-Match` - _optional_ - The etag of the record set. Omit this value to always overwrite the current record set. Specify the last-seen etag value to prevent accidentally overwriting any concurrent changes.
* `If-None-Match` - _optional_ - Set to '*' to allow a new record set to be created, but to prevent updating an existing record set. Other values will be ignored.
* `api-version` - _required_ - Specifies the API version.
* `subscriptionId` - _required_ - Specifies the Azure subscription ID, which uniquely identifies the Microsoft Azure subscription.

## License

**flow**ground :- Telekom iPaaS / azure-com-dns-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.

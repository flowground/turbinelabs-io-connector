# ![LOGO](logo.png) Turbine Labs **flow**ground Connector

## Description

A generated **flow**ground connector for the Turbine Labs API (version 1.0).

Generated from: https://api.apis.guru/v2/specs/turbinelabs.io/1.0/swagger.json<br/>
Generated at: 2019-05-07T17:44:32+03:00

## API Description

The Turbine Labs API provides CRUD operations for core object types, and is
mostly RESTy. The easiest way to interact with the API is with
[tbnctl](https://docs.turbinelabs.io/advanced/tbnctl.html).
If you want to make direct HTTP calls, however, you can obtain an access
token using tbnctl, and then pass it in the Authorization header,
prefixed by `Token `:
```console
curl -H "Authorization: Token <access token>" https://api.turbinelabs.io/v1.0/cluster
```


## Authorization

Supported authorization schemes:
- API Key
## Actions

### Returns the user object for the account authorized and making this request.

> Request the user object for an authorized requesting account.

*Tags:* `User Management`

### Delete the specified access token.

*Tags:* `User Management`

#### Input Parameters
* `access-token-key` - _required_ - the key of the Access Token that should be deleted
* `checksum` - _required_ - the current checksum of the user to be modified

### Lists Access Tokens that are configured for the authenticated user.

*Tags:* `User Management`

### Creates a new Access Token and associates it with the authenticated user.

*Tags:* `User Management`

### Allows an arbitrary filter to be specified and applied to the org\'s change log.

> Perform an adhoc query against the change log for your org. The filter is a JSON encoded FilterSum as defined in this file.

*Tags:* `Audit Log`

#### Input Parameters
* `filter` - _optional_ - Encoded FilterSums representing the query you would like to execute. See object definition for details.

### get changes related to the indicated cluster

> Gets all changes to a cluster.

*Tags:* `Audit Log`

#### Input Parameters
* `clusterKey` - _required_ - the cluster key to see an audit log for
* `start` - _optional_ - The beginning of the window we want to see changes for; measured in
microseconds since Unix Epoch.

* `end` - _optional_ - The end of the window we want to see changes for; measured in
microseconds since Unix Epoch.

* `max_results` - _optional_ - Determines how many ChangeDescription object should be returned to
the calling code.

* `ref_id` - _optional_ - When paginating a Changelog request start on the entry that comes
immediately before or after this ID (as determined by the direction
argument).

* `direction` - _optional_ - If set to "before" then changes will be returned that occurred before
reference ID. If "after" then changes will be returned that have
occurred since the reference ID.

    Possible values: before, after.

### get changes related to the indicated domain

> Gets all changes to a domain, the proxies that front the specified domain,<br/>
> routes within that domain, the shared rules of each route, the clusters<br/>
> connected via route or shared rules.

*Tags:* `Audit Log`

#### Input Parameters
* `domainKey` - _required_ - the domain key to see an audit log for
* `start` - _optional_ - The beginning of the window we want to see changes for; measured in
microseconds since Unix Epoch.

* `end` - _optional_ - The end of the window we want to see changes for; measured in
microseconds since Unix Epoch.

* `max_results` - _optional_ - Determines how many ChangeDescription object should be returned to
the calling code.

* `ref_id` - _optional_ - When paginating a Changelog request start on the entry that comes
immediately before or after this ID (as determined by the direction
argument).

* `direction` - _optional_ - If set to "before" then changes will be returned that occurred before
reference ID. If "after" then changes will be returned that have
occurred since the reference ID.

    Possible values: before, after.

### get changes related to the indicated route

> Gets all changes to a route, the domains associated with it, the shared<br/>
> rules it references, and the clusters connected to it.

*Tags:* `Audit Log`

#### Input Parameters
* `routeKey` - _required_ - the route key to see an audit log for
* `start` - _optional_ - The beginning of the window we want to see changes for; measured in
microseconds since Unix Epoch.

* `end` - _optional_ - The end of the window we want to see changes for; measured in
microseconds since Unix Epoch.

* `max_results` - _optional_ - Determines how many ChangeDescription object should be returned to
the calling code.

* `ref_id` - _optional_ - When paginating a Changelog request start on the entry that comes
immediately before or after this ID (as determined by the direction
argument).

* `direction` - _optional_ - If set to "before" then changes will be returned that occurred before
reference ID. If "after" then changes will be returned that have
occurred since the reference ID.

    Possible values: before, after.

### get changes related to the indicated SharedRules

> Gets all changes associated with set of Shared Rules; the domains using<br/>
> it and the clusters referenced by it.

*Tags:* `Audit Log`

#### Input Parameters
* `sharedRulesKey` - _required_ - the shared rules key to see an audit log for
* `start` - _optional_ - The beginning of the window we want to see changes for; measured in
microseconds since Unix Epoch.

* `end` - _optional_ - The end of the window we want to see changes for; measured in
microseconds since Unix Epoch.

* `max_results` - _optional_ - Determines how many ChangeDescription object should be returned to
the calling code.

* `ref_id` - _optional_ - When paginating a Changelog request start on the entry that comes
immediately before or after this ID (as determined by the direction
argument).

* `direction` - _optional_ - If set to "before" then changes will be returned that occurred before
reference ID. If "after" then changes will be returned that have
occurred since the reference ID.

    Possible values: before, after.

### get changes in a specified zone

> Retrieve all changes in the specified zone.

*Tags:* `Audit Log`

#### Input Parameters
* `zoneKey` - _required_ - the zone key to see an audit log for
* `start` - _optional_ - The beginning of the window we want to see changes for; measured in
microseconds since Unix Epoch.

* `end` - _optional_ - The end of the window we want to see changes for; measured in
microseconds since Unix Epoch.

* `max_results` - _optional_ - Determines how many ChangeDescription object should be returned to
the calling code.

* `ref_id` - _optional_ - When paginating a Changelog request start on the entry that comes
immediately before or after this ID (as determined by the direction
argument).

* `direction` - _optional_ - If set to "before" then changes will be returned that occurred before
reference ID. If "after" then changes will be returned that have
occurred since the reference ID.

    Possible values: before, after.

### get clusters

> Get a list of clusters

*Tags:* `Cluster`

#### Input Parameters
* `filters` - _optional_ - A JSON encoded array of ClusterFilter objects. The filter is taken
as a union of intersections. In other words an object that matches
every constraint in any ClusterFilter will be included.


### create cluster

> Create a new cluster

*Tags:* `Cluster`

### delete cluster

> Delete an existing cluster

*Tags:* `Cluster`

#### Input Parameters
* `clusterKey` - _required_ - the cluster key
* `checksum` - _required_ - the current checksum of the cluster to be deleted

### get cluster

> Get details for an existing cluster

*Tags:* `Cluster`

#### Input Parameters
* `clusterKey` - _required_ - the cluster key

### modify cluster

> Modify an existing cluster

*Tags:* `Cluster`

#### Input Parameters
* `clusterKey` - _required_ - the cluster key

### add instance

> Add a new instance to a cluster

*Tags:* `Cluster`

#### Input Parameters
* `clusterKey` - _required_ - the cluster to add the instance to

### remove instance

> Remove an instance from a cluster

*Tags:* `Cluster`

#### Input Parameters
* `checksum` - _required_ - the current checksum of the instance to be deleted
* `clusterKey` - _required_ - the cluster to remove an instance from
* `instanceIdentifier` - _required_ - the instance to remove, identified as <host>:<port>

### get domains

> Get a list of domains

*Tags:* `Domain`

#### Input Parameters
* `filters` - _optional_ - A JSON encoded array of DomainFilter objects. The filter is taken
as a union of intersections. In other words an object that matches
every constraint in any DomainFilter will be included.


### create domain

> Create a new domain

*Tags:* `Domain`

### delete domain

> Delete an existing domain

*Tags:* `Domain`

#### Input Parameters
* `domainKey` - _required_ - the domain key
* `checksum` - _required_ - the current checksum of the domain to be deleted

### get domain

> Get details for a single domain

*Tags:* `Domain`

#### Input Parameters
* `domainKey` - _required_ - the domain key

### list listeners

> Get a list of listeners

*Tags:* `Listener`

#### Input Parameters
* `filters` - _optional_ - A JSON encoded array of ListenerFilter objects. The filter is taken
as a union of intersections. In other words an object that matches
every constraint in any ListenerFilter will be included.


### create listener

> Create a new listener

*Tags:* `Listener`

### delete listener

> Delete existing listener

*Tags:* `Listener`

#### Input Parameters
* `listenerKey` - _required_ - the listener key
* `checksum` - _required_ - the current checksum of the listener to be deleted

### get listener

> Get details for a single listener

*Tags:* `Listener`

#### Input Parameters
* `listenerKey` - _required_ - the listener key

### modify listener

> Modify an existing listener

*Tags:* `Listener`

#### Input Parameters
* `listenerKey` - _required_ - the listener key

### list proxies

> Get a list of proxies

*Tags:* `Proxy`

#### Input Parameters
* `filters` - _optional_ - A JSON encoded array of ProxyFilter objects. The filter is taken
as a union of intersections. In other words an object that matches
every constraint in any ProxyFilter will be included.


### create proxy

> Create a new proxy

*Tags:* `Proxy`

### delete proxy

> Delete existing proxy

*Tags:* `Proxy`

#### Input Parameters
* `proxyKey` - _required_ - the proxy key
* `checksum` - _required_ - the current checksum of the proxy to be deleted

### get proxy

> Get details for a single proxy

*Tags:* `Proxy`

#### Input Parameters
* `proxyKey` - _required_ - the proxy key

### get routes

> Get a list of routes

*Tags:* `Route`

#### Input Parameters
* `filters` - _optional_ - A JSON encoded array of RouteFilter objects. The filter is taken
as a union of intersections. In other words an object that matches
every constraint in any RouteFilter will be included.


### create route

> Create a new route

*Tags:* `Route`

### delete route

> Delete an existing route

*Tags:* `Route`

#### Input Parameters
* `routeKey` - _required_ - the route key
* `checksum` - _required_ - the current checksum of the route to be deleted

### get route

> Get details for an existing route

*Tags:* `Route`

#### Input Parameters
* `routeKey` - _required_ - the route key

### modify route

> Modify an existing route

*Tags:* `Route`

#### Input Parameters
* `routeKey` - _required_ - the route key

### get shared_rules

> Get a list of shared_rules

*Tags:* `Shared Rules`

#### Input Parameters
* `filters` - _optional_ - A JSON encoded array of SharedRulesFilter objects. The filter is taken
as a union of intersections. In other words an object that matches
every constraint in any SharedRulesFilter will be included.


### create shared_rules

> Create a new shared_rules object

*Tags:* `Shared Rules`

### delete shared_rules object

> Delete an existing shared_rules object

*Tags:* `Route`

#### Input Parameters
* `sharedRulesKey` - _required_ - the shared_rules key
* `checksum` - _required_ - the current checksum of the shared_rules to be deleted

### get shared_rules object

> Get details for an existing shared_rules object

*Tags:* `Shared Rules`

#### Input Parameters
* `sharedRulesKey` - _required_ - the shared_rules key

### modify shared_rules object

> Modify an existing shared_rules object

*Tags:* `Shared Rules`

#### Input Parameters
* `sharedRulesKey` - _required_ - the shared_rules key

### get a list of zones

> Get all zones. possibly with filters

*Tags:* `Zone`

#### Input Parameters
* `filters` - _optional_ - A JSON encoded array of ZoneFilter objects. The filter is taken
as a union of intersections. In other words an object that matches
every constraint in any ZoneFilter will be included.


### create zone

> Create a new zone.

*Tags:* `Zone`

### delete zone

> Delete a zone.

*Tags:* `Zone`

#### Input Parameters
* `zoneKey` - _required_ - the zone key
* `checksum` - _required_ - the current checksum of the zone to be deleted

### get zone

> Get details for a single zone

*Tags:* `Zone`

#### Input Parameters
* `zoneKey` - _required_ - the zone key

## License

**flow**ground :- Telekom iPaaS / turbinelabs-io-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.

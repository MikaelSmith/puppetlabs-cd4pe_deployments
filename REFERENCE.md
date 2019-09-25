# Reference
<!-- DO NOT EDIT: This document was generated by Puppet Strings -->

## Table of Contents

**Functions**

* [`cd4pe_deployments::delete_node_group`](#cd4pe_deploymentsdelete_node_group): Delete a Puppet Enterprise node group
* [`cd4pe_deployments::get_node_group`](#cd4pe_deploymentsget_node_group): Get information about a Puppet Enterprise node group
* [`cd4pe_deployments::pin_nodes_to_env`](#cd4pe_deploymentspin_nodes_to_env): Pin a list of nodes to Puppet Enterprise environment group

## Functions

### cd4pe_deployments::delete_node_group

Type: Ruby 4.x API

Delete a Puppet Enterprise node group

#### Examples

##### Delete node group 3ed5c6c0-be33-4c62-9f41-a863a282b6ae

```puppet
delete_node_group("3ed5c6c0-be33-4c62-9f41-a863a282b6ae")
```

#### `cd4pe_deployments::delete_node_group(String $node_group_id)`

The cd4pe_deployments::delete_node_group function.

Returns: `Object` success object
* success [Boolean] whether or not the operation was successful

##### Examples

###### Delete node group 3ed5c6c0-be33-4c62-9f41-a863a282b6ae

```puppet
delete_node_group("3ed5c6c0-be33-4c62-9f41-a863a282b6ae")
```

##### `node_group_id`

Data type: `String`

The ID string of the node group

### cd4pe_deployments::get_node_group

Type: Ruby 4.x API

Get information about a Puppet Enterprise node group

#### Examples

##### Get information about node group 3ed5c6c0-be33-4c62-9f41-a863a282b6ae

```puppet
$node_group = get_node_group_info("3ed5c6c0-be33-4c62-9f41-a863a282b6ae")
```

#### `cd4pe_deployments::get_node_group(String $node_group_id)`

The cd4pe_deployments::get_node_group function.

Returns: `NodeGroup` a NodeGroup object:
* `name [String] name of the node group`
* `id [String] the node group's id`
* `description [String] a short description of the node group`
* `environment [String] the name of the environment`
* `environmentTrumps [Boolean] is this an environment group?``
* `parent [String] the name of the parent node group`
* `rule [Array] puppetDB rule`
* `classes [Hash] list of classes assigned to this node group`
* `configData [Hash] node group's configuration`
* `nodes [Array] list of nodes pinned to this group`

##### Examples

###### Get information about node group 3ed5c6c0-be33-4c62-9f41-a863a282b6ae

```puppet
$node_group = get_node_group_info("3ed5c6c0-be33-4c62-9f41-a863a282b6ae")
```

##### `node_group_id`

Data type: `String`

The ID string of the node group

### cd4pe_deployments::pin_nodes_to_env

Type: Ruby 4.x API

Pin a list of nodes to Puppet Enterprise environment group

#### Examples

##### Pin a list of nodes to an environment group

```puppet
$my_cool_node_group_id = "3ed5c6c0-be33-4c62-9f41-a863a282b6ae"
pin_nodes_to_env(["example.node1.net", "example.node2.net", "example.node3.net"], $my_cool_node_group_id)
```

#### `cd4pe_deployments::pin_nodes_to_env(Array $nodes, String $node_group_id)`

The cd4pe_deployments::pin_nodes_to_env function.

Returns: `Object` success object
* success [Boolean] whether or not the operation was sucessful

##### Examples

###### Pin a list of nodes to an environment group

```puppet
$my_cool_node_group_id = "3ed5c6c0-be33-4c62-9f41-a863a282b6ae"
pin_nodes_to_env(["example.node1.net", "example.node2.net", "example.node3.net"], $my_cool_node_group_id)
```

##### `nodes`

Data type: `Array`

List of nodes to pin to the group

##### `node_group_id`

Data type: `String`

The ID string of the node group

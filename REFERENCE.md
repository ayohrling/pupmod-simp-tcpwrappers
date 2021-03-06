# Reference
<!-- DO NOT EDIT: This document was generated by Puppet Strings -->

## Table of Contents

**Classes**

* [`tcpwrappers`](#tcpwrappers): Set up tcpwrappers

**Defined types**

* [`tcpwrappers::allow`](#tcpwrappersallow): 

## Classes

### tcpwrappers

Set up tcpwrappers

#### Parameters

The following parameters are available in the `tcpwrappers` class.

##### `default_deny`

Data type: `Boolean`

Add a default ``ALL: ALL`` to ``/etc/hosts.deny``

Default value: `true`

##### `allow_all_local`

Data type: `Boolean`

Allow connections to all services from the local system

* This includes all representations of the local system that are available
  via ``facter`` and shortcut notation, such as ``LOCAL``.

Default value: `true`

##### `package_ensure`

Data type: `String`

The ensure status of packages to be managed

Default value: simplib::lookup('simp_options::package_ensure', { 'default_value' => 'installed' })

## Defined types

### tcpwrappers::allow

The tcpwrappers::allow class.

#### Parameters

The following parameters are available in the `tcpwrappers::allow` defined type.

##### `pattern`

Data type: `Variant[String,Array[String]]`

The allow pattern based on the content of the man page

##### `order`

Data type: `Integer`

The order in which you want this rule to appear

* IF you don't specify an order, the rules will be listed in alphabetical
  order

Default value: 1000

##### `svc`

Data type: `Optional[String]`

The name of the service

* This is useful if you wish to use the same service name more than once

Default value: `undef`


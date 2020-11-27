## Requirements

The following requirements are needed by this module:

- helm (~> 1.3.2)

- kubernetes (~> 1.13.3)

## Providers

The following providers are used by this module:

- aws

- helm (~> 1.3.2)

- kubernetes (~> 1.13.3)

- template

- terraform

## Required Inputs

The following input variables are required:

### aws\_acct\_no

Description: Base AWS Account Number for the Project; e.g. 00000000000

Type: `string`

### builder

Description: AWS UserID of the person who Ran the Terraform last.

Type: `string`

### dns\_zone

Description: Domain where the Project Lives; if prod just base domain, else; e.g. <env>.<domain

Type: `string`

### domain

Description: Base Domain on AWS; e.g. domain.tld

Type: `string`

### host\_cidr

Description: Classless Inter-Domain Routing; e.g. 10.1.0.0/16

Type: `string`

### kubeNode\_type

Description: Define Pod Size for Project; e.g. t2.micro

Type: `string`

### minDistSize

Description: Minium Distribution size for Subnet, Cluster, and more..

Type: `number`

### myCo

Description: Shortname of the Company; e.g. acme-co

Type: `string`

### myProject

Description: Base Project Name; e.g. test

Type: `string`

### projectType

Description: Unique Project Type; e.g. r-n-d

Type: `string`

### region

Description: AWS Region the project will process in.

Type: `string`

### sre\_users

Description: Site Reliability Engineers to create Associated Account Permissions on the Kubernetes Cluster.

Type: `list(string)`

### twoOctets

Description: First two Octets for a CIDR; e.g. 10.25

Type: `string`

## Optional Inputs

The following input variables are optional (have default values):

### db\_cloudwatch

Description: Cloudwatch Logs Exports

Type: `list(string)`

Default:

```json
[
  "postgresql",
  "upgrade"
]
```

### db\_port

Description: Database Port

Type: `number`

Default: `5432`

### db\_type

Description: AWS Database Type

Type: `string`

Default: `"postgres"`

### db\_verison

Description: Database Version

Type: `string`

Default: `"11.6"`

### envBuild

Description: Build Environment; e.g. dev, stage or prod

Type: `string`

Default: `"dev"`

### maxDistSize

Description: Maxium Distribution size for Subnet, Cluster, and more..

Type: `number`

Default: `6`

### project

Description: Unique Tag for the Project; e.g. <name>-<env>-<type>

Type: `string`

Default: `"example"`

### subnet\_count

Description: Distribution size for Subnet

Type: `number`

Default: `3`

## Outputs

No output.


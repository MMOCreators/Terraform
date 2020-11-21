## Information

* Code Analysis [Document](code-analysis.md)

![](https://raw.github.com/MMOCreators/Terraform/master/graph.svg?sanitize=true)

## Providers

The following providers are used by this module:

- aws

- random

- tls

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

The following outputs are exported:

### cluster\_ca\_certificate

Description: The base64 encoded certificate data required to communicate with your cluster.

### cluster\_endpoint

Description: The endpoint for your Kubernetes API server.

### cluster\_token

Description: The token to use to authenticate with the cluster.

### database\_endpoint

Description: Database Endpoint

### database\_password

Description: Database Password

### database\_port

Description: Database Port

### database\_username

Description: Database Username

### domain\_zone\_id

Description: Project Domain Zone ID

### node\_group\_arn

Description: ARN for EKS Node Workers, used for SRE Auth via ConfigMap

### ssl\_cert\_arn

Description: ACM Certificate ARN for SSL Cert Validation

### vault\_kms\_key

Description: KMS Key value needed for Vault to Auto-Unseal

### xdns\_arn

Description: Role ARN for External DNS


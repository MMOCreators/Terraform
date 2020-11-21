terraform scan results:

Passed checks: 64, Failed checks: 0, Skipped checks: 0

Check: CKV_AWS_41: "Ensure no hard coded AWS access key and and secret key exists in provider"
	PASSED for resource: aws.default
	File: /provider.tf:2-5
	Guide: https://docs.bridgecrew.io/docs/bc_aws_secrets_5

Check: CKV_AWS_58: "Ensure EKS Cluster has Secrets Encryption Enabled"
	PASSED for resource: aws_eks_cluster.project_cluster
	File: /base/cluster.tf:1-33
	Variable project (of /base/variables.tf) evaluated to value "example" in expression: name = ${var.project}-cluster
	Guide: https://docs.bridgecrew.io/docs/bc_aws_kubernetes_3

Check: CKV_AWS_37: "Ensure Amazon EKS control plane logging enabled for all log types"
	PASSED for resource: aws_eks_cluster.project_cluster
	File: /base/cluster.tf:1-33
	Variable project (of /base/variables.tf) evaluated to value "example" in expression: name = ${var.project}-cluster
	Guide: https://docs.bridgecrew.io/docs/bc_aws_kubernetes_4

Check: CKV_AWS_7: "Ensure rotation for customer created CMKs is enabled"
	PASSED for resource: aws_kms_key.project_cluster_kms
	File: /base/cluster.tf:42-52
	Guide: https://docs.bridgecrew.io/docs/logging_8

Check: CKV_AWS_61: "Ensure IAM role allows only specific principals in account to assume it"
	PASSED for resource: aws_iam_role.project_cluster_iam_role
	File: /base/cluster.tf:54-67
	Guide: https://docs.bridgecrew.io/docs/bc_aws_iam_45

Check: CKV_AWS_60: "Ensure IAM role allows only specific services or principals to assume it"
	PASSED for resource: aws_iam_role.project_cluster_iam_role
	File: /base/cluster.tf:54-67
	Guide: https://docs.bridgecrew.io/docs/bc_aws_iam_44

Check: CKV_AWS_23: "Ensure every security groups rule has a description"
	PASSED for resource: aws_security_group_rule.project_security_rule_cluster_cluster
	File: /base/cluster.tf:92-100
	Guide: https://docs.bridgecrew.io/docs/networking_31

Check: CKV_AWS_24: "Ensure no security groups allow ingress from 0.0.0.0:0 to port 22"
	PASSED for resource: aws_security_group_rule.project_security_rule_cluster_cluster
	File: /base/cluster.tf:92-100
	Guide: https://docs.bridgecrew.io/docs/networking_1-port-security

Check: CKV_AWS_25: "Ensure no security groups allow ingress from 0.0.0.0:0 to port 3389"
	PASSED for resource: aws_security_group_rule.project_security_rule_cluster_cluster
	File: /base/cluster.tf:92-100
	Guide: https://docs.bridgecrew.io/docs/networking_2

Check: CKV_AWS_23: "Ensure every security groups rule has a description"
	PASSED for resource: aws_security_group_rule.project_security_rule_cluster_workers
	File: /base/cluster.tf:101-109
	Guide: https://docs.bridgecrew.io/docs/networking_31

Check: CKV_AWS_24: "Ensure no security groups allow ingress from 0.0.0.0:0 to port 22"
	PASSED for resource: aws_security_group_rule.project_security_rule_cluster_workers
	File: /base/cluster.tf:101-109
	Guide: https://docs.bridgecrew.io/docs/networking_1-port-security

Check: CKV_AWS_25: "Ensure no security groups allow ingress from 0.0.0.0:0 to port 3389"
	PASSED for resource: aws_security_group_rule.project_security_rule_cluster_workers
	File: /base/cluster.tf:101-109
	Guide: https://docs.bridgecrew.io/docs/networking_2

Check: CKV_AWS_23: "Ensure every security groups rule has a description"
	PASSED for resource: aws_security_group.project_clusters_security_group
	File: /base/cluster.tf:110-137
	Guide: https://docs.bridgecrew.io/docs/networking_31

Check: CKV_AWS_24: "Ensure no security groups allow ingress from 0.0.0.0:0 to port 22"
	PASSED for resource: aws_security_group.project_clusters_security_group
	File: /base/cluster.tf:110-137
	Guide: https://docs.bridgecrew.io/docs/networking_1-port-security

Check: CKV_AWS_25: "Ensure no security groups allow ingress from 0.0.0.0:0 to port 3389"
	PASSED for resource: aws_security_group.project_clusters_security_group
	File: /base/cluster.tf:110-137
	Guide: https://docs.bridgecrew.io/docs/networking_2

Check: CKV_AWS_66: "Ensure cloudwatch log groups specify retention days"
	PASSED for resource: aws_cloudwatch_log_group.project_cloudwatch_logs
	File: /base/cluster.tf:148-161
	Guide: https://docs.bridgecrew.io/docs/logging_13

Check: CKV_AWS_49: "Ensure no IAM policies documents allow "*" as a statement's actions"
	PASSED for resource: aws_iam_policy_document.project_cluster_role_policy
	File: /base/cluster.tf:69-80
	Guide: https://docs.bridgecrew.io/docs/bc_aws_iam_43

Check: CKV_AWS_1: "Ensure IAM policies that allow full "*-*" administrative privileges are not created"
	PASSED for resource: aws_iam_policy_document.project_cluster_role_policy
	File: /base/cluster.tf:69-80
	Guide: https://docs.bridgecrew.io/docs/iam_23

Check: CKV_AWS_49: "Ensure no IAM policies documents allow "*" as a statement's actions"
	PASSED for resource: aws_iam_policy_document.external_dns_role_policy
	File: /base/external-dns.tf:17-31
	Guide: https://docs.bridgecrew.io/docs/bc_aws_iam_43

Check: CKV_AWS_1: "Ensure IAM policies that allow full "*-*" administrative privileges are not created"
	PASSED for resource: aws_iam_policy_document.external_dns_role_policy
	File: /base/external-dns.tf:17-31
	Guide: https://docs.bridgecrew.io/docs/iam_23

Check: CKV_AWS_49: "Ensure no IAM policies documents allow "*" as a statement's actions"
	PASSED for resource: aws_iam_policy_document.dns_challenge_policy_document
	File: /base/external-dns.tf:47-71
	Guide: https://docs.bridgecrew.io/docs/bc_aws_iam_43

Check: CKV_AWS_1: "Ensure IAM policies that allow full "*-*" administrative privileges are not created"
	PASSED for resource: aws_iam_policy_document.dns_challenge_policy_document
	File: /base/external-dns.tf:47-71
	Guide: https://docs.bridgecrew.io/docs/iam_23

Check: CKV_AWS_61: "Ensure IAM role allows only specific principals in account to assume it"
	PASSED for resource: aws_iam_role.external_dns
	File: /base/external-dns.tf:34-38
	Variable project (of /base/variables.tf) evaluated to value "example" in expression: name = ${var.project}-external-dns
	Guide: https://docs.bridgecrew.io/docs/bc_aws_iam_45

Check: CKV_AWS_60: "Ensure IAM role allows only specific services or principals to assume it"
	PASSED for resource: aws_iam_role.external_dns
	File: /base/external-dns.tf:34-38
	Variable project (of /base/variables.tf) evaluated to value "example" in expression: name = ${var.project}-external-dns
	Guide: https://docs.bridgecrew.io/docs/bc_aws_iam_44

Check: CKV_AWS_62: "Ensure IAM policies that allow full "*-*" administrative privileges are not created"
	PASSED for resource: aws_iam_role_policy.external_dns_policy
	File: /base/external-dns.tf:41-45
	Guide: https://docs.bridgecrew.io/docs/iam_47

Check: CKV_AWS_63: "Ensure no IAM policies documents allow "*" as a statement's actions"
	PASSED for resource: aws_iam_role_policy.external_dns_policy
	File: /base/external-dns.tf:41-45
	Guide: https://docs.bridgecrew.io/docs/iam_48

Check: CKV_AWS_23: "Ensure every security groups rule has a description"
	PASSED for resource: aws_security_group_rule.project_security_rule_api
	File: /base/nodes.tf:45-53
	Guide: https://docs.bridgecrew.io/docs/networking_31

Check: CKV_AWS_24: "Ensure no security groups allow ingress from 0.0.0.0:0 to port 22"
	PASSED for resource: aws_security_group_rule.project_security_rule_api
	File: /base/nodes.tf:45-53
	Guide: https://docs.bridgecrew.io/docs/networking_1-port-security

Check: CKV_AWS_25: "Ensure no security groups allow ingress from 0.0.0.0:0 to port 3389"
	PASSED for resource: aws_security_group_rule.project_security_rule_api
	File: /base/nodes.tf:45-53
	Guide: https://docs.bridgecrew.io/docs/networking_2

Check: CKV_AWS_23: "Ensure every security groups rule has a description"
	PASSED for resource: aws_security_group_rule.project_security_rule_nodes
	File: /base/nodes.tf:54-62
	Guide: https://docs.bridgecrew.io/docs/networking_31

Check: CKV_AWS_24: "Ensure no security groups allow ingress from 0.0.0.0:0 to port 22"
	PASSED for resource: aws_security_group_rule.project_security_rule_nodes
	File: /base/nodes.tf:54-62
	Guide: https://docs.bridgecrew.io/docs/networking_1-port-security

Check: CKV_AWS_25: "Ensure no security groups allow ingress from 0.0.0.0:0 to port 3389"
	PASSED for resource: aws_security_group_rule.project_security_rule_nodes
	File: /base/nodes.tf:54-62
	Guide: https://docs.bridgecrew.io/docs/networking_2

Check: CKV_AWS_23: "Ensure every security groups rule has a description"
	PASSED for resource: aws_security_group_rule.project_security_rule_node_workers
	File: /base/nodes.tf:63-71
	Guide: https://docs.bridgecrew.io/docs/networking_31

Check: CKV_AWS_24: "Ensure no security groups allow ingress from 0.0.0.0:0 to port 22"
	PASSED for resource: aws_security_group_rule.project_security_rule_node_workers
	File: /base/nodes.tf:63-71
	Guide: https://docs.bridgecrew.io/docs/networking_1-port-security

Check: CKV_AWS_25: "Ensure no security groups allow ingress from 0.0.0.0:0 to port 3389"
	PASSED for resource: aws_security_group_rule.project_security_rule_node_workers
	File: /base/nodes.tf:63-71
	Guide: https://docs.bridgecrew.io/docs/networking_2

Check: CKV_AWS_23: "Ensure every security groups rule has a description"
	PASSED for resource: aws_security_group.project_nodes_security_group
	File: /base/nodes.tf:72-101
	Guide: https://docs.bridgecrew.io/docs/networking_31

Check: CKV_AWS_24: "Ensure no security groups allow ingress from 0.0.0.0:0 to port 22"
	PASSED for resource: aws_security_group.project_nodes_security_group
	File: /base/nodes.tf:72-101
	Guide: https://docs.bridgecrew.io/docs/networking_1-port-security

Check: CKV_AWS_25: "Ensure no security groups allow ingress from 0.0.0.0:0 to port 3389"
	PASSED for resource: aws_security_group.project_nodes_security_group
	File: /base/nodes.tf:72-101
	Guide: https://docs.bridgecrew.io/docs/networking_2

Check: CKV_AWS_61: "Ensure IAM role allows only specific principals in account to assume it"
	PASSED for resource: aws_iam_role.project_nodes_iam_role
	File: /base/nodes.tf:103-116
	Guide: https://docs.bridgecrew.io/docs/bc_aws_iam_45

Check: CKV_AWS_60: "Ensure IAM role allows only specific services or principals to assume it"
	PASSED for resource: aws_iam_role.project_nodes_iam_role
	File: /base/nodes.tf:103-116
	Guide: https://docs.bridgecrew.io/docs/bc_aws_iam_44

Check: CKV_AWS_62: "Ensure IAM policies that allow full "*-*" administrative privileges are not created"
	PASSED for resource: aws_iam_policy.worker_autoscaling
	File: /base/nodes.tf:204-209
	Guide: https://docs.bridgecrew.io/docs/iam_47

Check: CKV_AWS_63: "Ensure no IAM policies documents allow "*" as a statement's actions"
	PASSED for resource: aws_iam_policy.worker_autoscaling
	File: /base/nodes.tf:204-209
	Guide: https://docs.bridgecrew.io/docs/iam_48

Check: CKV_AWS_49: "Ensure no IAM policies documents allow "*" as a statement's actions"
	PASSED for resource: aws_iam_policy_document.project_nodes_role_policy
	File: /base/nodes.tf:118-129
	Guide: https://docs.bridgecrew.io/docs/bc_aws_iam_43

Check: CKV_AWS_1: "Ensure IAM policies that allow full "*-*" administrative privileges are not created"
	PASSED for resource: aws_iam_policy_document.project_nodes_role_policy
	File: /base/nodes.tf:118-129
	Guide: https://docs.bridgecrew.io/docs/iam_23

Check: CKV_AWS_49: "Ensure no IAM policies documents allow "*" as a statement's actions"
	PASSED for resource: aws_iam_policy_document.worker_autoscaling
	File: /base/nodes.tf:152-198
	Guide: https://docs.bridgecrew.io/docs/bc_aws_iam_43

Check: CKV_AWS_1: "Ensure IAM policies that allow full "*-*" administrative privileges are not created"
	PASSED for resource: aws_iam_policy_document.worker_autoscaling
	File: /base/nodes.tf:152-198
	Guide: https://docs.bridgecrew.io/docs/iam_23

Check: CKV_AWS_16: "Ensure all data stored in the RDS is securely encrypted at rest"
	PASSED for resource: aws_db_instance.database_instance
	File: /base/rds.tf:38-58
	Variable db_port (of /base/variables.tf) evaluated to value "5432" in expression: port = ${var.db_port}
	Variable db_verison (of /base/variables.tf) evaluated to value "11.6" in expression: engine_version = ${var.db_verison}
	Variable db_type (of /base/variables.tf) evaluated to value "postgres" in expression: engine = ${var.db_type}
	Guide: https://docs.bridgecrew.io/docs/general_4

Check: CKV_AWS_23: "Ensure every security groups rule has a description"
	PASSED for resource: aws_security_group.project_database
	File: /base/rds.tf:60-98
	Guide: https://docs.bridgecrew.io/docs/networking_31

Check: CKV_AWS_24: "Ensure no security groups allow ingress from 0.0.0.0:0 to port 22"
	PASSED for resource: aws_security_group.project_database
	File: /base/rds.tf:60-98
	Guide: https://docs.bridgecrew.io/docs/networking_1-port-security

Check: CKV_AWS_25: "Ensure no security groups allow ingress from 0.0.0.0:0 to port 3389"
	PASSED for resource: aws_security_group.project_database
	File: /base/rds.tf:60-98
	Guide: https://docs.bridgecrew.io/docs/networking_2

Check: CKV_AWS_23: "Ensure every security groups rule has a description"
	PASSED for resource: aws_security_group_rule.project_cluster_ingress_database
	File: /base/rds.tf:100-108
	Guide: https://docs.bridgecrew.io/docs/networking_31

Check: CKV_AWS_24: "Ensure no security groups allow ingress from 0.0.0.0:0 to port 22"
	PASSED for resource: aws_security_group_rule.project_cluster_ingress_database
	File: /base/rds.tf:100-108
	Guide: https://docs.bridgecrew.io/docs/networking_1-port-security

Check: CKV_AWS_25: "Ensure no security groups allow ingress from 0.0.0.0:0 to port 3389"
	PASSED for resource: aws_security_group_rule.project_cluster_ingress_database
	File: /base/rds.tf:100-108
	Guide: https://docs.bridgecrew.io/docs/networking_2

Check: CKV_AWS_23: "Ensure every security groups rule has a description"
	PASSED for resource: aws_security_group_rule.project_node_ingress_database
	File: /base/rds.tf:110-118
	Guide: https://docs.bridgecrew.io/docs/networking_31

Check: CKV_AWS_24: "Ensure no security groups allow ingress from 0.0.0.0:0 to port 22"
	PASSED for resource: aws_security_group_rule.project_node_ingress_database
	File: /base/rds.tf:110-118
	Guide: https://docs.bridgecrew.io/docs/networking_1-port-security

Check: CKV_AWS_25: "Ensure no security groups allow ingress from 0.0.0.0:0 to port 3389"
	PASSED for resource: aws_security_group_rule.project_node_ingress_database
	File: /base/rds.tf:110-118
	Guide: https://docs.bridgecrew.io/docs/networking_2

Check: CKV_AWS_62: "Ensure IAM policies that allow full "*-*" administrative privileges are not created"
	PASSED for resource: aws_iam_policy.kms_use_policy_for_vault
	File: /base/vault.tf:6-10
	Variable envBuild (of /base/variables.tf) evaluated to value "dev" in expression: name = KMS-Vault-Policy-${var.envBuild}
	Guide: https://docs.bridgecrew.io/docs/iam_47

Check: CKV_AWS_63: "Ensure no IAM policies documents allow "*" as a statement's actions"
	PASSED for resource: aws_iam_policy.kms_use_policy_for_vault
	File: /base/vault.tf:6-10
	Variable envBuild (of /base/variables.tf) evaluated to value "dev" in expression: name = KMS-Vault-Policy-${var.envBuild}
	Guide: https://docs.bridgecrew.io/docs/iam_48

Check: CKV_AWS_7: "Ensure rotation for customer created CMKs is enabled"
	PASSED for resource: aws_kms_key.vault_auto_unseal
	File: /base/vault.tf:35-47
	Guide: https://docs.bridgecrew.io/docs/logging_8

Check: CKV_AWS_49: "Ensure no IAM policies documents allow "*" as a statement's actions"
	PASSED for resource: aws_iam_policy_document.kms_use_policy_document
	File: /base/vault.tf:19-33
	Guide: https://docs.bridgecrew.io/docs/bc_aws_iam_43

Check: CKV_AWS_1: "Ensure IAM policies that allow full "*-*" administrative privileges are not created"
	PASSED for resource: aws_iam_policy_document.kms_use_policy_document
	File: /base/vault.tf:19-33
	Guide: https://docs.bridgecrew.io/docs/iam_23

Check: CKV_AWS_39: "Ensure Amazon EKS public endpoint disabled"
	PASSED for resource: aws_eks_cluster.project_cluster
	File: /base/cluster.tf:1-33
	Variable project (of /base/variables.tf) evaluated to value "example" in expression: name = ${var.project}-cluster
	Guide: https://docs.bridgecrew.io/docs/bc_aws_kubernetes_2

Check: CKV_AWS_38: "Ensure Amazon EKS public endpoint not accessible to 0.0.0.0/0"
	PASSED for resource: aws_eks_cluster.project_cluster
	File: /base/cluster.tf:1-33
	Variable project (of /base/variables.tf) evaluated to value "example" in expression: name = ${var.project}-cluster
	Guide: https://docs.bridgecrew.io/docs/bc_aws_kubernetes_1

Check: CKV_AWS_17: "Ensure all data stored in the RDS bucket is not public accessible"
	PASSED for resource: aws_db_instance.database_instance
	File: /base/rds.tf:38-58
	Variable db_port (of /base/variables.tf) evaluated to value "5432" in expression: port = ${var.db_port}
	Variable db_verison (of /base/variables.tf) evaluated to value "11.6" in expression: engine_version = ${var.db_verison}
	Variable db_type (of /base/variables.tf) evaluated to value "postgres" in expression: engine = ${var.db_type}
	Guide: https://docs.bridgecrew.io/docs/public_2


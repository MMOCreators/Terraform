terraform scan results:

Passed checks: 1, Failed checks: 0, Skipped checks: 0

Check: CKV_AWS_41: "Ensure no hard coded AWS access key and and secret key exists in provider"
	PASSED for resource: aws.default
	File: /provider.tf:2-5
	Guide: https://docs.bridgecrew.io/docs/bc_aws_secrets_5

kubernetes scan results:

Passed checks: 1, Failed checks: 0, Skipped checks: 0

Check: CKV_K8S_21: "The default namespace should not be used"
	PASSED for resource: ConfigMap.aws-auth.kube-system
	File: /output/temp/test.yaml:1-16
	Guide: https://docs.bridgecrew.io/docs/bc_k8s_20


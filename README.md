**Ticket Type:** Task  
**Title:** Output from AWS VPC resources  
**Project:** Cloud Network Infrastructure Deployment  
**Assignee:** You  
**Reporter:** Derek Morgan  
**Priority:** High  
**Labels:** Terraform, AWS  
**Epic Link:** AWS VPC Expansion  
**Sprint:** Sprint 01/Outputs

**Lab Setup**
This lab uses Localstack to simulate an AWS environment. Localstack is already preinstalled in your environment. You don't need keys or to configure the provider. If you'd like to use your own account, feel free to specify your provider configuration and run `unset aws` and `unset terraform` to decouple them from Localstack.

**Description:**

In an `outputs.tf` file, create a Terraform output that will display the information needed for the developers to understand the VPC configuration along with the AWS region and available availability zones.

**Acceptance Criteria:**

> **Note:** If the `terraform validate` command fails, all tasks in the lab will fail!

1\. In `main.tf`, a VPC has been provided for you. Feel free to modify any details or create your own.  
2\. In `datasources.tf`, create data sources to retrieve the AWS region and availability zones.   
3\. In `outputs.tf`, create an output in the following format replaced with your own information *inline*. Do not use an external template:

```
  Region: us-east-1
  VPC Information: 
    ID: vpc-1234567890abcdef0
    CIDR: 10.0.0.0/16
    Available AZs: us-east-1a, us-east-1b, us-east-1c

```

4\. Ensure the formatting is exactly as above with each piece of information on its own line with the VPC Information items indented.   
5\. Apply and output the information. 

**Implementation Notes:**

There are multiple ways to do this. Try at least 2 different ways using the documentation in the implementation notes. When choosing a method, choose the most readable. 

- <a href="https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/vpc" target="_blank">AWS VPC Resource Documentation</a>  
- <a href="https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/availability_zones" target="_blank">AWS Availability Zones Data Source</a>  
- <a href="https://developer.hashicorp.com/terraform/language/values/outputs" target="_blank">Terraform Documentation</a>  
- <a href="https://developer.hashicorp.com/terraform/language/expressions/strings#heredoc-strings" target="_blank">Heredoc Strings</a>  
- <a href="https://developer.hashicorp.com/terraform/language/expressions/strings#escape-sequences" target="_blank">Escape Sequences</a>

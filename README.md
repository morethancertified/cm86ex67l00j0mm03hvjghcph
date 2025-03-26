**Ticket Type:** Task  
**Title:** Output from GitHub resources  
**Project:** Version Control System Deployment  
**Assignee:** You  
**Reporter:** Derek Morgan  
**Priority:** High  
**Labels:** Terraform, GitHub  
**Epic Link:** GitHub Expansion  
**Sprint:** Sprint 01/Outputs

**Description:**

In an `outputs.tf` file, create a Terraform output that will display the information needed for the developers to clone a repo along with the name of the repository owner.

**Acceptance Criteria:**

> **Note:** If the `terraform validate` command fails, all tasks in the lab will fail!

1\. In `main.tf`, create or use an existing repository with the details of your choice in Terraform.  
2\. In `datasources.tf`, create a data source to retrieve the currently authenticated user.   
3\. In `outputs.tf`, create an output in the following format replaced with your own information *inline*. Do not use an external template:

```
  Login: morethancertified
  URL: 
    HTTP: https://github.com/morethancertified/dev-repo.git
    SSH: git@github.com:morethancertified/dev-repo.git

```

4\. Ensure the formatting is exactly as above with each piece of information on its own line with the HTTP and SSH items indented.   
5\. Apply and output the information. 

**Implementation Notes:**

There are multiple ways to do this. Try at least 2 different ways using the documentation in the implementation notes. When choosing a method, choose the most readable. 

- <a href="https://registry.terraform.io/providers/integrations/github/latest/docs" target="_blank">GitHub Provider Documentation</a>  
- <a href="https://developer.hashicorp.com/terraform/language/values/outputs" target="_blank">Terraform Documentation</a>  
- <a href="https://developer.hashicorp.com/terraform/language/expressions/strings#heredoc-strings" target="_blank">Terraform Documentation</a>  
- <a href="https://developer.hashicorp.com/terraform/language/expressions/strings#escape-sequences" target="_blank">Terraform Documentation</a>

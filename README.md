# Azure Devops Pipeline

Description

This project includes an Azure DevOps pipeline specifically designed for managing infrastructure as code using Terraform. It is structured to ensure a clean, efficient, and secure deployment process.

Features:

-CleanUp Stage: Ensures a clean workspace by removing previous builds.
-Terraform Init and Plan Stage: Initializes Terraform and prepares an execution plan to preview changes.
-Approval Stage: A control mechanism for reviewing and approving the proposed changes before they are applied.

Prerequisites:

-Azure DevOps account.
-Access to an Azure subscription and Azure Key Vault.
-Familiarity with Terraform for infrastructure management.


Azure DevOps Pipeline Setup

Overview

The pipeline is integrated with Terraform to manage Azure resources. It follows a three-stage process: cleanup, planning (with Terraform), and an approval stage for the deployment.

Pipeline Stages

1.CleanUp: 
-Removes previous builds to maintain a clean workspace.

2.TerraformInitandPlan:
-Initializes Terraform.
-Runs Terraform plan to create an execution plan.
-Outputs changes as a JSON for review.
-Publishes the plan artifacts for the Approval stage.

3.Approval:
-Depends on the successful completion of the TerraformInitandPlan stage.
-Downloads the Terraform plan artifacts.
-Applies the changes post-approval.

Configuration

-Azure and Terraform specific settings (such as Azure subscription, KeyVault names, and Terraform backend configuration) need to be specified in the pipeline variables.

-Update the variables section in the pipeline YAML with appropriate values.





